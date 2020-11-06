---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534552"
---
# <span data-ttu-id="1cf9a-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf9a-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="1cf9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf9a-103">저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cf9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cf9a-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1cf9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1cf9a-105">DESCRIPTION</span></span>
<span data-ttu-id="1cf9a-106">**AzureRmStorageAccount** Cmdlet은 Azure 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="1cf9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1cf9a-107">EXAMPLES</span></span>

### <span data-ttu-id="1cf9a-108">예제 1: 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="1cf9a-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="1cf9a-109">이 명령은 리소스 그룹 이름 MyResourceGroup에 대 한 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="1cf9a-110">예제 2: 저장소 서비스 암호화를 사용 하는 Blob 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="1cf9a-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="1cf9a-111">이 명령은 핫 access 형식을 사용 하는 Blob 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="1cf9a-112">계정에서 Blob 서비스에 대 한 저장소 서비스 암호화를 사용 하도록 설정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="1cf9a-113">예제 3: Blob 및 파일 서비스에서 저장소 서비스 암호화를 사용 하도록 설정 하 고 Azure KeyVault에 대 한 Id를 생성 하 고 할당 하는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="1cf9a-114">이 명령은 Blob 및 파일 서비스에서 저장소 서비스 암호화를 사용 하도록 설정 하는 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="1cf9a-115">또한 Azure KeyVault를 통해 계정 키를 관리 하는 데 사용할 수 있는 id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="1cf9a-116">변수</span><span class="sxs-lookup"><span data-stu-id="1cf9a-116">PARAMETERS</span></span>

### <span data-ttu-id="1cf9a-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="1cf9a-117">-AccessTier</span></span>
<span data-ttu-id="1cf9a-118">이 cmdlet이 만드는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1cf9a-119">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="1cf9a-120">*Kind* 매개 변수에 대 한 blobstorage의 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="1cf9a-121">이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-122">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="1cf9a-122">-AssignIdentity</span></span>
<span data-ttu-id="1cf9a-123">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="1cf9a-124">-CustomDomainName</span></span>
<span data-ttu-id="1cf9a-125">저장소 계정의 사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="1cf9a-126">기본 값은 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-127">-Enable\ \ 서비스</span><span class="sxs-lookup"><span data-stu-id="1cf9a-127">-EnableEncryptionService</span></span>
<span data-ttu-id="1cf9a-128">이 cmdlet이 저장소 서비스에서 저장소 서비스 암호화를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="1cf9a-129">Azure Blob 및 Azure 파일 서비스가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="1cf9a-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="1cf9a-131">저장소 계정이 https 트래픽만 사용 하도록 설정 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1cf9a-132">-InformationAction</span></span>
<span data-ttu-id="1cf9a-133">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1cf9a-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1cf9a-135">하기로</span><span class="sxs-lookup"><span data-stu-id="1cf9a-135">Continue</span></span>
- <span data-ttu-id="1cf9a-136">숨기기</span><span class="sxs-lookup"><span data-stu-id="1cf9a-136">Ignore</span></span>
- <span data-ttu-id="1cf9a-137">Inquire</span><span class="sxs-lookup"><span data-stu-id="1cf9a-137">Inquire</span></span>
- <span data-ttu-id="1cf9a-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1cf9a-138">SilentlyContinue</span></span>
- <span data-ttu-id="1cf9a-139">중지가</span><span class="sxs-lookup"><span data-stu-id="1cf9a-139">Stop</span></span>
- <span data-ttu-id="1cf9a-140">대기</span><span class="sxs-lookup"><span data-stu-id="1cf9a-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1cf9a-141">-InformationVariable</span></span>
<span data-ttu-id="1cf9a-142">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-143">-종류</span><span class="sxs-lookup"><span data-stu-id="1cf9a-143">-Kind</span></span>
<span data-ttu-id="1cf9a-144">이 cmdlet이 만드는 저장소 계정의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1cf9a-145">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1cf9a-146">용량.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-146">Storage.</span></span>
<span data-ttu-id="1cf9a-147">Blob, 테이블, 대기열, 파일, 디스크의 저장소를 지 원하는 범용 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="1cf9a-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-148">BlobStorage.</span></span>
<span data-ttu-id="1cf9a-149">Blob 저장소만 지 원하는 blob 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="1cf9a-150">기본 값은 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-151">-위치</span><span class="sxs-lookup"><span data-stu-id="1cf9a-151">-Location</span></span>
<span data-ttu-id="1cf9a-152">만들 저장소 계정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-153">-이름</span><span class="sxs-lookup"><span data-stu-id="1cf9a-153">-Name</span></span>
<span data-ttu-id="1cf9a-154">만들 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf9a-155">-ResourceGroupName</span></span>
<span data-ttu-id="1cf9a-156">저장소 계정을 추가할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-157">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="1cf9a-157">-SkuName</span></span>
<span data-ttu-id="1cf9a-158">이 cmdlet이 만드는 저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="1cf9a-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1cf9a-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-160">Standard_LRS.</span></span>
<span data-ttu-id="1cf9a-161">로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="1cf9a-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-162">Standard_ZRS.</span></span>
<span data-ttu-id="1cf9a-163">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="1cf9a-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-164">Standard_GRS.</span></span>
<span data-ttu-id="1cf9a-165">지리적 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="1cf9a-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-166">Standard_RAGRS.</span></span>
<span data-ttu-id="1cf9a-167">액세스 지리적 중복 저장소 읽기</span><span class="sxs-lookup"><span data-stu-id="1cf9a-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="1cf9a-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-168">Premium_LRS.</span></span>
<span data-ttu-id="1cf9a-169">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-170">태그</span><span class="sxs-lookup"><span data-stu-id="1cf9a-170">-Tag</span></span>
<span data-ttu-id="1cf9a-171">*Kind* 매개 변수에 대 한 blobstorage의 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="1cf9a-172">이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-173">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="1cf9a-173">-UseSubDomain</span></span>
<span data-ttu-id="1cf9a-174">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf9a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf9a-175">CommonParameters</span></span>
<span data-ttu-id="1cf9a-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf9a-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf9a-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf9a-178">입력</span><span class="sxs-lookup"><span data-stu-id="1cf9a-178">INPUTS</span></span>

### <span data-ttu-id="1cf9a-179">않아야</span><span class="sxs-lookup"><span data-stu-id="1cf9a-179">None</span></span>
<span data-ttu-id="1cf9a-180">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cf9a-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1cf9a-181">출력</span><span class="sxs-lookup"><span data-stu-id="1cf9a-181">OUTPUTS</span></span>

## <span data-ttu-id="1cf9a-182">상속자</span><span class="sxs-lookup"><span data-stu-id="1cf9a-182">NOTES</span></span>

## <span data-ttu-id="1cf9a-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cf9a-183">RELATED LINKS</span></span>

[<span data-ttu-id="1cf9a-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf9a-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="1cf9a-185">제거-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf9a-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="1cf9a-186">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1cf9a-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
