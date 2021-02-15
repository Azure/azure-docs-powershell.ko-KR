---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183172"
---
# <span data-ttu-id="a7471-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7471-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="a7471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7471-102">SYNOPSIS</span></span>
<span data-ttu-id="a7471-103">Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="a7471-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7471-104">SYNTAX</span></span>

### <span data-ttu-id="a7471-105">StorageEncryption(기본값)</span><span class="sxs-lookup"><span data-stu-id="a7471-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7471-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a7471-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7471-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="a7471-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7471-108">설명</span><span class="sxs-lookup"><span data-stu-id="a7471-108">DESCRIPTION</span></span>
<span data-ttu-id="a7471-109">**Set-AzStorageAccount** cmdlet은 Azure Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="a7471-110">이 cmdlet을 사용하여 계정 유형을 수정하거나, 고객 도메인을 업데이트하거나, Storage 계정에 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="a7471-111">예제</span><span class="sxs-lookup"><span data-stu-id="a7471-111">EXAMPLES</span></span>

### <span data-ttu-id="a7471-112">예제 1: Storage 계정 유형 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="a7471-113">이 명령은 Storage 계정 유형을 저장소 계정 유형으로 Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="a7471-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="a7471-114">예제 2: Storage 계정에 대한 사용자 지정 도메인 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="a7471-115">이 명령은 Storage 계정에 대한 사용자 지정 도메인을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="a7471-116">예제 3: 액세스 계층 값 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="a7471-117">이 명령은 액세스 계층 값을 쿨로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="a7471-118">예제 4: 사용자 지정 도메인 및 태그 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="a7471-119">이 명령은 Storage 계정에 대한 사용자 지정 도메인 및 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="a7471-120">예제 5: 암호화 KeySource를 Keyvault로 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="a7471-121">이 명령은 새로 만든 Keyvault로 암호화 KeySource를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="a7471-122">예제 6: 암호화 KeySource를 "Microsoft.Storage"로 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="a7471-123">이 명령은 암호화 KeySource를 "Microsoft.Storage"로 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="a7471-124">예제 7: JSON을 통해 Storage 계정의 NetworkRuleSet 속성 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="a7471-125">이 명령은 JSON을 사용하여 Storage 계정의 NetworkRuleSet 속성을 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="a7471-126">예제 8: Storage 계정에서 NetworkRuleSet 속성을 액세스하고 다른 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="a7471-127">이 첫 번째 명령은 Storage 계정에서 NetworkRuleSet 속성을, 두 번째 명령은 다른 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="a7471-128">예제 9: 종류가 "Storage" 또는 "BlobStorage"인 Storage 계정을 "StorageV2" 종류의 Storage 계정으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="a7471-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="a7471-129">이 명령은 종류가 "Storage" 또는 "BlobStorage"인 Storage 계정을 "StorageV2" 종류의 Storage 계정으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="a7471-130">예제 10: Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="a7471-131">이 명령은 Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="a7471-132">예제 11: Files Active Directory Domain Service 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 표시</span><span class="sxs-lookup"><span data-stu-id="a7471-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="a7471-133">이 명령은 Azure Files Active Directory Domain Service 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="a7471-134">예제 12: MinimumTlsVersion 및 AllowBlobPublicAccess 설정</span><span class="sxs-lookup"><span data-stu-id="a7471-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="a7471-135">이 명령은 MinimumTlsVersion 및 AllowBlobPublicAccess를 설정한 다음 계정의 2개 속성을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="a7471-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

### <span data-ttu-id="a7471-136">예제 13: RoutingPreference 설정을 사용하여 Storage 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="a7471-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
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

<span data-ttu-id="a7471-137">이 명령은 RoutingPreference 설정으로 Storage 계정을 업데이트합니다. PublishMicrosoftEndpoint를 false로, PublishInternetEndpoint를 true로, MicrosoftRouting으로 RoutingChoice를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="a7471-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7471-138">PARAMETERS</span></span>

