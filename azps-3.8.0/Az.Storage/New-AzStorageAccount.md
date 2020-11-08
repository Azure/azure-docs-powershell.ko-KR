---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043146"
---
# <span data-ttu-id="fb6ab-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb6ab-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="fb6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6ab-103">저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-103">Creates a Storage account.</span></span>

## <span data-ttu-id="fb6ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb6ab-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb6ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6ab-106">**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="fb6ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6ab-108">예제 1: 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fb6ab-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="fb6ab-109">이 명령은 리소스 그룹 이름 MyResourceGroup에 대 한 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="fb6ab-110">예제 2: BlobStorage Kind 및 hot AccessTier를 사용 하 여 Blob 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fb6ab-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="fb6ab-111">이 명령은 BlobStorage Kind 및 hot AccessTier를 사용 하는 Blob 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="fb6ab-112">예제 3: Kind StorageV2를 사용 하 여 저장소 계정을 만들고 Azure KeyVault에 대 한 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="fb6ab-113">이 명령은 Kind StorageV2를 사용 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="fb6ab-114">또한 Azure KeyVault를 통해 계정 키를 관리 하는 데 사용할 수 있는 id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="fb6ab-115">예제 4: JSON에서 NetworkRuleSet 집합을 사용 하 여 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fb6ab-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="fb6ab-116">이 명령은 JSON의 NetworkRuleSet 집합 속성이 있는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="fb6ab-117">예제 5: 계층적 네임 스페이스를 사용 하는 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fb6ab-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="fb6ab-118">이 명령은 계층적 네임 스페이스를 사용 하도록 설정 된 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="fb6ab-119">예제 6: Azure Files AAD DS 인증을 사용 하 여 저장소 계정을 만들고, 큰 파일 공유를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="fb6ab-120">이 명령은 Azure Files AAD DS 인증을 사용 하 여 저장소 계정을 만들고, 큰 파일 공유를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="fb6ab-121">예제 8: 큐 및 테이블 서비스가 포함 된 저장소 계정 만들기 계정 범위 암호화 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="fb6ab-122">이 명령은 큐 및 테이블 서비스가 계정 범위의 암호화 키를 사용 하 여 저장소 계정을 만들기 때문에 대기열과 테이블은 Blob 및 File 서비스와 동일한 암호화 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="fb6ab-123">그런 다음 저장소 계정 속성을 가져오고 대기열 및 테이블 서비스의 암호화 keytype을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="fb6ab-124">변수</span><span class="sxs-lookup"><span data-stu-id="fb6ab-124">PARAMETERS</span></span>

