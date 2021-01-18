---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494694"
---
# <span data-ttu-id="91607-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91607-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="91607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91607-102">SYNOPSIS</span></span>
<span data-ttu-id="91607-103">Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-103">Creates a Storage account.</span></span>

## <span data-ttu-id="91607-104">구문</span><span class="sxs-lookup"><span data-stu-id="91607-104">SYNTAX</span></span>

### <span data-ttu-id="91607-105">AzureActiveDirectoryDomainServicesForFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="91607-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91607-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="91607-106">ActiveDirectoryDomainServicesForFile</span></span>
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

## <span data-ttu-id="91607-107">설명</span><span class="sxs-lookup"><span data-stu-id="91607-107">DESCRIPTION</span></span>
<span data-ttu-id="91607-108">**New-AzStorageAccount** cmdlet은 Azure Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="91607-109">예제</span><span class="sxs-lookup"><span data-stu-id="91607-109">EXAMPLES</span></span>

### <span data-ttu-id="91607-110">예제 1: Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="91607-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="91607-111">이 명령은 MyResourceGroup 리소스 그룹 이름에 대한 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="91607-112">예제 2: BlobStorage Kind 및 hot AccessTier를 사용하여 Blob Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="91607-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="91607-113">이 명령은 BlobStorage Kind 및 hot AccessTier를 사용하여 Blob Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="91607-114">예제 3: Kind StorageV2를 사용하여 Storage 계정을 만들고 Azure KeyVault에 대한 ID를 생성 및 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="91607-115">이 명령은 Kind StorageV2를 사용하여 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="91607-116">또한 Azure KeyVault를 통해 계정 키를 관리하는 데 사용할 수 있는 ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="91607-117">예제 4: JSON에서 NetworkRuleSet을 사용하여 Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="91607-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="91607-118">이 명령은 JSON에서 NetworkRuleSet 속성이 있는 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="91607-119">예제 5: 계층적 네임스페이스를 사용하도록 설정된 Storage 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="91607-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="91607-120">이 명령은 계층적 네임스페이스를 사용하도록 설정된 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="91607-121">예제 6: Azure Files AAD DS 인증을 사용하여 Storage 계정을 만들고 큰 파일 공유를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="91607-122">이 명령은 Azure Files AAD DS 인증을 사용하여 Storage 계정을 만들고 대용량 파일 공유를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="91607-123">예제 7: Files Active Directory 도메인 서비스 인증을 사용하도록 설정하여 Storage 계정을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="91607-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="91607-124">이 명령은 파일 Active Directory 도메인 서비스 인증을 사용하여 Storage 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91607-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="91607-125">예제 8: Queue 및 Table Service에서 계정 범위 암호화 키를 사용하며 인프라 암호화 필요를 사용하여 Storage 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="91607-126">이 명령은 큐 및 Table Service에서 계정 범위 암호화 키 및 인프라 암호화 필요를 사용하여 Storage 계정을 만듭니다. 따라서 큐와 테이블은 Blob 및 파일 서비스에서 동일한 암호화 키를 사용하며, 서비스는 미사용 데이터에 대해 플랫폼 관리 키를 사용하여 보조 암호화 계층을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="91607-127">그런 다음 Storage 계정 속성을 얻습니다. 큐 및 Table Service의 암호화 키타프 및 RequireInfrastructureEncryption 값을 본다.</span><span class="sxs-lookup"><span data-stu-id="91607-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="91607-128">예제 9: MinimumTlsVersion 및 AllowBlobPublicAccess 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="91607-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="91607-129">이 명령은 MinimumTlsVersion 및 AllowBlobPublicAccess를 사용하여 계정을 만든 다음, 만든 계정의 2개 속성을 보여 주며</span><span class="sxs-lookup"><span data-stu-id="91607-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="91607-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91607-130">PARAMETERS</span></span>

