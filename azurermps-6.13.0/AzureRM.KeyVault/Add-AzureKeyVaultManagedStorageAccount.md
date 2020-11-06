---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: fcef87b196d07ffd7a4ce43bda2cf1c2372910b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530277"
---
# <span data-ttu-id="492ee-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="492ee-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="492ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="492ee-102">SYNOPSIS</span></span>
<span data-ttu-id="492ee-103">키 자격 증명 모음 서비스에서 관리 하는 키에 대 한 지정 된 키 보관소에 기존 Azure 저장소 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="492ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="492ee-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="492ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="492ee-105">DESCRIPTION</span></span>
<span data-ttu-id="492ee-106">키 자격 증명 모음에서 관리 하도록 저장소 계정 키에 대 한 키 보관소를 사용 하 여 기존 Azure Storage 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="492ee-107">저장소 계정이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-107">The Storage Account must already exist.</span></span> <span data-ttu-id="492ee-108">저장소 키는 호출자에 게 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="492ee-109">키 보관소는 재생성 기간을 기준으로 활성 키를 자동으로 다시 생성 하 고 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="492ee-110">예제의</span><span class="sxs-lookup"><span data-stu-id="492ee-110">EXAMPLES</span></span>

### <span data-ttu-id="492ee-111">예제 1: 키 보관소를 사용 하 여 Azure Storage 계정을 설정 하 여 키를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzureRmStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzureRmADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzureRmRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzureRmADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

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

<span data-ttu-id="492ee-112">키 자격 증명 모음에서 키를 관리 하는 데 사용할 키 보관소를 사용 하 여 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="492ee-113">활성 키 집합은 ' key1 '입니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-113">The active key set is 'key1'.</span></span> <span data-ttu-id="492ee-114">이 키는 sas 토큰을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="492ee-115">키 자격 증명 모음이이 명령 시간에서 재생성 기간 후에 ' key2 ' 키를 다시 생성 하 고 활성 키로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="492ee-116">이 자동 다시 생성 프로세스는 ' key1 ' 및 ' key2 ' 사이에 계속 해 서 90 일간 간격이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="492ee-117">예제 2: 키 자격 증명 모음을 사용 하 여 키를 관리 하는 클래식 Azure Storage 계정 설정</span><span class="sxs-lookup"><span data-stu-id="492ee-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

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

<span data-ttu-id="492ee-118">키 자격 증명 모음에 키를 사용 하 여 해당 키를 관리 하는 기본 저장소 계정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="492ee-119">활성 키 집합은 ' 주 '입니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="492ee-120">이 키는 sas 토큰을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="492ee-121">키 자격 증명 모음이이 명령 시간에서 재생성 기간 후에 ' 보조 ' 키를 다시 생성 하 고 활성 키로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="492ee-122">이 자동 다시 생성 프로세스는 90 일 간격으로 ' 주 '와 ' 보조 ' 사이에 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="492ee-123">변수</span><span class="sxs-lookup"><span data-stu-id="492ee-123">PARAMETERS</span></span>

### <span data-ttu-id="492ee-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="492ee-124">-AccountName</span></span>
<span data-ttu-id="492ee-125">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="492ee-126">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="492ee-127">-계정 Resourceid</span><span class="sxs-lookup"><span data-stu-id="492ee-127">-AccountResourceId</span></span>
<span data-ttu-id="492ee-128">저장소 계정의 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-128">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="492ee-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="492ee-129">-ActiveKeyName</span></span>
<span data-ttu-id="492ee-130">Sas 토큰을 생성 하는 데 사용 해야 하는 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="492ee-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492ee-131">-DefaultProfile</span></span>
<span data-ttu-id="492ee-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="492ee-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="492ee-133">-Disable</span><span class="sxs-lookup"><span data-stu-id="492ee-133">-Disable</span></span>
<span data-ttu-id="492ee-134">Sas 토큰 생성을 위해 관리 저장소 계정의 키를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="492ee-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="492ee-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="492ee-136">자동으로 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-136">Auto regenerate key.</span></span> <span data-ttu-id="492ee-137">True 이면 관리 되는 저장소 계정의 비활성 키가 자동으로 다시 생성 되며 재생성 기간 후 새 활성 키가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="492ee-138">False 인 경우 관리 저장소 계정의 키가 자동으로 다시 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="492ee-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="492ee-139">-RegenerationPeriod</span></span>
<span data-ttu-id="492ee-140">재생성 기간.</span><span class="sxs-lookup"><span data-stu-id="492ee-140">Regeneration period.</span></span> <span data-ttu-id="492ee-141">자동 다시 생성 키를 사용 하는 경우이 값은 관리 저장소 계정의 비활성 keygets 재생성 되 고 새 활성 키가 되는 timespan을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="492ee-142">태그</span><span class="sxs-lookup"><span data-stu-id="492ee-142">-Tag</span></span>
<span data-ttu-id="492ee-143">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="492ee-144">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="492ee-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="492ee-145">-VaultName</span><span class="sxs-lookup"><span data-stu-id="492ee-145">-VaultName</span></span>
<span data-ttu-id="492ee-146">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="492ee-146">Vault name.</span></span>
<span data-ttu-id="492ee-147">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-147">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="492ee-148">-확인</span><span class="sxs-lookup"><span data-stu-id="492ee-148">-Confirm</span></span>
<span data-ttu-id="492ee-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="492ee-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="492ee-150">-WhatIf</span></span>
<span data-ttu-id="492ee-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="492ee-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="492ee-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492ee-153">CommonParameters</span></span>
<span data-ttu-id="492ee-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="492ee-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492ee-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="492ee-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492ee-156">입력</span><span class="sxs-lookup"><span data-stu-id="492ee-156">INPUTS</span></span>

### <span data-ttu-id="492ee-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="492ee-157">System.String</span></span>

### <span data-ttu-id="492ee-158">시스템 Null 허용 ' 1 [[System. Timespan.zero, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="492ee-158">System.Nullable\`1[[System.TimeSpan, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="492ee-159">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="492ee-159">System.Collections.Hashtable</span></span>

## <span data-ttu-id="492ee-160">출력</span><span class="sxs-lookup"><span data-stu-id="492ee-160">OUTPUTS</span></span>

### <span data-ttu-id="492ee-161">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="492ee-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="492ee-162">상속자</span><span class="sxs-lookup"><span data-stu-id="492ee-162">NOTES</span></span>

## <span data-ttu-id="492ee-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="492ee-163">RELATED LINKS</span></span>

[<span data-ttu-id="492ee-164">AzureRM 볼트</span><span class="sxs-lookup"><span data-stu-id="492ee-164">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)