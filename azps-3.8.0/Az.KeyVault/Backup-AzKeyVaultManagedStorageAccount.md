---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879258"
---
# <span data-ttu-id="e69eb-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e69eb-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e69eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e69eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e69eb-103">KeyVault 관리 저장소 계정을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="e69eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e69eb-104">SYNTAX</span></span>

### <span data-ttu-id="e69eb-105">ByStorageAccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e69eb-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e69eb-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e69eb-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e69eb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e69eb-107">DESCRIPTION</span></span>
<span data-ttu-id="e69eb-108">**AzKeyVaultManagedStorageAccount** cmdlet은 지정 된 관리 저장소 계정을 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="e69eb-109">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="e69eb-110">백업 된 저장소 계정은 백업 된 구독의 모든 키 보관소에 복원할 수 있으며,이는 보관소가 동일한 Azure 지역에 있는 경우에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="e69eb-111">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="e69eb-112">자격 증명 모음에서 원본을 실수로 삭제 하는 경우 저장소 계정의 오프 라인 복사본을 유지 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="e69eb-113">키 자격 증명 모음을 사용 하 여 관리 되는 저장소 계정을 만든 후 해당 개체를 다른 Azure 지역에 복제 하 여 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="e69eb-114">**AzKeyVaultManagedStorageAccount** cmdlet을 사용 하 여 암호화 된 형식으로 관리 저장소 계정을 검색 한 다음 **Restore-AzKeyVaultManagedStorageAccount** cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="e69eb-115">예제의</span><span class="sxs-lookup"><span data-stu-id="e69eb-115">EXAMPLES</span></span>

### <span data-ttu-id="e69eb-116">예제 1: 자동으로 생성 된 파일 이름을 사용 하 여 관리 되는 저장소 계정 백업</span><span class="sxs-lookup"><span data-stu-id="e69eb-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="e69eb-117">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyMSAK 이라는 관리 되는 저장소 계정을 검색 하 고, 해당 관리 저장소 계정의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고, 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="e69eb-118">예제 2: 관리 저장소 계정을 지정 된 파일 이름으로 백업</span><span class="sxs-lookup"><span data-stu-id="e69eb-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="e69eb-119">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyMSAK 이라는 관리 되는 저장소 계정을 검색 하 고, 해당 관리 되는 저장소 계정의 백업을. i a t a i a b 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="e69eb-120">예제 3: 이전에 검색 한 관리 저장소 계정을 지정 된 파일 이름으로 백업 하 고 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="e69eb-121">이 명령은 $msak 이라는 관리 되는 저장소 계정의 백업을 만듭니다. $Msak의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="e69eb-122">변수</span><span class="sxs-lookup"><span data-stu-id="e69eb-122">PARAMETERS</span></span>

### <span data-ttu-id="e69eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69eb-123">-DefaultProfile</span></span>
<span data-ttu-id="e69eb-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69eb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e69eb-125">-Force</span></span>
<span data-ttu-id="e69eb-126">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="e69eb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e69eb-127">-InputObject</span></span>
<span data-ttu-id="e69eb-128">백업할 저장소 계정 번들은 검색 호출의 출력에서 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="e69eb-129">-이름</span><span class="sxs-lookup"><span data-stu-id="e69eb-129">-Name</span></span>
<span data-ttu-id="e69eb-130">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="e69eb-130">Secret name.</span></span>
<span data-ttu-id="e69eb-131">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="e69eb-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e69eb-132">-OutputFile</span></span>
<span data-ttu-id="e69eb-133">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-133">Output file.</span></span>
<span data-ttu-id="e69eb-134">저장소 계정 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="e69eb-135">지정 하지 않으면 기본 파일 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="e69eb-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e69eb-136">-VaultName</span></span>
<span data-ttu-id="e69eb-137">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="e69eb-137">Vault name.</span></span>
<span data-ttu-id="e69eb-138">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e69eb-139">-확인</span><span class="sxs-lookup"><span data-stu-id="e69eb-139">-Confirm</span></span>
<span data-ttu-id="e69eb-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e69eb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e69eb-141">-WhatIf</span></span>
<span data-ttu-id="e69eb-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e69eb-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e69eb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69eb-144">CommonParameters</span></span>
<span data-ttu-id="e69eb-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e69eb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69eb-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e69eb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69eb-147">입력</span><span class="sxs-lookup"><span data-stu-id="e69eb-147">INPUTS</span></span>

### <span data-ttu-id="e69eb-148">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e69eb-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e69eb-149">출력</span><span class="sxs-lookup"><span data-stu-id="e69eb-149">OUTPUTS</span></span>

### <span data-ttu-id="e69eb-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e69eb-150">System.String</span></span>

## <span data-ttu-id="e69eb-151">상속자</span><span class="sxs-lookup"><span data-stu-id="e69eb-151">NOTES</span></span>

## <span data-ttu-id="e69eb-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e69eb-152">RELATED LINKS</span></span>
