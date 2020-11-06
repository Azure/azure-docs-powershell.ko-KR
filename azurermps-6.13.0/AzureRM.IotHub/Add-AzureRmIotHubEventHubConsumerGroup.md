---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 00342fddd1a8755f22f925e25595ec36b9326c09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530287"
---
# <span data-ttu-id="88234-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="88234-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="88234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88234-102">SYNOPSIS</span></span>
<span data-ttu-id="88234-103">Eventhub 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88234-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88234-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88234-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88234-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88234-105">DESCRIPTION</span></span>
<span data-ttu-id="88234-106">지정 된 IotHub와 관련 된 Eventhub에 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88234-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="88234-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88234-107">EXAMPLES</span></span>

### <span data-ttu-id="88234-108">예제 1: 원격 분석 eventhub에 소비자 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="88234-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="88234-109">"Myiothub" 이라는 iothub의 원격 분석 이벤트에 대 한 eventhub에 "myconsumergroup" 라는 새 consumergroup를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="88234-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="88234-110">예제 2: 운영 모니터링 eventhub에 소비자 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="88234-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="88234-111">"Myiothub" iothub의 운영 모니터링 이벤트에 대 한 eventhub에 "myconsumergroup" 라는 새 consumergroup를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="88234-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="88234-112">변수</span><span class="sxs-lookup"><span data-stu-id="88234-112">PARAMETERS</span></span>

### <span data-ttu-id="88234-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88234-113">-DefaultProfile</span></span>
<span data-ttu-id="88234-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88234-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88234-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="88234-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="88234-116">추가 하려는 EventHub ConsumerGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88234-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88234-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="88234-117">-EventHubEndpointName</span></span>
<span data-ttu-id="88234-118">EventHub 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88234-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="88234-119">사용할 수 있는 값 이벤트, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="88234-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88234-120">-이름</span><span class="sxs-lookup"><span data-stu-id="88234-120">-Name</span></span>
<span data-ttu-id="88234-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="88234-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88234-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88234-122">-ResourceGroupName</span></span>
<span data-ttu-id="88234-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88234-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="88234-124">-확인</span><span class="sxs-lookup"><span data-stu-id="88234-124">-Confirm</span></span>
<span data-ttu-id="88234-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88234-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88234-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88234-126">-WhatIf</span></span>
<span data-ttu-id="88234-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88234-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88234-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88234-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88234-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88234-129">CommonParameters</span></span>
<span data-ttu-id="88234-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88234-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88234-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88234-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88234-132">입력</span><span class="sxs-lookup"><span data-stu-id="88234-132">INPUTS</span></span>

### <span data-ttu-id="88234-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88234-133">System.String</span></span>

## <span data-ttu-id="88234-134">출력</span><span class="sxs-lookup"><span data-stu-id="88234-134">OUTPUTS</span></span>

### <span data-ttu-id="88234-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88234-135">System.String</span></span>

## <span data-ttu-id="88234-136">상속자</span><span class="sxs-lookup"><span data-stu-id="88234-136">NOTES</span></span>

## <span data-ttu-id="88234-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88234-137">RELATED LINKS</span></span>
