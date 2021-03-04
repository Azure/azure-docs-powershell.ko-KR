---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993202"
---
# <span data-ttu-id="11985-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11985-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="11985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11985-102">SYNOPSIS</span></span>
<span data-ttu-id="11985-103">Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-103">Creates a Storage account.</span></span>

## <span data-ttu-id="11985-104">구문</span><span class="sxs-lookup"><span data-stu-id="11985-104">SYNTAX</span></span>

### <span data-ttu-id="11985-105">AzureActiveDirectoryDomainServicesForFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="11985-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="11985-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="11985-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="11985-107">설명</span><span class="sxs-lookup"><span data-stu-id="11985-107">DESCRIPTION</span></span>
<span data-ttu-id="11985-108">**New-AzStorageAccount** cmdlet은 Azure Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="11985-109">예제</span><span class="sxs-lookup"><span data-stu-id="11985-109">EXAMPLES</span></span>

### <span data-ttu-id="11985-110">예제 1: Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="11985-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="11985-111">이 명령은 리소스 그룹 이름 MyResourceGroup에 대한 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="11985-112">예제 2: BlobStorage Kind 및 hot AccessTier를 사용하여 Blob Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="11985-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="11985-113">이 명령은 BlobStorage Kind 및 hot AccessTier를 사용하여 Blob Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="11985-114">예제 3: Kind StorageV2를 사용하여 Storage 계정을 만들고 Azure KeyVault에 대한 ID 생성 및 할당</span><span class="sxs-lookup"><span data-stu-id="11985-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="11985-115">이 명령은 Kind StorageV2를 사용하여 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="11985-116">또한 Azure KeyVault를 통해 계정 키를 관리하는 데 사용할 수 있는 ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="11985-117">예제 4: JSON에서 NetworkRuleSet을 사용하여 Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="11985-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="11985-118">이 명령은 JSON에서 NetworkRuleSet 속성이 있는 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="11985-119">예제 5: 계층적 네임스페이스를 사용하도록 설정한 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="11985-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="11985-120">이 명령은 계층적 네임스페이스를 사용하도록 설정한 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="11985-121">예제 6: Azure Files AAD DS 인증을 사용하여 Storage 계정을 만들고 대용량 파일 공유를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="11985-122">이 명령은 Azure Files AAD DS 인증을 사용하여 Storage 계정을 만들고 대용량 파일 공유를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="11985-123">예제 7: Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="11985-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="11985-124">이 명령은 사용 가능한 Files Active Directory 도메인 서비스 인증이 있는 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="11985-125">예제 8: 큐 및 Table Service를 사용하여 Storage 계정을 만들고 계정 범위 암호화 키를 사용하며 인프라 암호화가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="11985-126">이 명령은 큐 및 Table Service에서 계정 범위 암호화 키 및 인프라 암호화 요구를 사용하여 Storage 계정을 만듭니다. 따라서 큐와 테이블은 Blob 및 File service와 동일한 암호화 키를 사용하며, 서비스는 미사용 데이터에 대해 플랫폼 관리 키로 보조 암호화 계층을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="11985-127">그런 다음 Storage 계정 속성을 얻게 하여 큐 및 테이블 서비스의 암호화 키 타이프 및 RequireInfrastructureEncryption 값을 를 본다.</span><span class="sxs-lookup"><span data-stu-id="11985-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="11985-128">예제 9: Account MinimumTlsVersion 및 AllowBlobPublicAccesss를 만들고 SharedKey Access를 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="11985-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="11985-129">명령은 MinimumTlsVersion, AllowBlobPublicAccess를 사용하여 계정을 만들고 계정에 대한 SharedKey 액세스를 사용하지 않도록 설정한 다음, 생성된 계정의 3개 속성을 보여 주며</span><span class="sxs-lookup"><span data-stu-id="11985-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="11985-130">예제 10: RoutingPreference 설정을 사용하여 Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="11985-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="11985-131">이 명령은 RoutingPreference 설정이 있는 Storage 계정을 만듭니다. PublishMicrosoftEndpoint 및 PublishInternetEndpoint는 true로, RoutingChoice를 MicrosoftRouting으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11985-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="11985-132">매개 변수</span><span class="sxs-lookup"><span data-stu-id="11985-132">PARAMETERS</span></span>

