---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 05166cbfad437858b85e189d75df9b8216db4fae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977632"
---
# <span data-ttu-id="7019d-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7019d-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="7019d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7019d-102">SYNOPSIS</span></span>
<span data-ttu-id="7019d-103">Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="7019d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7019d-104">SYNTAX</span></span>

### <span data-ttu-id="7019d-105">StorageEncryption(기본값)</span><span class="sxs-lookup"><span data-stu-id="7019d-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7019d-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7019d-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7019d-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7019d-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7019d-108">설명</span><span class="sxs-lookup"><span data-stu-id="7019d-108">DESCRIPTION</span></span>
<span data-ttu-id="7019d-109">**Set-AzStorageAccount** cmdlet은 Azure Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="7019d-110">이 cmdlet을 사용하여 계정 유형을 수정하거나, 고객 도메인을 업데이트하거나, Storage 계정에서 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="7019d-111">예제</span><span class="sxs-lookup"><span data-stu-id="7019d-111">EXAMPLES</span></span>

### <span data-ttu-id="7019d-112">예제 1: Storage 계정 유형 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="7019d-113">이 명령은 Storage 계정 형식을 Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="7019d-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="7019d-114">예제 2: Storage 계정에 대한 사용자 지정 도메인 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="7019d-115">이 명령은 Storage 계정에 대한 사용자 지정 도메인을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="7019d-116">예제 3: 액세스 계층 값 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="7019d-117">명령은 액세스 계층 값을 멋지게 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="7019d-118">예제 4: 사용자 지정 도메인 및 태그 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="7019d-119">명령은 Storage 계정에 대한 사용자 지정 도메인 및 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="7019d-120">예제 5: 암호화 KeySource를 Keyvault로 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="7019d-121">이 명령은 새로 만든 Keyvault를 사용하여 암호화 KeySource를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="7019d-122">예제 6: 암호화 키소스를 "Microsoft.Storage"로 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="7019d-123">이 명령은 암호화 KeySource를 "Microsoft.Storage"로 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="7019d-124">예제 7: JSON을 통해 Storage 계정의 NetworkRuleSet 속성 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="7019d-125">이 명령은 JSON을 사용하여 Storage 계정의 NetworkRuleSet 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="7019d-126">예제 8: Storage 계정에서 NetworkRuleSet 속성을 얻고 다른 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="7019d-127">이 첫 번째 명령은 Storage 계정에서 NetworkRuleSet 속성을 얻게 하여 두 번째 명령은 다른 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="7019d-128">예제 9: Kind "Storage" 또는 "BlobStorage"를 "StorageV2" kind Storage 계정으로 저장소 계정 업그레이드</span><span class="sxs-lookup"><span data-stu-id="7019d-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="7019d-129">명령은 Kind "Storage" 또는 "BlobStorage"를 사용하여 Storage 계정을 "StorageV2" kind Storage 계정으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="7019d-130">예제 10: Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="7019d-131">명령은 Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="7019d-132">예제 11: Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정 업데이트 및 파일 ID 기반 인증 설정을 보여 주어</span><span class="sxs-lookup"><span data-stu-id="7019d-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="7019d-133">명령은 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="7019d-134">예제 12: MinimumTlsVersion, AllowBlobPublicAccess 및 AllowSharedKeyAccesss 설정</span><span class="sxs-lookup"><span data-stu-id="7019d-134">Example 12: Set MinimumTlsVersion, AllowBlobPublicAccess and AllowSharedKeyAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $true

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
True
```

<span data-ttu-id="7019d-135">명령은 MinimumTlsVersion, AllowBlobPublicAccess 및 AllowSharedKeyAccess를 설정한 다음 계정의 3개 속성을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-135">The command sets MinimumTlsVersion, AllowBlobPublicAccess and AllowSharedKeyAccess, and then show the the 3 properties of the account</span></span> 

### <span data-ttu-id="7019d-136">예제 13: RoutingPreference 설정으로 Storage 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="7019d-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="7019d-137">이 명령은 RoutingPreference 설정으로 Storage 계정을 업데이트합니다. PublishMicrosoftEndpoint를 false로, PublishInternetEndpoint를 true로, 그리고 RoutingChoice를 MicrosoftRouting으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="7019d-138">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7019d-138">PARAMETERS</span></span>

### <span data-ttu-id="7019d-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="7019d-139">-AccessTier</span></span>
<span data-ttu-id="7019d-140">이 cmdlet이 수정하는 Storage 계정의 액세스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="7019d-141">이 매개 변수에 대해 허용되는 값은 핫 및 쿨입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="7019d-142">액세스 계층을 변경하면 추가 요금이 부과될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="7019d-143">자세한 내용은 Azure Blob Storage: 핫 및 [쿨 저장소 계층을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="7019d-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="7019d-144">Storage 계정에 Kind as StorageV2 또는 BlobStorage가 있는 경우 *AccessTier* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="7019d-145">Storage 계정에 Kind as Storage가 있는 경우 *AccessTier 매개 변수를 지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="7019d-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="7019d-147">Azure Storage에 대한 SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="7019d-148">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="7019d-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="7019d-150">도메인 GUID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-150">Specifies the domain GUID.</span></span> <span data-ttu-id="7019d-151">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="7019d-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="7019d-153">AD DNS 서버가 권한이 있는 기본 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="7019d-154">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="7019d-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="7019d-156">SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="7019d-157">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="7019d-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="7019d-159">얻을 Active Directory 포리스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="7019d-160">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-161">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="7019d-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="7019d-162">NetBIOS 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="7019d-163">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-164">-AllowBlobPublicAccesss</span><span class="sxs-lookup"><span data-stu-id="7019d-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="7019d-165">저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용하거나 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-166">-AllowSharedKeyAccesss</span><span class="sxs-lookup"><span data-stu-id="7019d-166">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="7019d-167">저장소 계정이 공유 키를 통해 계정 액세스 키로 권한을 부여하는 요청을 허용하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-167">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="7019d-168">false인 경우 공유 액세스 서명을 포함한 모든 요청은 Azure AD(Azure Active Directory)를 사용하여 권한을 부여해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-168">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="7019d-169">기본값은 true와 동일한 null입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-169">The default value is null, which is equivalent to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-170">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7019d-170">-AsJob</span></span>
<span data-ttu-id="7019d-171">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7019d-171">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7019d-172">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7019d-172">-AssignIdentity</span></span>
<span data-ttu-id="7019d-173">Azure KeyVault와 같은 주요 관리 서비스와 함께 사용하기 위해 이 Storage 계정에 대한 새 Storage 계정 ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-173">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7019d-174">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7019d-174">-CustomDomainName</span></span>
<span data-ttu-id="7019d-175">사용자 지정 도메인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-175">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7019d-176">-DefaultProfile</span></span>
<span data-ttu-id="7019d-177">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-177">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7019d-178">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7019d-178">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7019d-179">저장소 계정에 대해 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-179">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-180">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7019d-180">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7019d-181">저장소 계정에 대해 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-181">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-182">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="7019d-182">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="7019d-183">Storage 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-183">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-184">-enableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="7019d-184">-EnableLargeFileShare</span></span>
<span data-ttu-id="7019d-185">저장소 계정이 TiB 용량이 5개 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-185">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="7019d-186">계정을 사용하도록 설정하면 기능을 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-186">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="7019d-187">현재 LRS 및 ZRS 복제 유형에만 지원됩니다. 따라서 지역 중복 계정으로 계정 변환은 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-187">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="7019d-188">자세히 알아보기 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="7019d-188">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="7019d-189">-Force</span><span class="sxs-lookup"><span data-stu-id="7019d-189">-Force</span></span>
<span data-ttu-id="7019d-190">변경을 저장소 계정에 작성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-190">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="7019d-191">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7019d-191">-KeyName</span></span>
<span data-ttu-id="7019d-192">-KeyvaultEncryption을 사용하여 Key Vault에서 암호화를 사용하도록 설정하는 경우 이 옵션을 사용하여 Keyname 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-192">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-193">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7019d-193">-KeyvaultEncryption</span></span>
<span data-ttu-id="7019d-194">Storage Service 암호화를 사용할 때 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-194">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="7019d-195">KeyName, KeyVersion 및 KeyVaultUri가 모두 설정된 경우 KeySource는 이 매개 변수가 설정되어 있는지 여부에 따라 Microsoft.Keyvault로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-195">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-196">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7019d-196">-KeyVaultUri</span></span>
<span data-ttu-id="7019d-197">-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 Key Vault에 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-197">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-198">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="7019d-198">-KeyVersion</span></span>
<span data-ttu-id="7019d-199">-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 키 버전에 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-199">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-200">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7019d-200">-MinimumTlsVersion</span></span>
<span data-ttu-id="7019d-201">저장소에 대한 요청에 허용되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-201">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-202">-Name</span><span class="sxs-lookup"><span data-stu-id="7019d-202">-Name</span></span>
<span data-ttu-id="7019d-203">수정할 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-203">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-204">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7019d-204">-NetworkRuleSet</span></span>
<span data-ttu-id="7019d-205">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-205">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-206">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="7019d-206">-PublishInternetEndpoint</span></span>
<span data-ttu-id="7019d-207">인터넷 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-207">Indicates whether internet  routing storage endpoints are to be published</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-208">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="7019d-208">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="7019d-209">Microsoft 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-209">Indicates whether microsoft routing storage endpoints are to be published</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-210">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7019d-210">-ResourceGroupName</span></span>
<span data-ttu-id="7019d-211">Storage 계정을 수정할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-211">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="7019d-212">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="7019d-212">-RoutingChoice</span></span>
<span data-ttu-id="7019d-213">라우팅 선택은 사용자가 선택한 네트워크 라우팅의 종류를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-213">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="7019d-214">가능한 값에는 'MicrosoftRouting', 'InternetRouting'이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-214">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-215">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7019d-215">-SkuName</span></span>
<span data-ttu-id="7019d-216">Storage 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-216">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="7019d-217">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-217">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7019d-218">Standard_LRS - 로컬 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-218">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="7019d-219">Standard_ZRS - 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="7019d-219">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="7019d-220">Standard_GRS - 지역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-220">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="7019d-221">Standard_RAGRS - 액세스 지역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-221">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="7019d-222">Premium_LRS - Premium 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="7019d-222">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="7019d-223">Standard_GZRS - 지역 중복 영역-중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="7019d-223">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="7019d-224">Standard_RAGZRS - 액세스 지역 중복 영역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-224">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="7019d-225">다른 계정 유형으로 Standard_ZRS Premium_LRS 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-225">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="7019d-226">다른 계정 형식을 Standard_ZRS 변경할 수 Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="7019d-226">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-227">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="7019d-227">-StorageEncryption</span></span>
<span data-ttu-id="7019d-228">Microsoft 관리 키를 사용할 저장소 계정 암호화를 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-228">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-229">-Tag</span><span class="sxs-lookup"><span data-stu-id="7019d-229">-Tag</span></span>
<span data-ttu-id="7019d-230">서버의 태그로 설정된 해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-230">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="7019d-231">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7019d-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7019d-232">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="7019d-232">-UpgradeToStorageV2</span></span>
<span data-ttu-id="7019d-233">Storage 또는 BlobStorage에서 StorageV2로 Storage 계정 종류를 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-233">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="7019d-234">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="7019d-234">-UseSubDomain</span></span>
<span data-ttu-id="7019d-235">간접 CName 유효성 검사를 사용하도록 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-235">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-236">-확인</span><span class="sxs-lookup"><span data-stu-id="7019d-236">-Confirm</span></span>
<span data-ttu-id="7019d-237">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-237">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-238">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7019d-238">-WhatIf</span></span>
<span data-ttu-id="7019d-239">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-239">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7019d-240">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-240">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7019d-241">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7019d-241">CommonParameters</span></span>
<span data-ttu-id="7019d-242">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7019d-242">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7019d-243">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7019d-243">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7019d-244">입력</span><span class="sxs-lookup"><span data-stu-id="7019d-244">INPUTS</span></span>

### <span data-ttu-id="7019d-245">System.String</span><span class="sxs-lookup"><span data-stu-id="7019d-245">System.String</span></span>

### <span data-ttu-id="7019d-246">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7019d-246">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7019d-247">출력</span><span class="sxs-lookup"><span data-stu-id="7019d-247">OUTPUTS</span></span>

### <span data-ttu-id="7019d-248">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7019d-248">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7019d-249">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7019d-249">NOTES</span></span>

## <span data-ttu-id="7019d-250">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7019d-250">RELATED LINKS</span></span>

[<span data-ttu-id="7019d-251">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7019d-251">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="7019d-252">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7019d-252">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="7019d-253">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7019d-253">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