### <span data-ttu-id="a7471-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="a7471-139">-AccessTier</span></span>
<span data-ttu-id="a7471-140">이 cmdlet이 수정하는 Storage 계정의 액세스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="a7471-141">이 매개 변수에 허용되는 값은 핫 및 쿨입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="a7471-142">액세스 계층을 변경하면 추가 요금이 부과될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="a7471-143">자세한 내용은 Azure Blob Storage: 핫 및 쿨 [스토리지 계층을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="a7471-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="a7471-144">Storage 계정에 Kind as StorageV2 또는 BlobStorage가 있는 경우 *AccessTier* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="a7471-145">Storage 계정에 Kind as Storage가 있는 경우 *AccessTier* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="a7471-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="a7471-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="a7471-147">Azure Storage에 대한 SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="a7471-148">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a7471-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="a7471-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="a7471-150">도메인 GUID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-150">Specifies the domain GUID.</span></span> <span data-ttu-id="a7471-151">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a7471-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="a7471-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="a7471-153">AD DNS 서버가 권한이 있는 주 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="a7471-154">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a7471-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="a7471-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="a7471-156">SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="a7471-157">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a7471-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="a7471-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="a7471-159">얻을 Active Directory 포리스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="a7471-160">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a7471-161">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="a7471-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="a7471-162">NetBIOS 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="a7471-163">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a7471-164">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="a7471-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="a7471-165">저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용하거나 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="a7471-166">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7471-166">-AsJob</span></span>
<span data-ttu-id="a7471-167">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a7471-167">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7471-168">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a7471-168">-AssignIdentity</span></span>
<span data-ttu-id="a7471-169">Azure KeyVault와 같은 키 관리 서비스에서 사용할 새 Storage 계정 ID를 생성하고 이 Storage 계정에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-169">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a7471-170">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a7471-170">-CustomDomainName</span></span>
<span data-ttu-id="a7471-171">사용자 지정 도메인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-171">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="a7471-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7471-172">-DefaultProfile</span></span>
<span data-ttu-id="a7471-173">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7471-174">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="a7471-174">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="a7471-175">저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="a7471-176">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="a7471-176">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="a7471-177">저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-177">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="a7471-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="a7471-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="a7471-179">Storage 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="a7471-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="a7471-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="a7471-181">저장소 계정이 용량이 5 TiB 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="a7471-182">계정이 활성화되면 기능을 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="a7471-183">현재 LRS 및 ZRS 복제 유형에서만 지원됩니다. 따라서 계정은 지역 중복 계정으로 변환할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="a7471-184">자세한 내용은 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="a7471-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="a7471-185">-Force</span><span class="sxs-lookup"><span data-stu-id="a7471-185">-Force</span></span>
<span data-ttu-id="a7471-186">변경을 저장소 계정에 강제로 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-186">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="a7471-187">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a7471-187">-KeyName</span></span>
<span data-ttu-id="a7471-188">-KeyvaultEncryption을 사용하여 Key Vault에서 암호화를 사용하도록 설정하는 경우 이 옵션을 사용하여 Keyname 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-188">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="a7471-189">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a7471-189">-KeyvaultEncryption</span></span>
<span data-ttu-id="a7471-190">Storage 서비스 암호화를 사용할 때 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-190">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="a7471-191">KeyName, KeyVersion 및 KeyVaultUri가 모두 설정된 경우 KeySource는 이 매개 변수가 설정되어 있는지 여부에 따라 Microsoft.Keyvault로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-191">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="a7471-192">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a7471-192">-KeyVaultUri</span></span>
<span data-ttu-id="a7471-193">-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 Key Vault에 대한 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="a7471-194">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="a7471-194">-KeyVersion</span></span>
<span data-ttu-id="a7471-195">-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 키 버전에 대한 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-195">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="a7471-196">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a7471-196">-MinimumTlsVersion</span></span>
<span data-ttu-id="a7471-197">저장소에 대한 요청에 허용되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-197">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="a7471-198">-Name</span><span class="sxs-lookup"><span data-stu-id="a7471-198">-Name</span></span>
<span data-ttu-id="a7471-199">수정할 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-199">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="a7471-200">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7471-200">-NetworkRuleSet</span></span>
<span data-ttu-id="a7471-201">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고, 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-201">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="a7471-202">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7471-202">-PublishInternetEndpoint</span></span>
<span data-ttu-id="a7471-203">인터넷 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-203">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="a7471-204">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7471-204">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="a7471-205">Microsoft 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-205">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="a7471-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7471-206">-ResourceGroupName</span></span>
<span data-ttu-id="a7471-207">Storage 계정을 수정할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-207">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="a7471-208">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="a7471-208">-RoutingChoice</span></span>
<span data-ttu-id="a7471-209">라우팅 선택은 사용자가 선택한 네트워크 라우팅의 종류를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-209">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="a7471-210">가능한 값은 'MicrosoftRouting', 'InternetRouting'입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-210">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="a7471-211">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a7471-211">-SkuName</span></span>
<span data-ttu-id="a7471-212">Storage 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-212">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="a7471-213">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a7471-213">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a7471-214">Standard_LRS - 로컬 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-214">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="a7471-215">Standard_ZRS - 영역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-215">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="a7471-216">Standard_GRS - 지역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-216">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="a7471-217">Standard_RAGRS - 읽기 액세스 지역 중복 저장소</span><span class="sxs-lookup"><span data-stu-id="a7471-217">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="a7471-218">Premium_LRS - 프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="a7471-218">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="a7471-219">Standard_GZRS - 지역 중복 영역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-219">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="a7471-220">Standard_RAGZRS - 읽기 액세스 지역 중복 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="a7471-220">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="a7471-221">다른 계정 유형으로 Standard_ZRS Premium_LRS 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-221">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="a7471-222">다른 계정 유형을 다른 계정 유형으로 변경하거나 Standard_ZRS 변경할 Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="a7471-222">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="a7471-223">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="a7471-223">-StorageEncryption</span></span>
<span data-ttu-id="a7471-224">Microsoft 관리 키를 사용하기 위해 Storage 계정 암호화를 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-224">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="a7471-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7471-225">-Tag</span></span>
<span data-ttu-id="a7471-226">서버의 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-226">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="a7471-227">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a7471-227">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a7471-228">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="a7471-228">-UpgradeToStorageV2</span></span>
<span data-ttu-id="a7471-229">Storage 계정 종류를 Storage 또는 BlobStorage에서 StorageV2로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-229">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="a7471-230">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="a7471-230">-UseSubDomain</span></span>
<span data-ttu-id="a7471-231">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-231">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="a7471-232">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7471-232">-Confirm</span></span>
<span data-ttu-id="a7471-233">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-233">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7471-234">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7471-234">-WhatIf</span></span>
<span data-ttu-id="a7471-235">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a7471-235">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7471-236">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-236">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7471-237">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7471-237">CommonParameters</span></span>
<span data-ttu-id="a7471-238">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7471-238">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7471-239">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a7471-239">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7471-240">입력</span><span class="sxs-lookup"><span data-stu-id="a7471-240">INPUTS</span></span>

### <span data-ttu-id="a7471-241">System.String</span><span class="sxs-lookup"><span data-stu-id="a7471-241">System.String</span></span>

### <span data-ttu-id="a7471-242">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a7471-242">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a7471-243">출력</span><span class="sxs-lookup"><span data-stu-id="a7471-243">OUTPUTS</span></span>

### <span data-ttu-id="a7471-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7471-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a7471-245">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7471-245">NOTES</span></span>

## <span data-ttu-id="a7471-246">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7471-246">RELATED LINKS</span></span>

[<span data-ttu-id="a7471-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7471-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="a7471-248">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7471-248">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="a7471-249">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7471-249">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
