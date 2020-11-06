---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523548"
---
# <span data-ttu-id="446c6-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="446c6-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="446c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="446c6-102">SYNOPSIS</span></span>
<span data-ttu-id="446c6-103">파일 공유를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-103">Deletes a file share.</span></span>

## <span data-ttu-id="446c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="446c6-104">SYNTAX</span></span>

### <span data-ttu-id="446c6-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="446c6-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446c6-106">공유</span><span class="sxs-lookup"><span data-stu-id="446c6-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="446c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="446c6-107">DESCRIPTION</span></span>
<span data-ttu-id="446c6-108">**제거-AzureStorageShare** cmdlet은 파일 공유를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="446c6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="446c6-109">EXAMPLES</span></span>

### <span data-ttu-id="446c6-110">예제 1: 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="446c6-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="446c6-111">이 명령은 ContosoShare06 이라는 이름의 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="446c6-112">변수</span><span class="sxs-lookup"><span data-stu-id="446c6-112">PARAMETERS</span></span>

### <span data-ttu-id="446c6-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="446c6-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="446c6-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="446c6-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="446c6-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="446c6-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="446c6-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="446c6-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="446c6-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="446c6-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="446c6-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="446c6-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-122">The default value is 10.</span></span>

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

### <span data-ttu-id="446c6-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="446c6-123">-Context</span></span>
<span data-ttu-id="446c6-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="446c6-125">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="446c6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="446c6-126">-Force</span></span>
<span data-ttu-id="446c6-127">공유 및 모든 콘텐츠를 강제로 제거</span><span class="sxs-lookup"><span data-stu-id="446c6-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="446c6-128">-이름</span><span class="sxs-lookup"><span data-stu-id="446c6-128">-Name</span></span>
<span data-ttu-id="446c6-129">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="446c6-130">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="446c6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="446c6-131">-PassThru</span></span>
<span data-ttu-id="446c6-132">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="446c6-133">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="446c6-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="446c6-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="446c6-135">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="446c6-136">-공유</span><span class="sxs-lookup"><span data-stu-id="446c6-136">-Share</span></span>
<span data-ttu-id="446c6-137">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="446c6-138">이 cmdlet은이 매개 변수에서 지정 하는 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="446c6-139">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="446c6-140">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-140">This object contains the storage context.</span></span>
<span data-ttu-id="446c6-141">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="446c6-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="446c6-142">-확인</span><span class="sxs-lookup"><span data-stu-id="446c6-142">-Confirm</span></span>
<span data-ttu-id="446c6-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446c6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="446c6-144">-WhatIf</span></span>
<span data-ttu-id="446c6-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="446c6-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446c6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446c6-147">CommonParameters</span></span>
<span data-ttu-id="446c6-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="446c6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446c6-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="446c6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446c6-150">입력</span><span class="sxs-lookup"><span data-stu-id="446c6-150">INPUTS</span></span>

## <span data-ttu-id="446c6-151">출력</span><span class="sxs-lookup"><span data-stu-id="446c6-151">OUTPUTS</span></span>

## <span data-ttu-id="446c6-152">상속자</span><span class="sxs-lookup"><span data-stu-id="446c6-152">NOTES</span></span>

## <span data-ttu-id="446c6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="446c6-153">RELATED LINKS</span></span>

[<span data-ttu-id="446c6-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="446c6-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="446c6-155">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="446c6-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="446c6-156">새로운 AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="446c6-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
