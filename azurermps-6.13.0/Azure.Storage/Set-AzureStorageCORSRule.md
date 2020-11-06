---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
ms.openlocfilehash: 21293b8262a10c5710ed132413658c3c1cfbd254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526428"
---
# <span data-ttu-id="cec27-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="cec27-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="cec27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cec27-102">SYNOPSIS</span></span>
<span data-ttu-id="cec27-103">저장소 서비스 유형에 대 한 CORS 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cec27-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cec27-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cec27-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cec27-105">DESCRIPTION</span></span>
<span data-ttu-id="cec27-106">**AzureStorageCORSRule** Cmdlet은 Azure 저장소 서비스 유형에 대 한 CORS (교차 원본 리소스 공유) 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="cec27-107">이 cmdlet에 대 한 저장소 서비스의 유형은 Blob, 테이블, 큐 및 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="cec27-108">이 cmdlet은 기존 규칙을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="cec27-109">현재 규칙을 보려면 Get-AzureStorageCORSRule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="cec27-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cec27-110">EXAMPLES</span></span>

### <span data-ttu-id="cec27-111">예제 1: blob 서비스에 CORS 규칙 할당</span><span class="sxs-lookup"><span data-stu-id="cec27-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="cec27-112">첫 번째 명령은 $CorsRules 변수에 규칙 배열을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="cec27-113">이 명령은이 코드 블록의 여러 줄에 걸쳐 표준 확장을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="cec27-114">두 번째 명령은 $CorsRules의 규칙을 Blob 서비스 유형에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="cec27-115">예제 2: blob 서비스에 대 한 CORS 규칙의 속성 변경</span><span class="sxs-lookup"><span data-stu-id="cec27-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="cec27-116">첫 번째 명령은 **AzureStorageCORSRule** cmdlet을 사용 하 여 Blob 형식에 대 한 현재 CORS 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="cec27-117">명령은 $CorsRules 배열 변수에 규칙을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="cec27-118">두 번째 및 세 번째 명령은 $CorsRules의 첫 번째 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="cec27-119">마지막 명령은 $CorsRules의 규칙을 Blob 서비스 형식에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="cec27-120">수정 된 규칙은 현재 CORS 규칙을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="cec27-121">변수</span><span class="sxs-lookup"><span data-stu-id="cec27-121">PARAMETERS</span></span>

### <span data-ttu-id="cec27-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cec27-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cec27-123">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cec27-124">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cec27-125">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cec27-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cec27-127">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cec27-128">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cec27-129">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cec27-130">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cec27-131">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-131">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-132">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cec27-132">-Context</span></span>
<span data-ttu-id="cec27-133">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cec27-134">컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="cec27-135">-CorsRules</span></span>
<span data-ttu-id="cec27-136">CORS 규칙의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="cec27-137">Get-AzureStorageCORSRule cmdlet을 사용 하 여 기존 규칙을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec27-138">-DefaultProfile</span></span>
<span data-ttu-id="cec27-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cec27-140">-PassThru</span></span>
<span data-ttu-id="cec27-141">이 cmdlet이 작업의 성공 여부를 반영 하는 Boolean을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="cec27-142">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cec27-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cec27-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cec27-144">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-144">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="cec27-145">-ServiceType</span></span>
<span data-ttu-id="cec27-146">이 cmdlet이 규칙을 할당 하는 Azure 저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="cec27-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cec27-148">블</span><span class="sxs-lookup"><span data-stu-id="cec27-148">Blob</span></span> 
- <span data-ttu-id="cec27-149">테이블로</span><span class="sxs-lookup"><span data-stu-id="cec27-149">Table</span></span> 
- <span data-ttu-id="cec27-150">전담팀</span><span class="sxs-lookup"><span data-stu-id="cec27-150">Queue</span></span> 
- <span data-ttu-id="cec27-151">파일</span><span class="sxs-lookup"><span data-stu-id="cec27-151">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec27-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec27-152">CommonParameters</span></span>
<span data-ttu-id="cec27-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec27-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec27-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec27-155">입력</span><span class="sxs-lookup"><span data-stu-id="cec27-155">INPUTS</span></span>

### <span data-ttu-id="cec27-156">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cec27-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cec27-157">출력</span><span class="sxs-lookup"><span data-stu-id="cec27-157">OUTPUTS</span></span>

### <span data-ttu-id="cec27-158">WindowsAzure. ResourceModel를 PSCorsRule로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec27-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="cec27-159">상속자</span><span class="sxs-lookup"><span data-stu-id="cec27-159">NOTES</span></span>

## <span data-ttu-id="cec27-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cec27-160">RELATED LINKS</span></span>

[<span data-ttu-id="cec27-161">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="cec27-161">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="cec27-162">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cec27-162">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cec27-163">제거-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="cec27-163">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


