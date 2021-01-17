---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348321"
---
# <span data-ttu-id="7b840-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b840-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="7b840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b840-102">SYNOPSIS</span></span>
<span data-ttu-id="7b840-103">Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="7b840-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b840-104">SYNTAX</span></span>

### <span data-ttu-id="7b840-105">StorageEncryption(기본값)</span><span class="sxs-lookup"><span data-stu-id="7b840-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b840-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7b840-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b840-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7b840-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b840-108">설명</span><span class="sxs-lookup"><span data-stu-id="7b840-108">DESCRIPTION</span></span>
<span data-ttu-id="7b840-109">**Set-AzStorageAccount** cmdlet은 Azure Storage 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="7b840-110">이 cmdlet을 사용하여 계정 유형을 수정하거나, 고객 도메인을 업데이트하거나, Storage 계정에 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="7b840-111">예제</span><span class="sxs-lookup"><span data-stu-id="7b840-111">EXAMPLES</span></span>

### <span data-ttu-id="7b840-112">예제 1: Storage 계정 유형 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="7b840-113">이 명령은 Storage 계정 유형을 저장소 계정 유형으로 Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="7b840-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="7b840-114">예제 2: Storage 계정에 대한 사용자 지정 도메인 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="7b840-115">이 명령은 Storage 계정에 대한 사용자 지정 도메인을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="7b840-116">예제 3: 액세스 계층 값 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="7b840-117">이 명령은 액세스 계층 값을 쿨로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="7b840-118">예제 4: 사용자 지정 도메인 및 태그 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="7b840-119">이 명령은 Storage 계정에 대한 사용자 지정 도메인 및 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="7b840-120">예제 5: 암호화 KeySource를 Keyvault로 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="7b840-121">이 명령은 새로 만든 Keyvault로 암호화 KeySource를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="7b840-122">예제 6: 암호화 KeySource를 "Microsoft.Storage"로 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="7b840-123">이 명령은 암호화 KeySource를 "Microsoft.Storage"로 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="7b840-124">예제 7: JSON을 통해 Storage 계정의 NetworkRuleSet 속성 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="7b840-125">이 명령은 JSON을 사용하여 Storage 계정의 NetworkRuleSet 속성을 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="7b840-126">예제 8: Storage 계정에서 NetworkRuleSet 속성을 액세스하고 다른 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="7b840-127">이 첫 번째 명령은 Storage 계정에서 NetworkRuleSet 속성을, 두 번째 명령은 다른 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="7b840-128">예제 9: 종류가 "Storage" 또는 "BlobStorage"인 Storage 계정을 "StorageV2" 종류의 Storage 계정으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="7b840-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="7b840-129">이 명령은 종류가 "Storage" 또는 "BlobStorage"인 Storage 계정을 "StorageV2" 종류의 Storage 계정으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="7b840-130">예제 10: Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="7b840-131">이 명령은 Azure Files AAD DS 인증을 사용하도록 설정하여 Storage 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="7b840-132">예제 11: Files Active Directory Domain Service 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 표시</span><span class="sxs-lookup"><span data-stu-id="7b840-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="7b840-133">이 명령은 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정을 업데이트한 다음 파일 ID 기반 인증 설정을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="7b840-134">예제 12: MinimumTlsVersion 및 AllowBlobPublicAccess 설정</span><span class="sxs-lookup"><span data-stu-id="7b840-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="7b840-135">이 명령은 MinimumTlsVersion 및 AllowBlobPublicAccess를 설정한 다음 계정의 2개 속성을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="7b840-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="7b840-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b840-136">PARAMETERS</span></span>

