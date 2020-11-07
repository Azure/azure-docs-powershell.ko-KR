---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: d75111b27b03317f757cbf0def4d9d66c43427c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703305"
---
# <span data-ttu-id="e25be-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e25be-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="e25be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e25be-102">SYNOPSIS</span></span>
<span data-ttu-id="e25be-103">Azure 저장소 blob에 대 한 SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e25be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e25be-104">SYNTAX</span></span>

### <span data-ttu-id="e25be-105">BlobNameWithPermission (기본값)</span><span class="sxs-lookup"><span data-stu-id="e25be-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e25be-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e25be-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e25be-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="e25be-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e25be-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="e25be-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e25be-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e25be-109">DESCRIPTION</span></span>
<span data-ttu-id="e25be-110">**AzureStorageBlobSASToken** Cmdlet은 Azure storage blob에 대 한 SAS (공유 액세스 서명) 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="e25be-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e25be-111">EXAMPLES</span></span>

### <span data-ttu-id="e25be-112">예제 1: full blob 권한을 사용 하 여 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="e25be-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="e25be-113">이 예제에서는 full blob 권한이 있는 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="e25be-114">예제 2: 수명 기간 동안 blob SAS 토큰 생성</span><span class="sxs-lookup"><span data-stu-id="e25be-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e25be-115">이 예제에서는 수명 기간 동안 blob SAS 토큰을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="e25be-116">변수</span><span class="sxs-lookup"><span data-stu-id="e25be-116">PARAMETERS</span></span>

### <span data-ttu-id="e25be-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="e25be-117">-Blob</span></span>
<span data-ttu-id="e25be-118">저장소 blob 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e25be-119">-CloudBlob</span></span>
<span data-ttu-id="e25be-120">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="e25be-121">**CloudBlob** 개체를 가져오려면 [Get-azurestorageblob](./Get-AzureStorageBlob.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-122">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="e25be-122">-Container</span></span>
<span data-ttu-id="e25be-123">저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e25be-124">-Context</span></span>
<span data-ttu-id="e25be-125">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-125">Specifies the storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e25be-126">-ExpiryTime</span></span>
<span data-ttu-id="e25be-127">공유 액세스 서명이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-127">Specifies when the shared access signature expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e25be-128">-FullUri</span></span>
<span data-ttu-id="e25be-129">이 cmdlet이 full blob URI 및 공유 액세스 서명 토큰을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e25be-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e25be-130">-IPAddressOrRange</span></span>
<span data-ttu-id="e25be-131">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e25be-132">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-132">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-133">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="e25be-133">-Permission</span></span>
<span data-ttu-id="e25be-134">저장소 blob에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-135">-정책</span><span class="sxs-lookup"><span data-stu-id="e25be-135">-Policy</span></span>
<span data-ttu-id="e25be-136">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-137">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="e25be-137">-Protocol</span></span>
<span data-ttu-id="e25be-138">요청에 허용 된 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e25be-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e25be-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e25be-140">HttpsOnly</span></span>
* <span data-ttu-id="e25be-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e25be-141">HttpsOrHttp</span></span>

<span data-ttu-id="e25be-142">기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e25be-143">-StartTime</span></span>
<span data-ttu-id="e25be-144">공유 액세스 서명이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25be-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25be-145">CommonParameters</span></span>
<span data-ttu-id="e25be-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25be-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25be-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25be-148">입력</span><span class="sxs-lookup"><span data-stu-id="e25be-148">INPUTS</span></span>

### <span data-ttu-id="e25be-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e25be-149">IStorageContext</span></span>

<span data-ttu-id="e25be-150">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25be-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e25be-151">출력</span><span class="sxs-lookup"><span data-stu-id="e25be-151">OUTPUTS</span></span>

### <span data-ttu-id="e25be-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e25be-152">System.String</span></span>

## <span data-ttu-id="e25be-153">상속자</span><span class="sxs-lookup"><span data-stu-id="e25be-153">NOTES</span></span>

## <span data-ttu-id="e25be-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e25be-154">RELATED LINKS</span></span>

[<span data-ttu-id="e25be-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e25be-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="e25be-156">새로운 AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e25be-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
