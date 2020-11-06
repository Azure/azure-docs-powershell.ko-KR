---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535867"
---
# <span data-ttu-id="9b90d-101">Backup-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b90d-101">Backup-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="9b90d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b90d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b90d-103">KeyVault 관리 저장소 계정을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-103">Backs up a KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b90d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b90d-104">SYNTAX</span></span>

### <span data-ttu-id="9b90d-105">ByStorageAccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b90d-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b90d-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b90d-106">ByStorageAccount</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b90d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b90d-107">DESCRIPTION</span></span>
<span data-ttu-id="9b90d-108">**AzureKeyVaultManagedStorageAccount** cmdlet은 지정 된 관리 저장소 계정을 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-108">The **Backup-AzureKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="9b90d-109">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="9b90d-110">백업 된 저장소 계정은 백업 된 구독의 모든 키 보관소에 복원할 수 있으며,이는 보관소가 동일한 Azure 지역에 있는 경우에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="9b90d-111">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="9b90d-112">자격 증명 모음에서 원본을 실수로 삭제 하는 경우 저장소 계정의 오프 라인 복사본을 유지 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="9b90d-113">키 자격 증명 모음을 사용 하 여 관리 되는 저장소 계정을 만든 후 해당 개체를 다른 Azure 지역에 복제 하 여 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="9b90d-114">**AzureKeyVaultManagedStorageAccount** cmdlet을 사용 하 여 암호화 된 형식으로 관리 저장소 계정을 검색 한 다음 **Restore-AzureKeyVaultManagedStorageAccount** cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-114">Use the **Backup-AzureKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzureKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="9b90d-115">예제의</span><span class="sxs-lookup"><span data-stu-id="9b90d-115">EXAMPLES</span></span>

### <span data-ttu-id="9b90d-116">예제 1: 자동으로 생성 된 파일 이름을 사용 하 여 관리 되는 저장소 계정 백업</span><span class="sxs-lookup"><span data-stu-id="9b90d-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="9b90d-117">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyMSAK 이라는 관리 되는 저장소 계정을 검색 하 고, 해당 관리 저장소 계정의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고, 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="9b90d-118">예제 2: 관리 저장소 계정을 지정 된 파일 이름으로 백업</span><span class="sxs-lookup"><span data-stu-id="9b90d-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="9b90d-119">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyMSAK 이라는 관리 되는 저장소 계정을 검색 하 고, 해당 관리 되는 저장소 계정의 백업을. i a t a i a b 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="9b90d-120">예제 3: 이전에 검색 한 관리 저장소 계정을 지정 된 파일 이름으로 백업 하 고 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="9b90d-121">이 명령은 $msak 이라는 관리 되는 저장소 계정의 백업을 만듭니다. $Msak의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="9b90d-122">변수</span><span class="sxs-lookup"><span data-stu-id="9b90d-122">PARAMETERS</span></span>

### <span data-ttu-id="9b90d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b90d-123">-DefaultProfile</span></span>
<span data-ttu-id="9b90d-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9b90d-125">-Force</span></span>
<span data-ttu-id="9b90d-126">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-126">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b90d-127">-InputObject</span></span>
<span data-ttu-id="9b90d-128">백업할 저장소 계정 번들은 검색 호출의 출력에서 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-129">-이름</span><span class="sxs-lookup"><span data-stu-id="9b90d-129">-Name</span></span>
<span data-ttu-id="9b90d-130">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="9b90d-130">Secret name.</span></span>
<span data-ttu-id="9b90d-131">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9b90d-132">-OutputFile</span></span>
<span data-ttu-id="9b90d-133">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-133">Output file.</span></span>
<span data-ttu-id="9b90d-134">저장소 계정 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="9b90d-135">지정 하지 않으면 기본 파일 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9b90d-136">-VaultName</span></span>
<span data-ttu-id="9b90d-137">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="9b90d-137">Vault name.</span></span>
<span data-ttu-id="9b90d-138">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-139">-확인</span><span class="sxs-lookup"><span data-stu-id="9b90d-139">-Confirm</span></span>
<span data-ttu-id="9b90d-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b90d-141">-WhatIf</span></span>
<span data-ttu-id="9b90d-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b90d-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b90d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b90d-144">CommonParameters</span></span>
<span data-ttu-id="9b90d-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b90d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b90d-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b90d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b90d-147">입력</span><span class="sxs-lookup"><span data-stu-id="9b90d-147">INPUTS</span></span>

### <span data-ttu-id="9b90d-148">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9b90d-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="9b90d-149">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b90d-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9b90d-150">출력</span><span class="sxs-lookup"><span data-stu-id="9b90d-150">OUTPUTS</span></span>

### <span data-ttu-id="9b90d-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b90d-151">System.String</span></span>

## <span data-ttu-id="9b90d-152">상속자</span><span class="sxs-lookup"><span data-stu-id="9b90d-152">NOTES</span></span>

## <span data-ttu-id="9b90d-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b90d-153">RELATED LINKS</span></span>
