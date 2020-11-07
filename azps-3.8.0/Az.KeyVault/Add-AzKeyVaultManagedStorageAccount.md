---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879277"
---
# <span data-ttu-id="8b1d9-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b1d9-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8b1d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1d9-103">키 자격 증명 모음 서비스에서 관리 하는 키에 대 한 지정 된 키 보관소에 기존 Azure 저장소 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="8b1d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b1d9-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b1d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b1d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8b1d9-106">키 자격 증명 모음에서 관리 하도록 저장소 계정 키에 대 한 키 보관소를 사용 하 여 기존 Azure Storage 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="8b1d9-107">저장소 계정이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-107">The Storage Account must already exist.</span></span> <span data-ttu-id="8b1d9-108">저장소 키는 호출자에 게 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="8b1d9-109">키 보관소는 재생성 기간을 기준으로 활성 키를 자동으로 다시 생성 하 고 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="8b1d9-110">이 기능에 대 한 개요는 [Azure 키 자격 증명 모음 관리 저장소 계정-PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="8b1d9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8b1d9-111">EXAMPLES</span></span>

### <span data-ttu-id="8b1d9-112">예제 1: 키 보관소를 사용 하 여 Azure Storage 계정을 설정 하 여 키를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="8b1d9-113">키 자격 증명 모음에서 키를 관리 하는 데 사용할 키 보관소를 사용 하 여 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="8b1d9-114">활성 키 집합은 ' key1 '입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-114">The active key set is 'key1'.</span></span> <span data-ttu-id="8b1d9-115">이 키는 sas 토큰을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="8b1d9-116">키 자격 증명 모음이이 명령 시간에서 재생성 기간 후에 ' key2 ' 키를 다시 생성 하 고 활성 키로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="8b1d9-117">이 자동 다시 생성 프로세스는 ' key1 ' 및 ' key2 ' 사이에 계속 해 서 90 일간 간격이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="8b1d9-118">예제 2: 키 자격 증명 모음을 사용 하 여 키를 관리 하는 클래식 Azure Storage 계정 설정</span><span class="sxs-lookup"><span data-stu-id="8b1d9-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="8b1d9-119">키 자격 증명 모음에 키를 사용 하 여 해당 키를 관리 하는 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="8b1d9-120">활성 키 집합은 ' 주 '입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="8b1d9-121">이 키는 sas 토큰을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="8b1d9-122">키 자격 증명 모음이이 명령 시간에서 재생성 기간 후에 ' 보조 ' 키를 다시 생성 하 고 활성 키로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="8b1d9-123">이 자동 다시 생성 프로세스는 90 일 간격으로 ' 주 '와 ' 보조 ' 사이에 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="8b1d9-124">변수</span><span class="sxs-lookup"><span data-stu-id="8b1d9-124">PARAMETERS</span></span>

### <span data-ttu-id="8b1d9-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b1d9-125">-AccountName</span></span>
<span data-ttu-id="8b1d9-126">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="8b1d9-127">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="8b1d9-128">-계정 Resourceid</span><span class="sxs-lookup"><span data-stu-id="8b1d9-128">-AccountResourceId</span></span>
<span data-ttu-id="8b1d9-129">저장소 계정의 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="8b1d9-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="8b1d9-130">-ActiveKeyName</span></span>
<span data-ttu-id="8b1d9-131">Sas 토큰을 생성 하는 데 사용 해야 하는 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="8b1d9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1d9-132">-DefaultProfile</span></span>
<span data-ttu-id="8b1d9-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8b1d9-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b1d9-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="8b1d9-134">-Disable</span></span>
<span data-ttu-id="8b1d9-135">Sas 토큰 생성을 위해 관리 저장소 계정의 키를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="8b1d9-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="8b1d9-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="8b1d9-137">자동으로 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-137">Auto regenerate key.</span></span> <span data-ttu-id="8b1d9-138">True 이면 관리 되는 저장소 계정의 비활성 키가 자동으로 다시 생성 되며 재생성 기간 후 새 활성 키가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="8b1d9-139">False 인 경우 관리 저장소 계정의 키가 자동으로 다시 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="8b1d9-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="8b1d9-140">-RegenerationPeriod</span></span>
<span data-ttu-id="8b1d9-141">재생성 기간.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-141">Regeneration period.</span></span> <span data-ttu-id="8b1d9-142">자동 다시 생성 키를 사용 하는 경우이 값은 관리 저장소 계정의 비활성 keygets 재생성 되 고 새 활성 키가 되는 timespan을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="8b1d9-143">태그</span><span class="sxs-lookup"><span data-stu-id="8b1d9-143">-Tag</span></span>
<span data-ttu-id="8b1d9-144">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8b1d9-145">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8b1d9-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8b1d9-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8b1d9-146">-VaultName</span></span>
<span data-ttu-id="8b1d9-147">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="8b1d9-147">Vault name.</span></span>
<span data-ttu-id="8b1d9-148">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8b1d9-149">-확인</span><span class="sxs-lookup"><span data-stu-id="8b1d9-149">-Confirm</span></span>
<span data-ttu-id="8b1d9-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b1d9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b1d9-151">-WhatIf</span></span>
<span data-ttu-id="8b1d9-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b1d9-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b1d9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1d9-154">CommonParameters</span></span>
<span data-ttu-id="8b1d9-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1d9-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b1d9-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1d9-157">입력</span><span class="sxs-lookup"><span data-stu-id="8b1d9-157">INPUTS</span></span>

### <span data-ttu-id="8b1d9-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8b1d9-158">System.String</span></span>

### <span data-ttu-id="8b1d9-159">시스템 Null 허용 ' 1 [[System. TimeSpan, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b1d9-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b1d9-160">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8b1d9-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8b1d9-161">출력</span><span class="sxs-lookup"><span data-stu-id="8b1d9-161">OUTPUTS</span></span>

### <span data-ttu-id="8b1d9-162">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b1d9-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8b1d9-163">상속자</span><span class="sxs-lookup"><span data-stu-id="8b1d9-163">NOTES</span></span>

## <span data-ttu-id="8b1d9-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b1d9-164">RELATED LINKS</span></span>

[<span data-ttu-id="8b1d9-165">Az의 KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b1d9-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
