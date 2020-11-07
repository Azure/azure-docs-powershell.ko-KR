---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878486"
---
# <span data-ttu-id="08681-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08681-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="08681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08681-102">SYNOPSIS</span></span>
<span data-ttu-id="08681-103">키 보관소 관리 Azure 저장소 계정 및 모든 관련 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="08681-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08681-104">SYNTAX</span></span>

### <span data-ttu-id="08681-105">ByDefinitionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="08681-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08681-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="08681-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08681-107">설명은</span><span class="sxs-lookup"><span data-stu-id="08681-107">DESCRIPTION</span></span>
<span data-ttu-id="08681-108">키 자격 증명 모음에서 Azure Storage 계정의 분리를 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="08681-109">Azure 저장소 계정이 제거 되는 것이 아니라 Azure 키 자격 증명 모음에서 관리 되는 계정 키가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08681-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="08681-110">연결 된 모든 키 보관소 관리 저장소 SAS 정의도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08681-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="08681-111">예제의</span><span class="sxs-lookup"><span data-stu-id="08681-111">EXAMPLES</span></span>

### <span data-ttu-id="08681-112">예제 1: 키 보관소를 관리 하는 Azure Storage 계정 및 모든 관련 SAS 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="08681-113">' Mystorageaccount '의 Azure 저장소 계정 및 키 보관소에서 키를 관리 하는 것을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="08681-114">계정 ' mystorageaccount '는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="08681-115">이 계정에 연결 된 모든 키 자격 증명 모음 관리 저장소 SAS 정의가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08681-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="08681-116">예제 2: 키 자격 증명 모음 관리 Azure 저장소 계정 및 모든 관련 SAS 정의를 사용자 확인 없이 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="08681-117">' Mystorageaccount '의 Azure 저장소 계정 및 키 보관소에서 키를 관리 하는 것을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="08681-118">계정 ' mystorageaccount '는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="08681-119">이 계정에 연결 된 모든 키 자격 증명 모음 관리 저장소 SAS 정의가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08681-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="08681-120">예제 3: 키 자격 증명 모음 관리 Azure 저장소 계정 및 소프트 삭제 사용 자격 증명 모음의 모든 관련 SAS 정의를 영구적으로 삭제 (제거) 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="08681-121">이 예제에서는이 자격 증명 모음에 대해 소프트 삭제를 사용할 수 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="08681-122">자격 증명 모음 속성을 검사 하거나 자격 증명 모음에 있는 엔터티의 RecoveryLevel 특성을 확인 하 여 해당 하는 경우 인지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="08681-123">첫 번째 cmdlet은 키 자격 증명 모음 ' mystorageaccount '의 할당량을 끊습니다. 키 보관소의 키 관리를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="08681-124">계정 ' mystorageaccount '는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="08681-125">이 계정에 연결 된 모든 키 자격 증명 모음 관리 저장소 SAS 정의가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08681-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="08681-126">두 번째 cmdlet은 저장소 계정이 삭제 되었지만 복구 가능한 상태 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="08681-127">이 상태에 도달 하는 동안 잠시 시간이 걸릴 수 있습니다. ~ 30s을 허용 하세요.</span><span class="sxs-lookup"><span data-stu-id="08681-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="08681-128">세 번째 cmdlet이 저장소 계정을 영구적으로 제거 합니다-복구는 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="08681-129">변수</span><span class="sxs-lookup"><span data-stu-id="08681-129">PARAMETERS</span></span>

### <span data-ttu-id="08681-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08681-130">-AccountName</span></span>
<span data-ttu-id="08681-131">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08681-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="08681-132">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="08681-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08681-133">-DefaultProfile</span></span>
<span data-ttu-id="08681-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08681-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08681-135">-Force</span><span class="sxs-lookup"><span data-stu-id="08681-135">-Force</span></span>
<span data-ttu-id="08681-136">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="08681-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08681-137">-InputObject</span></span>
<span data-ttu-id="08681-138">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08681-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="08681-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="08681-139">-InRemovedState</span></span>
<span data-ttu-id="08681-140">이전에 삭제 된 관리 저장소 계정을 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="08681-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08681-141">-PassThru</span></span>
<span data-ttu-id="08681-142">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="08681-143">이 스위치가 지정 된 경우 cmdlet은 삭제 된 관리 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="08681-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="08681-144">-VaultName</span></span>
<span data-ttu-id="08681-145">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="08681-145">Vault name.</span></span>
<span data-ttu-id="08681-146">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="08681-147">-확인</span><span class="sxs-lookup"><span data-stu-id="08681-147">-Confirm</span></span>
<span data-ttu-id="08681-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08681-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08681-149">-WhatIf</span></span>
<span data-ttu-id="08681-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08681-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08681-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08681-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08681-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08681-152">CommonParameters</span></span>
<span data-ttu-id="08681-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08681-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08681-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08681-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08681-155">입력</span><span class="sxs-lookup"><span data-stu-id="08681-155">INPUTS</span></span>

### <span data-ttu-id="08681-156">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="08681-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="08681-157">출력</span><span class="sxs-lookup"><span data-stu-id="08681-157">OUTPUTS</span></span>

### <span data-ttu-id="08681-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08681-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="08681-159">상속자</span><span class="sxs-lookup"><span data-stu-id="08681-159">NOTES</span></span>

## <span data-ttu-id="08681-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08681-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

