---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 316bcbd8efa101a53dc36ede5e56e2b9379f02e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698631"
---
# <span data-ttu-id="97277-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97277-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="97277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97277-102">SYNOPSIS</span></span>
<span data-ttu-id="97277-103">저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-103">Creates a Storage account.</span></span>

## <span data-ttu-id="97277-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97277-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97277-105">설명은</span><span class="sxs-lookup"><span data-stu-id="97277-105">DESCRIPTION</span></span>
<span data-ttu-id="97277-106">**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="97277-107">예제의</span><span class="sxs-lookup"><span data-stu-id="97277-107">EXAMPLES</span></span>

### <span data-ttu-id="97277-108">예제 1: 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="97277-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="97277-109">이 명령은 리소스 그룹 이름 MyResourceGroup에 대 한 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="97277-110">예제 2: BlobStorage Kind 및 hot AccessTier를 사용 하 여 Blob 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="97277-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="97277-111">이 명령은 BlobStorage Kind 및 hot AccessTier를 사용 하는 Blob 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="97277-112">예제 3: Kind StorageV2를 사용 하 여 저장소 계정을 만들고 Azure KeyVault에 대 한 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="97277-113">이 명령은 Kind StorageV2를 사용 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="97277-114">또한 Azure KeyVault를 통해 계정 키를 관리 하는 데 사용할 수 있는 id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="97277-115">예제 4: JSON에서 NetworkRuleSet 집합을 사용 하 여 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="97277-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="97277-116">이 명령은 JSON의 NetworkRuleSet 집합 속성이 있는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="97277-117">예제 5: 계층적 네임 스페이스를 사용 하는 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="97277-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="97277-118">이 명령은 계층적 네임 스페이스를 사용 하도록 설정 된 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97277-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

## <span data-ttu-id="97277-119">변수</span><span class="sxs-lookup"><span data-stu-id="97277-119">PARAMETERS</span></span>

### <span data-ttu-id="97277-120">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="97277-120">-AccessTier</span></span>
<span data-ttu-id="97277-121">이 cmdlet이 만드는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-121">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="97277-122">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-122">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="97277-123">*Kind* 매개 변수에 대 한 blobstorage의 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-123">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="97277-124">이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="97277-124">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="97277-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97277-125">-AsJob</span></span>
<span data-ttu-id="97277-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="97277-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97277-127">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="97277-127">-AssignIdentity</span></span>
<span data-ttu-id="97277-128">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-128">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="97277-129">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="97277-129">-CustomDomainName</span></span>
<span data-ttu-id="97277-130">저장소 계정의 사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-130">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="97277-131">기본 값은 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-131">The default value is Storage.</span></span>

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

### <span data-ttu-id="97277-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97277-132">-DefaultProfile</span></span>
<span data-ttu-id="97277-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97277-134">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="97277-134">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="97277-135">저장소 계정이 계층적 네임 스페이스를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="97277-135">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="97277-136">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="97277-136">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="97277-137">저장소 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="97277-137">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="97277-138">-종류</span><span class="sxs-lookup"><span data-stu-id="97277-138">-Kind</span></span>
<span data-ttu-id="97277-139">이 cmdlet이 만드는 저장소 계정의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-139">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="97277-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="97277-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97277-141">용량.</span><span class="sxs-lookup"><span data-stu-id="97277-141">Storage.</span></span> <span data-ttu-id="97277-142">Blob, 테이블, 대기열, 파일, 디스크의 저장소를 지 원하는 범용 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-142">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="97277-143">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="97277-143">StorageV2.</span></span> <span data-ttu-id="97277-144">데이터 계층화와 같은 고급 기능을 사용 하 여 Blob, 테이블, 대기열, 파일, 디스크를 지 원하는 범용 GPv2 (범용 버전 2) 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-144">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="97277-145">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="97277-145">BlobStorage.</span></span> <span data-ttu-id="97277-146">Blob 저장소만 지 원하는 blob 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-146">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="97277-147">기본 값은 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-147">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97277-148">-위치</span><span class="sxs-lookup"><span data-stu-id="97277-148">-Location</span></span>
<span data-ttu-id="97277-149">만들 저장소 계정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-149">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="97277-150">-이름</span><span class="sxs-lookup"><span data-stu-id="97277-150">-Name</span></span>
<span data-ttu-id="97277-151">만들 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-151">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="97277-152">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="97277-152">-NetworkRuleSet</span></span>
<span data-ttu-id="97277-153">NetworkRuleSet는 방화벽과 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 규칙을 우회 하도록 허용 된 서비스 같은 네트워크 속성에 대 한 값을 설정 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97277-153">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="97277-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97277-154">-ResourceGroupName</span></span>
<span data-ttu-id="97277-155">저장소 계정을 추가할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-155">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="97277-156">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="97277-156">-SkuName</span></span>
<span data-ttu-id="97277-157">이 cmdlet이 만드는 저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-157">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="97277-158">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="97277-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97277-159">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="97277-159">Standard_LRS.</span></span> <span data-ttu-id="97277-160">로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="97277-160">Locally-redundant storage.</span></span>
- <span data-ttu-id="97277-161">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="97277-161">Standard_ZRS.</span></span> <span data-ttu-id="97277-162">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="97277-162">Zone-redundant storage.</span></span>
- <span data-ttu-id="97277-163">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="97277-163">Standard_GRS.</span></span> <span data-ttu-id="97277-164">지리적 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="97277-164">Geo-redundant storage.</span></span>
- <span data-ttu-id="97277-165">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="97277-165">Standard_RAGRS.</span></span> <span data-ttu-id="97277-166">액세스 지리적 중복 저장소 읽기</span><span class="sxs-lookup"><span data-stu-id="97277-166">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="97277-167">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="97277-167">Premium_LRS.</span></span> <span data-ttu-id="97277-168">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="97277-168">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97277-169">태그</span><span class="sxs-lookup"><span data-stu-id="97277-169">-Tag</span></span>
<span data-ttu-id="97277-170">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="97277-170">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="97277-171">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="97277-171">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97277-172">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="97277-172">-UseSubDomain</span></span>
<span data-ttu-id="97277-173">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="97277-173">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="97277-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97277-174">CommonParameters</span></span>
<span data-ttu-id="97277-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97277-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97277-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97277-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97277-177">입력</span><span class="sxs-lookup"><span data-stu-id="97277-177">INPUTS</span></span>

### <span data-ttu-id="97277-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="97277-178">System.String</span></span>

## <span data-ttu-id="97277-179">출력</span><span class="sxs-lookup"><span data-stu-id="97277-179">OUTPUTS</span></span>

### <span data-ttu-id="97277-180">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97277-180">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="97277-181">상속자</span><span class="sxs-lookup"><span data-stu-id="97277-181">NOTES</span></span>

## <span data-ttu-id="97277-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97277-182">RELATED LINKS</span></span>

[<span data-ttu-id="97277-183">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97277-183">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="97277-184">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97277-184">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="97277-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97277-185">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
