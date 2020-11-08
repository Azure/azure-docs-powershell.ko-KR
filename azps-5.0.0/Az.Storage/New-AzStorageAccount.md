---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217189"
---
# <span data-ttu-id="fcdc2-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdc2-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="fcdc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcdc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdc2-103">저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-103">Creates a Storage account.</span></span>

## <span data-ttu-id="fcdc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcdc2-104">SYNTAX</span></span>

### <span data-ttu-id="fcdc2-105">AzureActiveDirectoryDomainServicesForFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcdc2-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcdc2-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="fcdc2-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcdc2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcdc2-107">DESCRIPTION</span></span>
<span data-ttu-id="fcdc2-108">**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="fcdc2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fcdc2-109">EXAMPLES</span></span>

### <span data-ttu-id="fcdc2-110">예제 1: 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fcdc2-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="fcdc2-111">이 명령은 리소스 그룹 이름 MyResourceGroup에 대 한 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="fcdc2-112">예제 2: BlobStorage Kind 및 hot AccessTier를 사용 하 여 Blob 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fcdc2-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="fcdc2-113">이 명령은 BlobStorage Kind 및 hot AccessTier를 사용 하는 Blob 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="fcdc2-114">예제 3: Kind StorageV2를 사용 하 여 저장소 계정을 만들고 Azure KeyVault에 대 한 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="fcdc2-115">이 명령은 Kind StorageV2를 사용 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="fcdc2-116">또한 Azure KeyVault를 통해 계정 키를 관리 하는 데 사용할 수 있는 id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="fcdc2-117">예제 4: JSON에서 NetworkRuleSet 집합을 사용 하 여 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fcdc2-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="fcdc2-118">이 명령은 JSON의 NetworkRuleSet 집합 속성이 있는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="fcdc2-119">예제 5: 계층적 네임 스페이스를 사용 하는 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fcdc2-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="fcdc2-120">이 명령은 계층적 네임 스페이스를 사용 하도록 설정 된 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="fcdc2-121">예제 6: Azure Files AAD DS 인증을 사용 하 여 저장소 계정을 만들고, 큰 파일 공유를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="fcdc2-122">이 명령은 Azure Files AAD DS 인증을 사용 하 여 저장소 계정을 만들고, 큰 파일 공유를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="fcdc2-123">예제 7: 파일 Active Directory 도메인 서비스 인증을 사용 하 여 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fcdc2-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="fcdc2-124">이 명령은 저장소 계정 withenable Active Directory 도메인 서비스 인증을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="fcdc2-125">예제 8: 큐 및 테이블 서비스가 포함 된 저장소 계정 만들기 계정 범위 암호화 키를 사용 하 고 인프라 암호화가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="fcdc2-126">이 명령은 큐 및 테이블 서비스를 사용 하 여 계정 범위 암호화 키를 만들고, 인프라 암호화가 필요 하므로, 대기열과 테이블은 Blob 및 파일 서비스와 동일한 암호화 키를 사용 하 고, 서비스는 나머지 데이터에 대 한 플랫폼 관리 키와 암호화의 보조 계층을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="fcdc2-127">그런 다음 저장소 계정 속성을 가져오고 대기열 및 테이블 서비스의 암호화 keytype 및 RequireInfrastructureEncryption value를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="fcdc2-128">예제 9: 계정 만들기 이상 \ a s 버전과 AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="fcdc2-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="fcdc2-129">예 버전 및 AllowBlobPublicAccess를 사용 하 여 계정 만들기 명령으로 만든 다음 생성 된 계정의 2 가지 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="fcdc2-130">변수</span><span class="sxs-lookup"><span data-stu-id="fcdc2-130">PARAMETERS</span></span>