### <span data-ttu-id="11985-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="11985-133">-AccessTier</span></span>
<span data-ttu-id="11985-134">이 cmdlet이 만드는 Storage 계정의 액세스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="11985-135">이 매개 변수에 대해 허용되는 값은 핫 및 쿨입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="11985-136">Kind 매개 변수에 BlobStorage  값을 지정하는 경우 *AccessTier* 매개 변수에 대한 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="11985-137">이 Kind 매개 변수에 대한 Storage 값을 *지정하는* 경우 *AccessTier 매개 변수를 지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11985-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="11985-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="11985-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="11985-139">Azure Storage에 대한 SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="11985-140">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="11985-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="11985-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="11985-142">도메인 GUID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-142">Specifies the domain GUID.</span></span> <span data-ttu-id="11985-143">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="11985-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="11985-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="11985-145">AD DNS 서버가 권한이 있는 기본 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="11985-146">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="11985-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="11985-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="11985-148">SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="11985-149">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="11985-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="11985-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="11985-151">얻을 Active Directory 포리스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="11985-152">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="11985-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="11985-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="11985-154">NetBIOS 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="11985-155">-EnableActiveDirectoryDomainServicesForFile이 true로 설정될 때 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="11985-156">-AllowBlobPublicAccesss</span><span class="sxs-lookup"><span data-stu-id="11985-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="11985-157">저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="11985-158">이 속성에 대한 기본 해석은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="11985-159">-AllowSharedKeyAccesss</span><span class="sxs-lookup"><span data-stu-id="11985-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="11985-160">저장소 계정이 공유 키를 통해 계정 액세스 키로 권한을 부여하는 요청을 허용하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="11985-161">false인 경우 공유 액세스 서명을 포함한 모든 요청은 Azure AD(Azure Active Directory)를 사용하여 권한을 부여해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="11985-162">기본값은 true와 동일한 null입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-162">The default value is null, which is equivalent to true.</span></span>

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

### <span data-ttu-id="11985-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11985-163">-AsJob</span></span>
<span data-ttu-id="11985-164">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="11985-164">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11985-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="11985-165">-AssignIdentity</span></span>
<span data-ttu-id="11985-166">Azure KeyVault와 같은 주요 관리 서비스와 함께 사용하기 위해 이 Storage 계정에 대한 새 Storage 계정 ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="11985-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="11985-167">-CustomDomainName</span></span>
<span data-ttu-id="11985-168">Storage 계정의 사용자 지정 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="11985-169">기본값은 Storage입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-169">The default value is Storage.</span></span>

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