### <span data-ttu-id="7b840-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="7b840-137">-AccessTier</span></span>
<span data-ttu-id="7b840-138">이 cmdlet이 수정하는 Storage 계정의 액세스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="7b840-139">이 매개 변수에 허용되는 값은 핫 및 쿨입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="7b840-140">액세스 계층을 변경하면 추가 요금이 부과될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="7b840-141">자세한 내용은 Azure Blob Storage: 핫 및 쿨 [스토리지 계층을 참조하세요.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="7b840-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="7b840-142">Storage 계정에 Kind as StorageV2 또는 BlobStorage가 있는 경우 *AccessTier* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="7b840-143">Storage 계정에 Kind as Storage가 있는 경우 *AccessTier* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="7b840-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="7b840-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="7b840-145">Azure Storage에 대한 SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="7b840-146">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="7b840-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="7b840-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="7b840-148">도메인 GUID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-148">Specifies the domain GUID.</span></span> <span data-ttu-id="7b840-149">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="7b840-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="7b840-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="7b840-151">AD DNS 서버가 권한이 있는 주 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="7b840-152">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="7b840-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="7b840-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="7b840-154">SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="7b840-155">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="7b840-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="7b840-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="7b840-157">얻을 Active Directory 포리스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="7b840-158">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="7b840-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="7b840-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="7b840-160">NetBIOS 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="7b840-161">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="7b840-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="7b840-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="7b840-163">저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용하거나 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="7b840-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b840-164">-AsJob</span></span>
<span data-ttu-id="7b840-165">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7b840-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b840-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7b840-166">-AssignIdentity</span></span>
<span data-ttu-id="7b840-167">Azure KeyVault와 같은 키 관리 서비스에서 사용할 새 Storage 계정 ID를 생성하고 이 Storage 계정에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7b840-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7b840-168">-CustomDomainName</span></span>
<span data-ttu-id="7b840-169">사용자 지정 도메인의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="7b840-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b840-170">-DefaultProfile</span></span>
<span data-ttu-id="7b840-171">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b840-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7b840-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7b840-173">저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="7b840-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7b840-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7b840-175">저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="7b840-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="7b840-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="7b840-177">Storage 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="7b840-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="7b840-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="7b840-179">저장소 계정이 용량이 5 TiB 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="7b840-180">계정이 활성화되면 기능을 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="7b840-181">현재 LRS 및 ZRS 복제 유형에서만 지원됩니다. 따라서 계정은 지역 중복 계정으로 변환할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="7b840-182">자세한 내용은 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="7b840-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="7b840-183">-Force</span><span class="sxs-lookup"><span data-stu-id="7b840-183">-Force</span></span>
<span data-ttu-id="7b840-184">변경을 저장소 계정에 강제로 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="7b840-185">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7b840-185">-KeyName</span></span>
<span data-ttu-id="7b840-186">-KeyvaultEncryption을 사용하여 Key Vault에서 암호화를 사용하도록 설정하는 경우 이 옵션을 사용하여 Keyname 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="7b840-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7b840-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="7b840-188">Storage 서비스 암호화를 사용할 때 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="7b840-189">KeyName, KeyVersion 및 KeyVaultUri가 모두 설정된 경우 KeySource는 이 매개 변수가 설정되어 있는지 여부에 따라 Microsoft.Keyvault로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="7b840-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7b840-190">-KeyVaultUri</span></span>
<span data-ttu-id="7b840-191">-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 Key Vault에 대한 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="7b840-192">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="7b840-192">-KeyVersion</span></span>
<span data-ttu-id="7b840-193">-KeyvaultEncryption 매개 변수를 지정하여 Key Vault 암호화를 사용하는 경우 이 옵션을 사용하여 키 버전에 대한 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="7b840-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7b840-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="7b840-195">저장소에 대한 요청에 허용되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-195">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="7b840-196">-Name</span><span class="sxs-lookup"><span data-stu-id="7b840-196">-Name</span></span>
<span data-ttu-id="7b840-197">수정할 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-197">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="7b840-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b840-198">-NetworkRuleSet</span></span>
<span data-ttu-id="7b840-199">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고, 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="7b840-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b840-200">-ResourceGroupName</span></span>
<span data-ttu-id="7b840-201">Storage 계정을 수정할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="7b840-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7b840-202">-SkuName</span></span>
<span data-ttu-id="7b840-203">Storage 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="7b840-204">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="7b840-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7b840-205">Standard_LRS - 로컬 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="7b840-206">Standard_ZRS - 영역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="7b840-207">Standard_GRS - 지역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="7b840-208">Standard_RAGRS - 읽기 액세스 지역 중복 저장소</span><span class="sxs-lookup"><span data-stu-id="7b840-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="7b840-209">Premium_LRS - 프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="7b840-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="7b840-210">Standard_GZRS - 지역 중복 영역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="7b840-211">Standard_RAGZRS - 읽기 액세스 지역 중복 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="7b840-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="7b840-212">다른 계정 유형으로 Standard_ZRS Premium_LRS 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="7b840-213">다른 계정 유형을 다른 계정 유형으로 변경하거나 Standard_ZRS 변경할 Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="7b840-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="7b840-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="7b840-214">-StorageEncryption</span></span>
<span data-ttu-id="7b840-215">Microsoft 관리 키를 사용하기 위해 Storage 계정 암호화를 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="7b840-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b840-216">-Tag</span></span>
<span data-ttu-id="7b840-217">서버의 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="7b840-218">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7b840-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7b840-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="7b840-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="7b840-220">Storage 계정 종류를 Storage 또는 BlobStorage에서 StorageV2로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="7b840-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="7b840-221">-UseSubDomain</span></span>
<span data-ttu-id="7b840-222">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="7b840-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b840-223">-Confirm</span></span>
<span data-ttu-id="7b840-224">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b840-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b840-225">-WhatIf</span></span>
<span data-ttu-id="7b840-226">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7b840-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b840-227">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b840-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b840-228">CommonParameters</span></span>
<span data-ttu-id="7b840-229">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b840-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b840-230">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b840-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b840-231">입력</span><span class="sxs-lookup"><span data-stu-id="7b840-231">INPUTS</span></span>

### <span data-ttu-id="7b840-232">System.String</span><span class="sxs-lookup"><span data-stu-id="7b840-232">System.String</span></span>

### <span data-ttu-id="7b840-233">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7b840-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7b840-234">출력</span><span class="sxs-lookup"><span data-stu-id="7b840-234">OUTPUTS</span></span>

### <span data-ttu-id="7b840-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b840-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7b840-236">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b840-236">NOTES</span></span>

## <span data-ttu-id="7b840-237">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b840-237">RELATED LINKS</span></span>

[<span data-ttu-id="7b840-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b840-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="7b840-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b840-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="7b840-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b840-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
