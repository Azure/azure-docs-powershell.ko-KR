---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495326"
---
# <span data-ttu-id="46611-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46611-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="46611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46611-102">SYNOPSIS</span></span>
<span data-ttu-id="46611-103">Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="46611-104">구문</span><span class="sxs-lookup"><span data-stu-id="46611-104">SYNTAX</span></span>

### <span data-ttu-id="46611-105">ByDefinitionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="46611-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46611-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="46611-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46611-107">설명</span><span class="sxs-lookup"><span data-stu-id="46611-107">DESCRIPTION</span></span>
<span data-ttu-id="46611-108">Key Vault에서 Azure Storage 계정을 분해합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="46611-109">이렇게 해서 Azure Storage 계정은 제거되지 않지만 계정 키는 Azure Key Vault에서 관리되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="46611-110">연결된 모든 Key Vault 관리 저장소 SAS 정의도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="46611-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="46611-111">예제</span><span class="sxs-lookup"><span data-stu-id="46611-111">EXAMPLES</span></span>

### <span data-ttu-id="46611-112">예제 1: Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="46611-113">Key Vault 'myvault'에서 Azure Storage 계정 'mystorageaccount'를 디스패치하고 Key Vault가 해당 키를 관리하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="46611-114">'mystorageaccount' 계정은 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="46611-115">이 계정과 연결된 모든 Key Vault 관리 저장소 SAS 정의가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="46611-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="46611-116">예제 2: 사용자 확인 없이 Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="46611-117">Key Vault 'myvault'에서 Azure Storage 계정 'mystorageaccount'를 디스패치하고 Key Vault가 해당 키를 관리하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="46611-118">'mystorageaccount' 계정은 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="46611-119">이 계정과 연결된 모든 Key Vault 관리 저장소 SAS 정의가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="46611-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="46611-120">예제 3: 영구적으로 삭제가 가능한 자격 증명 모음에서 Key Vault 관리 Azure Storage 계정 및 연결된 모든 SAS 정의를 영구적으로 삭제(제거)합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="46611-121">이 예제에서는 이 자격 증명 모음에 대해 소프트 삭제를 사용하도록 설정되어 있는 것으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="46611-122">자격 증명 모음 속성 또는 자격 증명 모음에 있는 엔터티의 RecoveryLevel 특성을 검사하여 이 경우인지를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="46611-123">첫 번째 cmdlet은 Key Vault 'myvault'에서 Azure Storage 계정 'mystorageaccount'를 디스패치하고 Key Vault가 해당 키를 관리하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="46611-124">'mystorageaccount' 계정은 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="46611-125">이 계정과 연결된 모든 Key Vault 관리 저장소 SAS 정의가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="46611-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="46611-126">두 번째 cmdlet은 저장소 계정이 삭제되지만 복구 가능한 상태인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="46611-127">이 상태로 도달하는 데 시간이 다소 필요할 수 있습니다. 시도하기 전에 최대 30초를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="46611-128">세 번째 cmdlet은 저장소 계정을 영구적으로 제거합니다. 복구는 더 이상 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="46611-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46611-129">PARAMETERS</span></span>

### <span data-ttu-id="46611-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46611-130">-AccountName</span></span>
<span data-ttu-id="46611-131">Key Vault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46611-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="46611-132">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46611-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46611-133">-DefaultProfile</span></span>
<span data-ttu-id="46611-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46611-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46611-135">-Force</span><span class="sxs-lookup"><span data-stu-id="46611-135">-Force</span></span>
<span data-ttu-id="46611-136">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46611-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46611-137">-InputObject</span></span>
<span data-ttu-id="46611-138">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="46611-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46611-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="46611-139">-InRemovedState</span></span>
<span data-ttu-id="46611-140">이전에 삭제된 관리되는 저장소 계정을 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="46611-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46611-141">-PassThru</span></span>
<span data-ttu-id="46611-142">Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="46611-143">이 스위치를 지정하면 cmdlet은 삭제된 관리되는 저장소 계정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="46611-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="46611-144">-VaultName</span></span>
<span data-ttu-id="46611-145">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46611-145">Vault name.</span></span>
<span data-ttu-id="46611-146">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46611-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46611-147">-Confirm</span></span>
<span data-ttu-id="46611-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46611-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46611-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46611-149">-WhatIf</span></span>
<span data-ttu-id="46611-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46611-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46611-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46611-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46611-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46611-152">CommonParameters</span></span>
<span data-ttu-id="46611-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46611-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46611-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46611-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46611-155">입력</span><span class="sxs-lookup"><span data-stu-id="46611-155">INPUTS</span></span>

### <span data-ttu-id="46611-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="46611-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="46611-157">출력</span><span class="sxs-lookup"><span data-stu-id="46611-157">OUTPUTS</span></span>

### <span data-ttu-id="46611-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46611-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="46611-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46611-159">NOTES</span></span>

## <span data-ttu-id="46611-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46611-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

