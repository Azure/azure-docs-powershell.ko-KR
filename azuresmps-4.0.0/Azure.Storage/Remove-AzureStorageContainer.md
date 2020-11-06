---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ccaa0ef1ce2a29851d6e90235e4564df3bde876
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523016"
---
# <span data-ttu-id="62adb-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="62adb-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="62adb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62adb-102">SYNOPSIS</span></span>
<span data-ttu-id="62adb-103">지정 된 저장소 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="62adb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62adb-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62adb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="62adb-105">DESCRIPTION</span></span>
<span data-ttu-id="62adb-106">**AzureStorageContainer** Cmdlet은 Azure에서 지정 된 저장소 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="62adb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="62adb-107">EXAMPLES</span></span>

### <span data-ttu-id="62adb-108">예제 1: 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="62adb-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="62adb-109">이 예제에서는 MyTestContainer 이라는 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="62adb-110">변수</span><span class="sxs-lookup"><span data-stu-id="62adb-110">PARAMETERS</span></span>

### <span data-ttu-id="62adb-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="62adb-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="62adb-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="62adb-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="62adb-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="62adb-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="62adb-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="62adb-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="62adb-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="62adb-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="62adb-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="62adb-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-120">The default value is 10.</span></span>

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

### <span data-ttu-id="62adb-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="62adb-121">-Context</span></span>
<span data-ttu-id="62adb-122">제거 하려는 컨테이너에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="62adb-123">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="62adb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="62adb-124">-Force</span></span>
<span data-ttu-id="62adb-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62adb-126">-이름</span><span class="sxs-lookup"><span data-stu-id="62adb-126">-Name</span></span>
<span data-ttu-id="62adb-127">제거할 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62adb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62adb-128">-PassThru</span></span>
<span data-ttu-id="62adb-129">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="62adb-130">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="62adb-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="62adb-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="62adb-132">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="62adb-133">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="62adb-134">-확인</span><span class="sxs-lookup"><span data-stu-id="62adb-134">-Confirm</span></span>
<span data-ttu-id="62adb-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62adb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62adb-136">-WhatIf</span></span>
<span data-ttu-id="62adb-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62adb-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62adb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62adb-139">CommonParameters</span></span>
<span data-ttu-id="62adb-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62adb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62adb-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62adb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62adb-142">입력</span><span class="sxs-lookup"><span data-stu-id="62adb-142">INPUTS</span></span>

## <span data-ttu-id="62adb-143">출력</span><span class="sxs-lookup"><span data-stu-id="62adb-143">OUTPUTS</span></span>

## <span data-ttu-id="62adb-144">상속자</span><span class="sxs-lookup"><span data-stu-id="62adb-144">NOTES</span></span>

## <span data-ttu-id="62adb-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62adb-145">RELATED LINKS</span></span>

[<span data-ttu-id="62adb-146">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="62adb-146">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="62adb-147">새로운 AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="62adb-147">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