### <span data-ttu-id="11985-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11985-170">-DefaultProfile</span></span>
<span data-ttu-id="11985-171">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11985-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="11985-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="11985-173">저장소 계정에 대해 Azure Files Active Directory 도메인 서비스 인증을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11985-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="11985-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="11985-175">저장소 계정에 대해 Azure Files Azure Active Directory 도메인 서비스 인증을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11985-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="11985-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="11985-177">저장소 계정이 계층적 네임스페이스를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="11985-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="11985-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="11985-179">Storage 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="11985-180">-enableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="11985-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="11985-181">저장소 계정이 TiB 용량이 5개 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="11985-182">계정을 사용하도록 설정하면 기능을 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11985-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="11985-183">현재 LRS 및 ZRS 복제 유형에만 지원됩니다. 따라서 지역 중복 계정으로 계정 변환은 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="11985-184">자세히 알아보기 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="11985-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="11985-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="11985-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="11985-186">큐에 대한 암호화 키 타이프를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="11985-187">기본값은 Service입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-187">The default value is Service.</span></span>
<span data-ttu-id="11985-188">-Account: 큐는 계정 범위 암호화 키로 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="11985-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="11985-189">-Service: 큐는 항상 키로 Service-Managed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11985-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11985-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="11985-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="11985-191">표에 대한 암호화 키 타이프를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="11985-192">기본값은 Service입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-192">The default value is Service.</span></span>
- <span data-ttu-id="11985-193">계정: 테이블은 계정 범위 암호화 키로 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="11985-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="11985-194">서비스: 테이블은 항상 키로 Service-Managed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11985-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11985-195">-Kind</span><span class="sxs-lookup"><span data-stu-id="11985-195">-Kind</span></span>
<span data-ttu-id="11985-196">이 cmdlet에서 만드는 저장소 계정의 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="11985-197">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11985-198">저장소.</span><span class="sxs-lookup"><span data-stu-id="11985-198">Storage.</span></span> <span data-ttu-id="11985-199">Blob, 테이블, 큐, 파일 및 디스크의 저장소를 지원하는 일반적 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="11985-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="11985-200">StorageV2.</span></span> <span data-ttu-id="11985-201">데이터 계층화와 같은 고급 기능을 사용하여 Blob, 테이블, 큐, 파일 및 디스크를 지원하는 일반 용도 버전 2(GPv2) Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="11985-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="11985-202">BlobStorage.</span></span> <span data-ttu-id="11985-203">Blob의 저장소만 지원하는 Blob Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="11985-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="11985-204">BlockBlobStorage.</span></span> <span data-ttu-id="11985-205">블록 Blob의 저장소만 지원하는 블록 Blob Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="11985-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="11985-206">FileStorage.</span></span> <span data-ttu-id="11985-207">파일 저장소만 지원하는 파일 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="11985-208">기본값은 StorageV2입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-208">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11985-209">-Location</span><span class="sxs-lookup"><span data-stu-id="11985-209">-Location</span></span>
<span data-ttu-id="11985-210">만들 저장소 계정의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-210">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="11985-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="11985-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="11985-212">저장소에 대한 요청에 허용되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="11985-213">기본 해석은 이 속성에 대한 TLS 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-213">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="11985-214">-Name</span><span class="sxs-lookup"><span data-stu-id="11985-214">-Name</span></span>
<span data-ttu-id="11985-215">만들 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-215">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="11985-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11985-216">-NetworkRuleSet</span></span>
<span data-ttu-id="11985-217">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="11985-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="11985-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="11985-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="11985-219">인터넷 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="11985-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="11985-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="11985-221">Microsoft 라우팅 저장소 엔드포인트를 게시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="11985-222">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="11985-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="11985-223">서비스는 미사용 데이터에 대한 플랫폼 관리 키가 있는 보조 암호화 계층을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="11985-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11985-224">-ResourceGroupName</span></span>
<span data-ttu-id="11985-225">Storage 계정을 추가할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="11985-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="11985-226">-RoutingChoice</span></span>
<span data-ttu-id="11985-227">라우팅 선택은 사용자가 선택한 네트워크 라우팅의 종류를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="11985-228">가능한 값에는 'MicrosoftRouting', 'InternetRouting'이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="11985-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="11985-229">-SkuName</span><span class="sxs-lookup"><span data-stu-id="11985-229">-SkuName</span></span>
<span data-ttu-id="11985-230">이 cmdlet이 만드는 Storage 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="11985-231">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11985-232">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="11985-232">Standard_LRS.</span></span> <span data-ttu-id="11985-233">로컬 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="11985-234">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="11985-234">Standard_ZRS.</span></span> <span data-ttu-id="11985-235">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="11985-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="11985-236">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="11985-236">Standard_GRS.</span></span> <span data-ttu-id="11985-237">지역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="11985-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="11985-238">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="11985-238">Standard_RAGRS.</span></span> <span data-ttu-id="11985-239">액세스 지역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="11985-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="11985-240">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="11985-240">Premium_LRS.</span></span> <span data-ttu-id="11985-241">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="11985-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="11985-242">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="11985-242">Premium_ZRS.</span></span> <span data-ttu-id="11985-243">프리미엄 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="11985-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="11985-244">Standard_GZRS - 지역 중복 영역-중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="11985-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="11985-245">Standard_RAGZRS - 액세스 지역 중복 영역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="11985-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11985-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="11985-246">-Tag</span></span>
<span data-ttu-id="11985-247">서버의 태그로 설정된 해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="11985-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="11985-248">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="11985-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11985-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="11985-249">-UseSubDomain</span></span>
<span data-ttu-id="11985-250">간접 CName 유효성 검사를 사용하도록 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11985-250">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="11985-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11985-251">CommonParameters</span></span>
<span data-ttu-id="11985-252">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11985-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11985-253">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="11985-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11985-254">입력</span><span class="sxs-lookup"><span data-stu-id="11985-254">INPUTS</span></span>

### <span data-ttu-id="11985-255">System.String</span><span class="sxs-lookup"><span data-stu-id="11985-255">System.String</span></span>

## <span data-ttu-id="11985-256">출력</span><span class="sxs-lookup"><span data-stu-id="11985-256">OUTPUTS</span></span>

### <span data-ttu-id="11985-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11985-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="11985-258">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11985-258">NOTES</span></span>

## <span data-ttu-id="11985-259">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11985-259">RELATED LINKS</span></span>

[<span data-ttu-id="11985-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11985-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="11985-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11985-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="11985-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11985-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
