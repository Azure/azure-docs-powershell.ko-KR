---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190713"
---
# <span data-ttu-id="6283f-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6283f-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="6283f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6283f-102">SYNOPSIS</span></span>
<span data-ttu-id="6283f-103">Storage 서비스 유형에 대한 CORS 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="6283f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6283f-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6283f-105">설명</span><span class="sxs-lookup"><span data-stu-id="6283f-105">DESCRIPTION</span></span>
<span data-ttu-id="6283f-106">**Set-AzStorageCORSRule** cmdlet은 Azure Storage 서비스 형식에 대한 CORS(원본 간 리소스 공유) 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="6283f-107">이 cmdlet에 대한 저장소 서비스의 유형은 Blob, 테이블, 큐 및 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="6283f-108">이 cmdlet은 기존 규칙을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="6283f-109">현재 규칙을 표시하기 위해 Get-AzStorageCORSRule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="6283f-110">예제</span><span class="sxs-lookup"><span data-stu-id="6283f-110">EXAMPLES</span></span>

### <span data-ttu-id="6283f-111">예제 1: BLOB 서비스에 CORS 규칙 할당</span><span class="sxs-lookup"><span data-stu-id="6283f-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="6283f-112">첫 번째 명령은 규칙 배열을 변수에 $CorsRules 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="6283f-113">이 명령은 이 코드 블록의 여러 줄에 대해 표준 확장을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="6283f-114">두 번째 명령은 Blob service $CorsRules 규칙에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="6283f-115">예제 2: Blob service에 대한 CORS 규칙의 속성 변경</span><span class="sxs-lookup"><span data-stu-id="6283f-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="6283f-116">첫 번째 명령은 **Get-AzStorageCORSRule** cmdlet을 사용하여 Blob 형식에 대한 현재 CORS 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="6283f-117">이 명령은 배열 변수에 $CorsRules 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="6283f-118">두 번째 및 세 번째 명령은 명령의 첫 번째 규칙을 $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="6283f-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="6283f-119">마지막 명령은 Blob service $CorsRules 규칙에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="6283f-120">수정된 규칙은 현재 CORS 규칙을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="6283f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6283f-121">PARAMETERS</span></span>

### <span data-ttu-id="6283f-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6283f-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6283f-123">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6283f-124">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6283f-125">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6283f-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6283f-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6283f-127">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6283f-128">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6283f-129">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6283f-130">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6283f-131">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-131">The default value is 10.</span></span>

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

### <span data-ttu-id="6283f-132">-Context</span><span class="sxs-lookup"><span data-stu-id="6283f-132">-Context</span></span>
<span data-ttu-id="6283f-133">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6283f-134">컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6283f-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="6283f-135">-CorsRules</span></span>
<span data-ttu-id="6283f-136">CORS 규칙의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="6283f-137">Get-AzStorageCORSRule cmdlet을 사용하여 기존 규칙을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="6283f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6283f-138">-DefaultProfile</span></span>
<span data-ttu-id="6283f-139">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6283f-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6283f-140">-PassThru</span></span>
<span data-ttu-id="6283f-141">이 cmdlet은 작업의 성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="6283f-142">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6283f-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6283f-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6283f-144">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-144">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6283f-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6283f-145">-ServiceType</span></span>
<span data-ttu-id="6283f-146">이 cmdlet에서 규칙을 할당하는 Azure Storage 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="6283f-147">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="6283f-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6283f-148">Blob</span><span class="sxs-lookup"><span data-stu-id="6283f-148">Blob</span></span> 
- <span data-ttu-id="6283f-149">표</span><span class="sxs-lookup"><span data-stu-id="6283f-149">Table</span></span> 
- <span data-ttu-id="6283f-150">큐</span><span class="sxs-lookup"><span data-stu-id="6283f-150">Queue</span></span> 
- <span data-ttu-id="6283f-151">파일</span><span class="sxs-lookup"><span data-stu-id="6283f-151">File</span></span>

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

### <span data-ttu-id="6283f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6283f-152">CommonParameters</span></span>
<span data-ttu-id="6283f-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6283f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6283f-154">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6283f-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6283f-155">입력</span><span class="sxs-lookup"><span data-stu-id="6283f-155">INPUTS</span></span>

### <span data-ttu-id="6283f-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6283f-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6283f-157">출력</span><span class="sxs-lookup"><span data-stu-id="6283f-157">OUTPUTS</span></span>

### <span data-ttu-id="6283f-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="6283f-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="6283f-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6283f-159">NOTES</span></span>

## <span data-ttu-id="6283f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6283f-160">RELATED LINKS</span></span>

[<span data-ttu-id="6283f-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6283f-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="6283f-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6283f-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6283f-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6283f-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


