---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346670"
---
# <span data-ttu-id="82bf7-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82bf7-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="82bf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="82bf7-103">Key Vault 서비스에서 관리할 키에 대해 지정된 키 자격 증명 모음에 기존 Azure Storage 계정을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="82bf7-104">구문</span><span class="sxs-lookup"><span data-stu-id="82bf7-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82bf7-105">설명</span><span class="sxs-lookup"><span data-stu-id="82bf7-105">DESCRIPTION</span></span>
<span data-ttu-id="82bf7-106">Key Vault에서 관리할 Storage 계정 키에 대한 Key Vault를 사용하여 기존 Azure Storage 계정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="82bf7-107">Storage 계정이 이미 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-107">The Storage Account must already exist.</span></span> <span data-ttu-id="82bf7-108">저장소 키는 호출자에 노출되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="82bf7-109">Key Vault는 다시 생성 기간에 따라 활성 키를 자동으로 다시 생성하고 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="82bf7-110">이 기능의 개요는 Azure Key Vault 관리 스토리지 계정 [- PowerShell을](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82bf7-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="82bf7-111">예제</span><span class="sxs-lookup"><span data-stu-id="82bf7-111">EXAMPLES</span></span>

### <span data-ttu-id="82bf7-112">예제 1: Key Vault로 Azure Storage 계정을 설정하여 키 관리</span><span class="sxs-lookup"><span data-stu-id="82bf7-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="82bf7-113">Key Vault에서 관리할 키에 대해 Key Vault가 있는 Storage 계정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="82bf7-114">활성 키 집합은 'key1'입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-114">The active key set is 'key1'.</span></span> <span data-ttu-id="82bf7-115">이 키는 sas 토큰을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="82bf7-116">Key Vault는 이 명령의 시간부터 다시 생성 기간 후에 'key2' 키를 다시 생성하고 활성 키로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="82bf7-117">이 자동 다시 재생성 프로세스는 90일 간격으로 'key1'과 'key2' 사이에서 계속됩니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="82bf7-118">예제 2: Key Vault에서 클래식 Azure Storage 계정을 설정하여 키 관리</span><span class="sxs-lookup"><span data-stu-id="82bf7-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="82bf7-119">Key Vault에서 관리할 키에 대해 Key Vault가 있는 클래식 저장소 계정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="82bf7-120">활성 키 집합은 '기본'입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="82bf7-121">이 키는 sas 토큰을 생성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="82bf7-122">Key Vault는 이 명령의 시간부터 다시 생성 기간 후에 '보조' 키를 다시 생성하고 활성 키로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="82bf7-123">이 자동 다시 재생성 프로세스는 90일 간격으로 'Primary'와 'Secondary' 간에 계속됩니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="82bf7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82bf7-124">PARAMETERS</span></span>

### <span data-ttu-id="82bf7-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82bf7-125">-AccountName</span></span>
<span data-ttu-id="82bf7-126">Key Vault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="82bf7-127">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bf7-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="82bf7-128">-AccountResourceId</span></span>
<span data-ttu-id="82bf7-129">저장소 계정의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bf7-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="82bf7-130">-ActiveKeyName</span></span>
<span data-ttu-id="82bf7-131">sas 토큰을 생성하는 데 사용되어야 하는 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bf7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82bf7-132">-DefaultProfile</span></span>
<span data-ttu-id="82bf7-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="82bf7-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82bf7-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="82bf7-134">-Disable</span></span>
<span data-ttu-id="82bf7-135">sas 토큰 생성을 위해 관리되는 저장소 계정의 키를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="82bf7-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="82bf7-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="82bf7-137">키를 자동으로 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-137">Auto regenerate key.</span></span> <span data-ttu-id="82bf7-138">true이면 관리되는 저장소 계정의 비활성 키가 자동으로 다시 생성되고 다시 생성 기간 후에 새 활성 키가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="82bf7-139">false이면 관리되는 저장소 계정의 키가 자동으로 다시 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="82bf7-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="82bf7-140">-RegenerationPeriod</span></span>
<span data-ttu-id="82bf7-141">다시 재생성 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-141">Regeneration period.</span></span> <span data-ttu-id="82bf7-142">자동 다시 생성 키를 사용하는 경우 이 값은 관리되는 저장소 계정의 비활성 키gets가 자동으로 다시 생성되고 새 활성 키가 되는 시간(시간)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bf7-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="82bf7-143">-Tag</span></span>
<span data-ttu-id="82bf7-144">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="82bf7-145">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="82bf7-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bf7-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="82bf7-146">-VaultName</span></span>
<span data-ttu-id="82bf7-147">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-147">Vault name.</span></span>
<span data-ttu-id="82bf7-148">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bf7-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82bf7-149">-Confirm</span></span>
<span data-ttu-id="82bf7-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82bf7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82bf7-151">-WhatIf</span></span>
<span data-ttu-id="82bf7-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82bf7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82bf7-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82bf7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82bf7-154">CommonParameters</span></span>
<span data-ttu-id="82bf7-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82bf7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82bf7-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82bf7-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82bf7-157">입력</span><span class="sxs-lookup"><span data-stu-id="82bf7-157">INPUTS</span></span>

### <span data-ttu-id="82bf7-158">System.String</span><span class="sxs-lookup"><span data-stu-id="82bf7-158">System.String</span></span>

### <span data-ttu-id="82bf7-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="82bf7-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="82bf7-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="82bf7-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="82bf7-161">출력</span><span class="sxs-lookup"><span data-stu-id="82bf7-161">OUTPUTS</span></span>

### <span data-ttu-id="82bf7-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82bf7-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="82bf7-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82bf7-163">NOTES</span></span>

## <span data-ttu-id="82bf7-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82bf7-164">RELATED LINKS</span></span>

[<span data-ttu-id="82bf7-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82bf7-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
