---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59e7652d8ca3b2e26246ba4f8924f6a6b9d48f96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527944"
---
# <span data-ttu-id="a183e-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a183e-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="a183e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a183e-102">SYNOPSIS</span></span>
<span data-ttu-id="a183e-103">Eventhub consumergroup를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a183e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a183e-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a183e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a183e-105">DESCRIPTION</span></span>
<span data-ttu-id="a183e-106">Eventhub consumergroup를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="a183e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a183e-107">EXAMPLES</span></span>

### <span data-ttu-id="a183e-108">예제 1 원격 분석 eventhub에서 eventhub consumergroup 제거</span><span class="sxs-lookup"><span data-stu-id="a183e-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="a183e-109">"Myiothub" IotHub에서 이름이 myconsumergroup 인 consumergroup을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a183e-110">변수</span><span class="sxs-lookup"><span data-stu-id="a183e-110">PARAMETERS</span></span>

### <span data-ttu-id="a183e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a183e-111">-DefaultProfile</span></span>
<span data-ttu-id="a183e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a183e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a183e-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="a183e-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="a183e-114">EventHub ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="a183e-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="a183e-115">-EventHubEndpointName</span></span>
<span data-ttu-id="a183e-116">EventHub 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="a183e-117">사용할 수 있는 값 이벤트, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="a183e-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="a183e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a183e-118">-Name</span></span>
<span data-ttu-id="a183e-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="a183e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a183e-120">-ResourceGroupName</span></span>
<span data-ttu-id="a183e-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a183e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a183e-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a183e-122">-Confirm</span></span>
<span data-ttu-id="a183e-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a183e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a183e-124">-WhatIf</span></span>
<span data-ttu-id="a183e-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a183e-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a183e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a183e-127">CommonParameters</span></span>
<span data-ttu-id="a183e-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a183e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a183e-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a183e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a183e-130">입력</span><span class="sxs-lookup"><span data-stu-id="a183e-130">INPUTS</span></span>

### <span data-ttu-id="a183e-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a183e-131">System.String</span></span>

## <span data-ttu-id="a183e-132">출력</span><span class="sxs-lookup"><span data-stu-id="a183e-132">OUTPUTS</span></span>

### <span data-ttu-id="a183e-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a183e-133">System.String</span></span>

## <span data-ttu-id="a183e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a183e-134">NOTES</span></span>

## <span data-ttu-id="a183e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a183e-135">RELATED LINKS</span></span>