### <span data-ttu-id="fcdc2-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="fcdc2-131">-AccessTier</span></span>
<span data-ttu-id="fcdc2-132">이 cmdlet이 만드는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fcdc2-133">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="fcdc2-134">*Kind* 매개 변수에 대 한 blobstorage의 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="fcdc2-135">이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="fcdc2-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="fcdc2-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="fcdc2-137">Azure Storage에 대 한 SID (보안 식별자)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="fcdc2-138">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="fcdc2-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="fcdc2-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="fcdc2-140">도메인 GUID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-140">Specifies the domain GUID.</span></span> <span data-ttu-id="fcdc2-141">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="fcdc2-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="fcdc2-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="fcdc2-143">광고 DNS 서버에 대해 권한이 있는 기본 도메인을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="fcdc2-144">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="fcdc2-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="fcdc2-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="fcdc2-146">SID (보안 식별자)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="fcdc2-147">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="fcdc2-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="fcdc2-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="fcdc2-149">가져올 Active Directory 포리스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="fcdc2-150">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="fcdc2-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="fcdc2-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="fcdc2-152">NetBIOS 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="fcdc2-153">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="fcdc2-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="fcdc2-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="fcdc2-155">저장소 계정의 모든 blob 또는 컨테이너에 대 한 공용 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="fcdc2-156">이 속성에 대 한 기본 해석은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="fcdc2-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcdc2-157">-AsJob</span></span>
<span data-ttu-id="fcdc2-158">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fcdc2-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcdc2-159">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="fcdc2-159">-AssignIdentity</span></span>
<span data-ttu-id="fcdc2-160">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fcdc2-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="fcdc2-161">-CustomDomainName</span></span>
<span data-ttu-id="fcdc2-162">저장소 계정의 사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="fcdc2-163">기본 값은 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="fcdc2-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdc2-164">-DefaultProfile</span></span>
<span data-ttu-id="fcdc2-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcdc2-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="fcdc2-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="fcdc2-167">Azure Files 저장소 계정에 대 한 Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="fcdc2-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="fcdc2-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="fcdc2-169">Azure Files 저장소 계정에 대 한 azure Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="fcdc2-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="fcdc2-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="fcdc2-171">저장소 계정이 계층적 네임 스페이스를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="fcdc2-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="fcdc2-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="fcdc2-173">저장소 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="fcdc2-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="fcdc2-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="fcdc2-175">저장소 계정이 5 개 이상의 TiB 용량으로 큰 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="fcdc2-176">계정을 사용 하도록 설정한 후에는 해당 기능을 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="fcdc2-177">현재 LRS 및 ZRS 복제 유형에만 지원 되므로 지역 중복 계정으로 계정 변환을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="fcdc2-178">자세한 정보 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="fcdc2-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="fcdc2-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="fcdc2-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="fcdc2-180">큐에 대 한 암호화 KeyType을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="fcdc2-181">기본 값은 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-181">The default value is Service.</span></span>
<span data-ttu-id="fcdc2-182">-Account: 대기열이 계정 범위 암호화 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="fcdc2-183">-서비스: 큐는 항상 Service-Managed 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="fcdc2-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="fcdc2-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="fcdc2-185">테이블에 대 한 암호화 KeyType을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="fcdc2-186">기본 값은 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-186">The default value is Service.</span></span>
- <span data-ttu-id="fcdc2-187">계정: 테이블은 계정 범위 암호화 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="fcdc2-188">서비스: 테이블은 항상 Service-Managed 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="fcdc2-189">-종류</span><span class="sxs-lookup"><span data-stu-id="fcdc2-189">-Kind</span></span>
<span data-ttu-id="fcdc2-190">이 cmdlet이 만드는 저장소 계정의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fcdc2-191">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fcdc2-192">용량.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-192">Storage.</span></span> <span data-ttu-id="fcdc2-193">Blob, 테이블, 대기열, 파일, 디스크의 저장소를 지 원하는 범용 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="fcdc2-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-194">StorageV2.</span></span> <span data-ttu-id="fcdc2-195">데이터 계층화와 같은 고급 기능을 사용 하 여 Blob, 테이블, 대기열, 파일, 디스크를 지 원하는 범용 GPv2 (범용 버전 2) 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="fcdc2-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-196">BlobStorage.</span></span> <span data-ttu-id="fcdc2-197">Blob 저장소만 지 원하는 blob 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="fcdc2-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-198">BlockBlobStorage.</span></span> <span data-ttu-id="fcdc2-199">블록 blob 저장소만 지 원하는 block Blob 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="fcdc2-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-200">FileStorage.</span></span> <span data-ttu-id="fcdc2-201">파일 저장소만 지 원하는 파일 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="fcdc2-202">기본 값은 StorageV2입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="fcdc2-203">-위치</span><span class="sxs-lookup"><span data-stu-id="fcdc2-203">-Location</span></span>
<span data-ttu-id="fcdc2-204">만들 저장소 계정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="fcdc2-205">-없음 Tls 버전</span><span class="sxs-lookup"><span data-stu-id="fcdc2-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="fcdc2-206">저장소 요청에 허용 되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="fcdc2-207">기본 해석은이 속성에 대 한 TLS 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="fcdc2-208">-이름</span><span class="sxs-lookup"><span data-stu-id="fcdc2-208">-Name</span></span>
<span data-ttu-id="fcdc2-209">만들 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="fcdc2-210">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="fcdc2-210">-NetworkRuleSet</span></span>
<span data-ttu-id="fcdc2-211">NetworkRuleSet는 방화벽과 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 규칙을 우회 하도록 허용 된 서비스 같은 네트워크 속성에 대 한 값을 설정 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="fcdc2-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="fcdc2-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="fcdc2-213">서비스는 나머지 데이터에 대 한 플랫폼 관리 키를 사용 하 여 암호화의 보조 계층을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="fcdc2-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcdc2-214">-ResourceGroupName</span></span>
<span data-ttu-id="fcdc2-215">저장소 계정을 추가할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="fcdc2-216">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="fcdc2-216">-SkuName</span></span>
<span data-ttu-id="fcdc2-217">이 cmdlet이 만드는 저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fcdc2-218">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fcdc2-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-219">Standard_LRS.</span></span> <span data-ttu-id="fcdc2-220">로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-221">Standard_ZRS.</span></span> <span data-ttu-id="fcdc2-222">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-223">Standard_GRS.</span></span> <span data-ttu-id="fcdc2-224">지리적 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-225">Standard_RAGRS.</span></span> <span data-ttu-id="fcdc2-226">액세스 지리적 중복 저장소 읽기</span><span class="sxs-lookup"><span data-stu-id="fcdc2-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-227">Premium_LRS.</span></span> <span data-ttu-id="fcdc2-228">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-229">Premium_ZRS.</span></span> <span data-ttu-id="fcdc2-230">프리미엄 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-231">Standard_GZRS 지역 중복 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="fcdc2-232">Standard_RAGZRS-액세스 지리적 중복 영역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="fcdc2-233">태그</span><span class="sxs-lookup"><span data-stu-id="fcdc2-233">-Tag</span></span>
<span data-ttu-id="fcdc2-234">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fcdc2-235">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fcdc2-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fcdc2-236">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="fcdc2-236">-UseSubDomain</span></span>
<span data-ttu-id="fcdc2-237">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="fcdc2-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdc2-238">CommonParameters</span></span>
<span data-ttu-id="fcdc2-239">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdc2-240">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcdc2-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdc2-241">입력</span><span class="sxs-lookup"><span data-stu-id="fcdc2-241">INPUTS</span></span>

### <span data-ttu-id="fcdc2-242">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcdc2-242">System.String</span></span>

## <span data-ttu-id="fcdc2-243">출력</span><span class="sxs-lookup"><span data-stu-id="fcdc2-243">OUTPUTS</span></span>

### <span data-ttu-id="fcdc2-244">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdc2-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fcdc2-245">상속자</span><span class="sxs-lookup"><span data-stu-id="fcdc2-245">NOTES</span></span>

## <span data-ttu-id="fcdc2-246">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcdc2-246">RELATED LINKS</span></span>

[<span data-ttu-id="fcdc2-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdc2-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="fcdc2-248">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdc2-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="fcdc2-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdc2-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
