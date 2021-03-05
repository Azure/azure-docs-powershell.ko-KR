---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991144"
---
# <span data-ttu-id="8a606-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a606-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8a606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a606-102">SYNOPSIS</span></span>
<span data-ttu-id="8a606-103">KeyVault 관리 저장소 계정을 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="8a606-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a606-104">SYNTAX</span></span>

### <span data-ttu-id="8a606-105">ByStorageAccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8a606-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a606-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a606-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a606-107">설명</span><span class="sxs-lookup"><span data-stu-id="8a606-107">DESCRIPTION</span></span>
<span data-ttu-id="8a606-108">**Backup-AzKeyVaultManagedStorageAccount** cmdlet은 키 자격 증명 모음에서 지정된 관리 저장소 계정을 다운로드하고 파일에 저장하여 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="8a606-109">다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="8a606-110">자격 증명 모음이 동일한 Azure 지리에 있는 경우 백업된 저장소 계정을 백업된 구독의 모든 키 자격 증명 모음에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="8a606-111">이 cmdlet을 사용하는 일반적인 이유는 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="8a606-112">자격 증명 모음에서 원본을 실수로 삭제하는 경우 저장소 계정의 오프라인 복사본을 유지하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="8a606-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="8a606-113">Key Vault를 사용하여 관리되는 저장소 계정을 만들었다가 이제 개체를 다른 Azure 지역으로 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="8a606-114">**Backup-AzKeyVaultManagedStorageAccount** cmdlet을 사용하여 관리 저장소 계정을 암호화된 형식으로 검색한 다음 **Restore-AzKeyVaultManagedStorageAccount** cmdlet을 사용하여 두 번째 지역에서 키 자격 증명 모음을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="8a606-115">예제</span><span class="sxs-lookup"><span data-stu-id="8a606-115">EXAMPLES</span></span>

### <span data-ttu-id="8a606-116">예제 1: 자동으로 생성된 파일 이름으로 관리되는 저장소 계정 백업</span><span class="sxs-lookup"><span data-stu-id="8a606-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="8a606-117">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyMSAK라는 관리 저장소 계정을 검색하고 해당 관리 저장소 계정의 백업을 자동으로 이름이 지정된 파일에 저장하고 파일 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="8a606-118">예제 2: 지정된 파일 이름으로 관리되는 저장소 계정 백업</span><span class="sxs-lookup"><span data-stu-id="8a606-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="8a606-119">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyMSAK라는 관리 저장소 계정을 검색하고 해당 관리 저장소 계정의 백업을 Backup.Blob이라는 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="8a606-120">예제 3: 이전에 검색한 관리 저장소 계정을 지정된 파일 이름으로 백업하여 메시지가 표시되지 않고 대상 파일을 덮어 니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="8a606-121">이 명령은 관리되는 저장소 계정의 백업을 $msak. 자격 증명 모음의 이름은 $msak. Backup.blob이라는 파일로 VaultName을 지정하여 파일이 이미 있는 경우 파일을 자동으로 덮어 덮어 봅니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="8a606-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a606-122">PARAMETERS</span></span>

### <span data-ttu-id="8a606-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a606-123">-DefaultProfile</span></span>
<span data-ttu-id="8a606-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a606-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8a606-125">-Force</span></span>
<span data-ttu-id="8a606-126">해당 파일이 있는 경우 주어진 파일을 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="8a606-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="8a606-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a606-127">-InputObject</span></span>
<span data-ttu-id="8a606-128">백업할 저장소 계정 번들, 검색 호출의 출력에서 파이프라인을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="8a606-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8a606-129">-Name</span></span>
<span data-ttu-id="8a606-130">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-130">Secret name.</span></span>
<span data-ttu-id="8a606-131">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름의 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="8a606-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="8a606-132">-OutputFile</span></span>
<span data-ttu-id="8a606-133">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-133">Output file.</span></span>
<span data-ttu-id="8a606-134">저장소 계정 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="8a606-135">지정하지 않으면 기본 파일 이름이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="8a606-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a606-136">-VaultName</span></span>
<span data-ttu-id="8a606-137">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-137">Vault name.</span></span>
<span data-ttu-id="8a606-138">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8a606-139">-확인</span><span class="sxs-lookup"><span data-stu-id="8a606-139">-Confirm</span></span>
<span data-ttu-id="8a606-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a606-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a606-141">-WhatIf</span></span>
<span data-ttu-id="8a606-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a606-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a606-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a606-144">CommonParameters</span></span>
<span data-ttu-id="8a606-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a606-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a606-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a606-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a606-147">입력</span><span class="sxs-lookup"><span data-stu-id="8a606-147">INPUTS</span></span>

### <span data-ttu-id="8a606-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8a606-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="8a606-149">출력</span><span class="sxs-lookup"><span data-stu-id="8a606-149">OUTPUTS</span></span>

### <span data-ttu-id="8a606-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8a606-150">System.String</span></span>

## <span data-ttu-id="8a606-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a606-151">NOTES</span></span>

## <span data-ttu-id="8a606-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a606-152">RELATED LINKS</span></span>
