---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495477"
---
# <span data-ttu-id="1da53-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1da53-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="1da53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1da53-102">SYNOPSIS</span></span>
<span data-ttu-id="1da53-103">eventhub 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="1da53-104">구문</span><span class="sxs-lookup"><span data-stu-id="1da53-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1da53-105">설명</span><span class="sxs-lookup"><span data-stu-id="1da53-105">DESCRIPTION</span></span>
<span data-ttu-id="1da53-106">지정된 IotHub와 연결된 Eventhub에 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="1da53-107">예제</span><span class="sxs-lookup"><span data-stu-id="1da53-107">EXAMPLES</span></span>

### <span data-ttu-id="1da53-108">예제 1: eventhub 원격 분석에 소비자 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="1da53-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="1da53-109">"myiothub"라는 iothub의 원격 분석 이벤트에 대한 eventhub에 "myconsumergroup"이라는 새 소비자group을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="1da53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1da53-110">PARAMETERS</span></span>

### <span data-ttu-id="1da53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da53-111">-DefaultProfile</span></span>
<span data-ttu-id="1da53-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1da53-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1da53-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="1da53-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="1da53-114">추가하려는 EventHub ConsumerGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1da53-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1da53-115">-Name</span></span>
<span data-ttu-id="1da53-116">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1da53-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1da53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da53-117">-ResourceGroupName</span></span>
<span data-ttu-id="1da53-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="1da53-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1da53-119">-Confirm</span></span>
<span data-ttu-id="1da53-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1da53-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1da53-121">-WhatIf</span></span>
<span data-ttu-id="1da53-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1da53-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1da53-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1da53-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da53-124">CommonParameters</span></span>
<span data-ttu-id="1da53-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1da53-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da53-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1da53-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da53-127">입력</span><span class="sxs-lookup"><span data-stu-id="1da53-127">INPUTS</span></span>

### <span data-ttu-id="1da53-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1da53-128">System.String</span></span>

## <span data-ttu-id="1da53-129">출력</span><span class="sxs-lookup"><span data-stu-id="1da53-129">OUTPUTS</span></span>

### <span data-ttu-id="1da53-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1da53-130">System.String</span></span>

## <span data-ttu-id="1da53-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1da53-131">NOTES</span></span>

## <span data-ttu-id="1da53-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1da53-132">RELATED LINKS</span></span>
