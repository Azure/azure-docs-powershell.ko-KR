---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24a61f071e806588976f601df69aa66dbbafc164
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523912"
---
# <span data-ttu-id="da485-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="da485-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="da485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da485-102">SYNOPSIS</span></span>
<span data-ttu-id="da485-103">저장소 공유에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="da485-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da485-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da485-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da485-105">DESCRIPTION</span></span>
<span data-ttu-id="da485-106">**AzureStorageShareStoredAccessPolicy** Cmdlet은 Azure 저장소 공유에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="da485-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da485-107">EXAMPLES</span></span>

### <span data-ttu-id="da485-108">예제 1: Azure 저장소 공유에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="da485-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="da485-109">이 명령은 ContosoShare에서 일반 정책 이라는 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="da485-110">변수</span><span class="sxs-lookup"><span data-stu-id="da485-110">PARAMETERS</span></span>

### <span data-ttu-id="da485-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="da485-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="da485-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="da485-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="da485-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="da485-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="da485-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="da485-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="da485-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da485-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="da485-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="da485-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="da485-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da485-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="da485-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="da485-120">The default value is 10.</span></span>

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

### <span data-ttu-id="da485-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="da485-121">-Context</span></span>
<span data-ttu-id="da485-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="da485-123">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="da485-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da485-124">-PassThru</span></span>
<span data-ttu-id="da485-125">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da485-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="da485-126">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da485-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="da485-127">-정책</span><span class="sxs-lookup"><span data-stu-id="da485-127">-Policy</span></span>
<span data-ttu-id="da485-128">이 cmdlet이 제거 하는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da485-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="da485-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="da485-130">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="da485-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="da485-131">-ShareName</span></span>
<span data-ttu-id="da485-132">이 cmdlet이 정책을 제거할 저장소 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da485-133">-확인</span><span class="sxs-lookup"><span data-stu-id="da485-133">-Confirm</span></span>
<span data-ttu-id="da485-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da485-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da485-135">-WhatIf</span></span>
<span data-ttu-id="da485-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da485-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da485-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da485-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da485-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da485-138">CommonParameters</span></span>
<span data-ttu-id="da485-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da485-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da485-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da485-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da485-141">입력</span><span class="sxs-lookup"><span data-stu-id="da485-141">INPUTS</span></span>

## <span data-ttu-id="da485-142">출력</span><span class="sxs-lookup"><span data-stu-id="da485-142">OUTPUTS</span></span>

## <span data-ttu-id="da485-143">상속자</span><span class="sxs-lookup"><span data-stu-id="da485-143">NOTES</span></span>

## <span data-ttu-id="da485-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da485-144">RELATED LINKS</span></span>

[<span data-ttu-id="da485-145">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="da485-145">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="da485-146">새로운 AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="da485-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="da485-147">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="da485-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="da485-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="da485-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)