### <span data-ttu-id="91607-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="91607-131">-AccessTier</span></span>
<span data-ttu-id="91607-132">이 cmdlet에서 만드는 Storage 계정의 액세스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="91607-133">이 매개 변수에 허용되는 값은 핫 및 쿨입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="91607-134">*Kind* 매개 변수에 BlobStorage 값을 지정하는 경우 *AccessTier* 매개 변수에 대한 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="91607-135">이 Kind 매개 변수에  대한 Storage 값을 지정하는 경우 *AccessTier* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="91607-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="91607-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="91607-137">Azure Storage에 대한 SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="91607-138">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="91607-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="91607-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="91607-140">도메인 GUID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-140">Specifies the domain GUID.</span></span> <span data-ttu-id="91607-141">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="91607-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="91607-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="91607-143">AD DNS 서버가 권한이 있는 주 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="91607-144">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="91607-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="91607-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="91607-146">SID(보안 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="91607-147">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="91607-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="91607-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="91607-149">얻을 Active Directory 포리스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="91607-150">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="91607-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="91607-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="91607-152">NetBIOS 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="91607-153">-EnableActiveDirectoryDomainServicesForFile이 true로 설정된 경우 이 매개 변수를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="91607-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="91607-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="91607-155">저장소 계정의 모든 Blob 또는 컨테이너에 대한 공용 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="91607-156">이 속성에 대한 기본 해석은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="91607-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91607-157">-AsJob</span></span>
<span data-ttu-id="91607-158">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="91607-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91607-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="91607-159">-AssignIdentity</span></span>
<span data-ttu-id="91607-160">Azure KeyVault와 같은 키 관리 서비스에서 사용할 새 Storage 계정 ID를 생성하고 이 Storage 계정에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="91607-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="91607-161">-CustomDomainName</span></span>
<span data-ttu-id="91607-162">Storage 계정의 사용자 지정 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="91607-163">기본값은 Storage입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="91607-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91607-164">-DefaultProfile</span></span>
<span data-ttu-id="91607-165">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91607-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="91607-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="91607-167">저장소 계정에 대해 Azure Files Active Directory Domain Service 인증을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="91607-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="91607-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="91607-169">저장소 계정에 대해 Azure Files Azure Active Directory Domain Service 인증을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="91607-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="91607-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="91607-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="91607-171">Storage 계정이 계층적 네임스페이스를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91607-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="91607-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="91607-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="91607-173">Storage 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91607-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="91607-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="91607-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="91607-175">저장소 계정이 용량이 5 TiB 이상인 대용량 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91607-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="91607-176">계정이 활성화되면 기능을 사용하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="91607-177">현재 LRS 및 ZRS 복제 유형에서만 지원됩니다. 따라서 계정은 지역 중복 계정으로 변환할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="91607-178">자세한 내용은 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="91607-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="91607-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="91607-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="91607-180">큐에 대한 암호화 KeyType을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="91607-181">기본값은 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-181">The default value is Service.</span></span>
<span data-ttu-id="91607-182">-Account: 큐는 계정 범위 암호화 키로 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91607-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="91607-183">-Service: 큐는 항상 Service-Managed 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91607-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="91607-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="91607-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="91607-185">테이블에 대한 암호화 KeyType을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="91607-186">기본값은 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-186">The default value is Service.</span></span>
- <span data-ttu-id="91607-187">계정: 테이블은 계정 범위 암호화 키로 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91607-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="91607-188">서비스: 테이블은 항상 Service-Managed 암호화됩니다.</span><span class="sxs-lookup"><span data-stu-id="91607-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="91607-189">-Kind</span><span class="sxs-lookup"><span data-stu-id="91607-189">-Kind</span></span>
<span data-ttu-id="91607-190">이 cmdlet에서 만드는 Storage 계정의 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="91607-191">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91607-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91607-192">저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-192">Storage.</span></span> <span data-ttu-id="91607-193">Blob, 테이블, 큐, 파일 및 디스크의 스토리지를 지원하는 일반 용도의 Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="91607-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="91607-194">StorageV2.</span></span> <span data-ttu-id="91607-195">데이터 계층화와 같은 고급 기능을 사용하여 Blob, 테이블, 큐, 파일 및 디스크를 지원하는 GPv2(General Purpose Version 2) Storage 계정</span><span class="sxs-lookup"><span data-stu-id="91607-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="91607-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="91607-196">BlobStorage.</span></span> <span data-ttu-id="91607-197">Blob의 스토리지만 지원하는 Blob Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="91607-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="91607-198">BlockBlobStorage.</span></span> <span data-ttu-id="91607-199">블록 Blob의 스토리지만 지원하는 블록 Blob Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="91607-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="91607-200">FileStorage.</span></span> <span data-ttu-id="91607-201">파일 스토리지만 지원하는 File Storage 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="91607-202">기본값은 StorageV2입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="91607-203">-Location</span><span class="sxs-lookup"><span data-stu-id="91607-203">-Location</span></span>
<span data-ttu-id="91607-204">만들 저장소 계정의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="91607-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="91607-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="91607-206">저장소에 대한 요청에 허용되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="91607-207">기본 해석은 이 속성에 대한 TLS 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="91607-208">-Name</span><span class="sxs-lookup"><span data-stu-id="91607-208">-Name</span></span>
<span data-ttu-id="91607-209">만들 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="91607-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="91607-210">-NetworkRuleSet</span></span>
<span data-ttu-id="91607-211">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고, 규칙을 무시할 수 있는 서비스 및 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="91607-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="91607-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="91607-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="91607-213">서비스는 미사용 데이터에 대한 플랫폼 관리 키를 사용하여 보조 암호화 계층을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="91607-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91607-214">-ResourceGroupName</span></span>
<span data-ttu-id="91607-215">Storage 계정을 추가할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="91607-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="91607-216">-SkuName</span></span>
<span data-ttu-id="91607-217">이 cmdlet에서 만드는 Storage 계정의 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="91607-218">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91607-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91607-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="91607-219">Standard_LRS.</span></span> <span data-ttu-id="91607-220">로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="91607-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="91607-221">Standard_ZRS.</span></span> <span data-ttu-id="91607-222">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="91607-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="91607-223">Standard_GRS.</span></span> <span data-ttu-id="91607-224">지역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="91607-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="91607-225">Standard_RAGRS.</span></span> <span data-ttu-id="91607-226">액세스 지역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="91607-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="91607-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="91607-227">Premium_LRS.</span></span> <span data-ttu-id="91607-228">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="91607-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="91607-229">Premium_ZRS.</span></span> <span data-ttu-id="91607-230">프리미엄 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="91607-231">Standard_GZRS - 지역 중복 영역 중복 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="91607-232">Standard_RAGZRS - 읽기 액세스 지역 중복 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="91607-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="91607-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="91607-233">-Tag</span></span>
<span data-ttu-id="91607-234">서버의 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="91607-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="91607-235">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="91607-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="91607-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="91607-236">-UseSubDomain</span></span>
<span data-ttu-id="91607-237">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91607-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="91607-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91607-238">CommonParameters</span></span>
<span data-ttu-id="91607-239">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91607-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91607-240">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="91607-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91607-241">입력</span><span class="sxs-lookup"><span data-stu-id="91607-241">INPUTS</span></span>

### <span data-ttu-id="91607-242">System.String</span><span class="sxs-lookup"><span data-stu-id="91607-242">System.String</span></span>

## <span data-ttu-id="91607-243">출력</span><span class="sxs-lookup"><span data-stu-id="91607-243">OUTPUTS</span></span>

### <span data-ttu-id="91607-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91607-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="91607-245">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91607-245">NOTES</span></span>

## <span data-ttu-id="91607-246">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91607-246">RELATED LINKS</span></span>

[<span data-ttu-id="91607-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91607-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="91607-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91607-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="91607-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91607-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
