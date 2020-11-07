---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: d321892ef2ebbe8e50908a5d519f1990ebb875ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689709"
---
# <span data-ttu-id="050f5-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="050f5-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="050f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050f5-102">SYNOPSIS</span></span>
<span data-ttu-id="050f5-103">Eventhub consumergroup를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="050f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="050f5-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="050f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="050f5-105">DESCRIPTION</span></span>
<span data-ttu-id="050f5-106">Eventhub consumergroup를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="050f5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="050f5-107">EXAMPLES</span></span>

### <span data-ttu-id="050f5-108">예제 1 원격 분석 eventhub에서 eventhub consumergroup 제거</span><span class="sxs-lookup"><span data-stu-id="050f5-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="050f5-109">"Myiothub" IotHub에서 이름이 myconsumergroup 인 consumergroup을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="050f5-110">변수</span><span class="sxs-lookup"><span data-stu-id="050f5-110">PARAMETERS</span></span>

### <span data-ttu-id="050f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050f5-111">-DefaultProfile</span></span>
<span data-ttu-id="050f5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="050f5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="050f5-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="050f5-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="050f5-114">EventHub ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050f5-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="050f5-115">-EventHubEndpointName</span></span>
<span data-ttu-id="050f5-116">EventHub 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="050f5-117">사용할 수 있는 값 이벤트, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="050f5-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="050f5-118">-이름</span><span class="sxs-lookup"><span data-stu-id="050f5-118">-Name</span></span>
<span data-ttu-id="050f5-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="050f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="050f5-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="050f5-121">Resource Group Name</span></span>

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

### <span data-ttu-id="050f5-122">-확인</span><span class="sxs-lookup"><span data-stu-id="050f5-122">-Confirm</span></span>
<span data-ttu-id="050f5-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050f5-124">-WhatIf</span></span>
<span data-ttu-id="050f5-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="050f5-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050f5-127">CommonParameters</span></span>
<span data-ttu-id="050f5-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="050f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050f5-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="050f5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050f5-130">입력</span><span class="sxs-lookup"><span data-stu-id="050f5-130">INPUTS</span></span>

### <span data-ttu-id="050f5-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="050f5-131">System.String</span></span>

## <span data-ttu-id="050f5-132">출력</span><span class="sxs-lookup"><span data-stu-id="050f5-132">OUTPUTS</span></span>

### <span data-ttu-id="050f5-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="050f5-133">System.String</span></span>

## <span data-ttu-id="050f5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="050f5-134">NOTES</span></span>

## <span data-ttu-id="050f5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="050f5-135">RELATED LINKS</span></span>