### <span data-ttu-id="fb6ab-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="fb6ab-125">-AccessTier</span></span>
<span data-ttu-id="fb6ab-126">이 cmdlet이 만드는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fb6ab-127">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="fb6ab-128">*Kind* 매개 변수에 대 한 blobstorage의 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="fb6ab-129">이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="fb6ab-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb6ab-130">-AsJob</span></span>
<span data-ttu-id="fb6ab-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb6ab-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb6ab-132">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="fb6ab-132">-AssignIdentity</span></span>
<span data-ttu-id="fb6ab-133">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fb6ab-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="fb6ab-134">-CustomDomainName</span></span>
<span data-ttu-id="fb6ab-135">저장소 계정의 사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="fb6ab-136">기본 값은 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="fb6ab-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6ab-137">-DefaultProfile</span></span>
<span data-ttu-id="fb6ab-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6ab-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="fb6ab-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="fb6ab-140">Azure Files 저장소 계정에 대 한 azure Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="fb6ab-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="fb6ab-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="fb6ab-142">저장소 계정이 계층적 네임 스페이스를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="fb6ab-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="fb6ab-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="fb6ab-144">저장소 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="fb6ab-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="fb6ab-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="fb6ab-146">저장소 계정이 5 개 이상의 TiB 용량으로 큰 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="fb6ab-147">계정을 사용 하도록 설정한 후에는 해당 기능을 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="fb6ab-148">현재 LRS 및 ZRS 복제 유형에만 지원 되므로 지역 중복 계정으로 계정 변환을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="fb6ab-149">자세한 정보 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="fb6ab-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="fb6ab-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="fb6ab-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="fb6ab-151">큐에 대 한 암호화 KeyType을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="fb6ab-152">기본 값은 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-152">The default value is Service.</span></span>
<span data-ttu-id="fb6ab-153">-Account: 대기열이 계정 범위 암호화 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="fb6ab-154">-서비스: 큐는 항상 Service-Managed 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="fb6ab-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="fb6ab-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="fb6ab-156">테이블에 대 한 암호화 KeyType을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="fb6ab-157">기본 값은 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-157">The default value is Service.</span></span>
- <span data-ttu-id="fb6ab-158">계정: 테이블은 계정 범위 암호화 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="fb6ab-159">서비스: 테이블은 항상 Service-Managed 키를 사용 하 여 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="fb6ab-160">-종류</span><span class="sxs-lookup"><span data-stu-id="fb6ab-160">-Kind</span></span>
<span data-ttu-id="fb6ab-161">이 cmdlet이 만드는 저장소 계정의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fb6ab-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb6ab-163">용량.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-163">Storage.</span></span> <span data-ttu-id="fb6ab-164">Blob, 테이블, 대기열, 파일, 디스크의 저장소를 지 원하는 범용 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="fb6ab-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-165">StorageV2.</span></span> <span data-ttu-id="fb6ab-166">데이터 계층화와 같은 고급 기능을 사용 하 여 Blob, 테이블, 대기열, 파일, 디스크를 지 원하는 범용 GPv2 (범용 버전 2) 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="fb6ab-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-167">BlobStorage.</span></span> <span data-ttu-id="fb6ab-168">Blob 저장소만 지 원하는 blob 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="fb6ab-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-169">BlockBlobStorage.</span></span> <span data-ttu-id="fb6ab-170">블록 blob 저장소만 지 원하는 block Blob 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="fb6ab-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-171">FileStorage.</span></span> <span data-ttu-id="fb6ab-172">파일 저장소만 지 원하는 파일 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="fb6ab-173">기본 값은 StorageV2입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6ab-174">-위치</span><span class="sxs-lookup"><span data-stu-id="fb6ab-174">-Location</span></span>
<span data-ttu-id="fb6ab-175">만들 저장소 계정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="fb6ab-176">-이름</span><span class="sxs-lookup"><span data-stu-id="fb6ab-176">-Name</span></span>
<span data-ttu-id="fb6ab-177">만들 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-177">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="fb6ab-178">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="fb6ab-178">-NetworkRuleSet</span></span>
<span data-ttu-id="fb6ab-179">NetworkRuleSet는 방화벽과 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 규칙을 우회 하도록 허용 된 서비스 같은 네트워크 속성에 대 한 값을 설정 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="fb6ab-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6ab-180">-ResourceGroupName</span></span>
<span data-ttu-id="fb6ab-181">저장소 계정을 추가할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="fb6ab-182">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="fb6ab-182">-SkuName</span></span>
<span data-ttu-id="fb6ab-183">이 cmdlet이 만드는 저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fb6ab-184">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb6ab-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-185">Standard_LRS.</span></span> <span data-ttu-id="fb6ab-186">로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-187">Standard_ZRS.</span></span> <span data-ttu-id="fb6ab-188">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-189">Standard_GRS.</span></span> <span data-ttu-id="fb6ab-190">지리적 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-191">Standard_RAGRS.</span></span> <span data-ttu-id="fb6ab-192">액세스 지리적 중복 저장소 읽기</span><span class="sxs-lookup"><span data-stu-id="fb6ab-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-193">Premium_LRS.</span></span> <span data-ttu-id="fb6ab-194">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-195">Premium_ZRS.</span></span> <span data-ttu-id="fb6ab-196">프리미엄 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-197">Standard_GZRS 지역 중복 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="fb6ab-198">Standard_RAGZRS-액세스 지리적 중복 영역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="fb6ab-199">태그</span><span class="sxs-lookup"><span data-stu-id="fb6ab-199">-Tag</span></span>
<span data-ttu-id="fb6ab-200">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fb6ab-201">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fb6ab-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fb6ab-202">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="fb6ab-202">-UseSubDomain</span></span>
<span data-ttu-id="fb6ab-203">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="fb6ab-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6ab-204">CommonParameters</span></span>
<span data-ttu-id="fb6ab-205">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6ab-206">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb6ab-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6ab-207">입력</span><span class="sxs-lookup"><span data-stu-id="fb6ab-207">INPUTS</span></span>

### <span data-ttu-id="fb6ab-208">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb6ab-208">System.String</span></span>

## <span data-ttu-id="fb6ab-209">출력</span><span class="sxs-lookup"><span data-stu-id="fb6ab-209">OUTPUTS</span></span>

### <span data-ttu-id="fb6ab-210">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb6ab-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fb6ab-211">상속자</span><span class="sxs-lookup"><span data-stu-id="fb6ab-211">NOTES</span></span>

## <span data-ttu-id="fb6ab-212">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb6ab-212">RELATED LINKS</span></span>

[<span data-ttu-id="fb6ab-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb6ab-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="fb6ab-214">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb6ab-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="fb6ab-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb6ab-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
