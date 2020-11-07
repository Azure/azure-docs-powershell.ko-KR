---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711008"
---
# <span data-ttu-id="bc837-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc837-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="bc837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc837-102">SYNOPSIS</span></span>
<span data-ttu-id="bc837-103">Azure storage 컨테이너에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc837-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc837-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc837-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc837-105">DESCRIPTION</span></span>
<span data-ttu-id="bc837-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet은 Azure storage 컨테이너에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="bc837-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc837-107">EXAMPLES</span></span>

### <span data-ttu-id="bc837-108">예제 1: 저장소 컨테이너에서 모든 권한을 사용 하 여 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="bc837-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="bc837-109">이 명령은 MyContainer 라는 저장소 컨테이너에 대 한 Policy06 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="bc837-110">변수</span><span class="sxs-lookup"><span data-stu-id="bc837-110">PARAMETERS</span></span>

### <span data-ttu-id="bc837-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bc837-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bc837-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bc837-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bc837-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bc837-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bc837-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bc837-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bc837-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bc837-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bc837-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="bc837-121">-Container</span></span>
<span data-ttu-id="bc837-122">Azure 저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bc837-123">-Context</span></span>
<span data-ttu-id="bc837-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bc837-125">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bc837-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bc837-126">-ExpiryTime</span></span>
<span data-ttu-id="bc837-127">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="bc837-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bc837-128">-NoExpiryTime</span></span>
<span data-ttu-id="bc837-129">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="bc837-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="bc837-130">-NoStartTime</span></span>
<span data-ttu-id="bc837-131">시작 시간을 $Null 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="bc837-132">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="bc837-132">-Permission</span></span>
<span data-ttu-id="bc837-133">저장 된 액세스 정책에서 저장소 컨테이너에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

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

### <span data-ttu-id="bc837-134">-정책</span><span class="sxs-lookup"><span data-stu-id="bc837-134">-Policy</span></span>
<span data-ttu-id="bc837-135">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bc837-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bc837-137">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bc837-138">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bc837-139">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bc837-140">-StartTime</span></span>
<span data-ttu-id="bc837-141">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="bc837-142">-확인</span><span class="sxs-lookup"><span data-stu-id="bc837-142">-Confirm</span></span>
<span data-ttu-id="bc837-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc837-144">-WhatIf</span></span>
<span data-ttu-id="bc837-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc837-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc837-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc837-147">CommonParameters</span></span>
<span data-ttu-id="bc837-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc837-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc837-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc837-150">입력</span><span class="sxs-lookup"><span data-stu-id="bc837-150">INPUTS</span></span>

### <span data-ttu-id="bc837-151">이름</span><span class="sxs-lookup"><span data-stu-id="bc837-151">String</span></span>

<span data-ttu-id="bc837-152">' Container ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="bc837-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc837-153">IStorageContext</span></span>

<span data-ttu-id="bc837-154">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc837-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="bc837-155">출력</span><span class="sxs-lookup"><span data-stu-id="bc837-155">OUTPUTS</span></span>

### <span data-ttu-id="bc837-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc837-156">System.String</span></span>

## <span data-ttu-id="bc837-157">상속자</span><span class="sxs-lookup"><span data-stu-id="bc837-157">NOTES</span></span>

## <span data-ttu-id="bc837-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc837-158">RELATED LINKS</span></span>

[<span data-ttu-id="bc837-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc837-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="bc837-160">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc837-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bc837-161">새로운 AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc837-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="bc837-162">제거-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc837-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
