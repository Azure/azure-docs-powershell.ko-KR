---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689763"
---
# <span data-ttu-id="dfcdd-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="dfcdd-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="dfcdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfcdd-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcdd-103">Eventhub 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="dfcdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfcdd-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcdd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfcdd-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcdd-106">지정 된 IotHub와 관련 된 Eventhub에 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="dfcdd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfcdd-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcdd-108">예제 1: 원격 분석 eventhub에 소비자 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="dfcdd-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="dfcdd-109">"Myiothub" 이라는 iothub의 원격 분석 이벤트에 대 한 eventhub에 "myconsumergroup" 라는 새 consumergroup를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="dfcdd-110">변수</span><span class="sxs-lookup"><span data-stu-id="dfcdd-110">PARAMETERS</span></span>

### <span data-ttu-id="dfcdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcdd-111">-DefaultProfile</span></span>
<span data-ttu-id="dfcdd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dfcdd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfcdd-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcdd-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="dfcdd-114">추가 하려는 EventHub ConsumerGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="dfcdd-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="dfcdd-115">-EventHubEndpointName</span></span>
<span data-ttu-id="dfcdd-116">EventHub 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="dfcdd-117">사용할 수 있는 값 이벤트, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="dfcdd-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="dfcdd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="dfcdd-118">-Name</span></span>
<span data-ttu-id="dfcdd-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="dfcdd-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dfcdd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcdd-120">-ResourceGroupName</span></span>
<span data-ttu-id="dfcdd-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="dfcdd-122">-확인</span><span class="sxs-lookup"><span data-stu-id="dfcdd-122">-Confirm</span></span>
<span data-ttu-id="dfcdd-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcdd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcdd-124">-WhatIf</span></span>
<span data-ttu-id="dfcdd-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcdd-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcdd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcdd-127">CommonParameters</span></span>
<span data-ttu-id="dfcdd-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfcdd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcdd-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcdd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcdd-130">입력</span><span class="sxs-lookup"><span data-stu-id="dfcdd-130">INPUTS</span></span>

### <span data-ttu-id="dfcdd-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfcdd-131">System.String</span></span>

## <span data-ttu-id="dfcdd-132">출력</span><span class="sxs-lookup"><span data-stu-id="dfcdd-132">OUTPUTS</span></span>

### <span data-ttu-id="dfcdd-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfcdd-133">System.String</span></span>

## <span data-ttu-id="dfcdd-134">상속자</span><span class="sxs-lookup"><span data-stu-id="dfcdd-134">NOTES</span></span>

## <span data-ttu-id="dfcdd-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfcdd-135">RELATED LINKS</span></span>
