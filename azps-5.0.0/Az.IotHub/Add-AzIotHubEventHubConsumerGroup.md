---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217779"
---
# <span data-ttu-id="7433d-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7433d-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="7433d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7433d-102">SYNOPSIS</span></span>
<span data-ttu-id="7433d-103">Eventhub 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="7433d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7433d-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7433d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7433d-105">DESCRIPTION</span></span>
<span data-ttu-id="7433d-106">지정 된 IotHub와 관련 된 Eventhub에 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="7433d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7433d-107">EXAMPLES</span></span>

### <span data-ttu-id="7433d-108">예제 1: 원격 분석 eventhub에 소비자 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="7433d-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="7433d-109">"Myiothub" 이라는 iothub의 원격 분석 이벤트에 대 한 eventhub에 "myconsumergroup" 라는 새 consumergroup를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="7433d-110">변수</span><span class="sxs-lookup"><span data-stu-id="7433d-110">PARAMETERS</span></span>

### <span data-ttu-id="7433d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7433d-111">-DefaultProfile</span></span>
<span data-ttu-id="7433d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7433d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7433d-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="7433d-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="7433d-114">추가 하려는 EventHub ConsumerGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="7433d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7433d-115">-Name</span></span>
<span data-ttu-id="7433d-116">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="7433d-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7433d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7433d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7433d-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="7433d-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7433d-119">-Confirm</span></span>
<span data-ttu-id="7433d-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7433d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7433d-121">-WhatIf</span></span>
<span data-ttu-id="7433d-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7433d-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7433d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7433d-124">CommonParameters</span></span>
<span data-ttu-id="7433d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7433d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7433d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7433d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7433d-127">입력</span><span class="sxs-lookup"><span data-stu-id="7433d-127">INPUTS</span></span>

### <span data-ttu-id="7433d-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7433d-128">System.String</span></span>

## <span data-ttu-id="7433d-129">출력</span><span class="sxs-lookup"><span data-stu-id="7433d-129">OUTPUTS</span></span>

### <span data-ttu-id="7433d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7433d-130">System.String</span></span>

## <span data-ttu-id="7433d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7433d-131">NOTES</span></span>

## <span data-ttu-id="7433d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7433d-132">RELATED LINKS</span></span>
