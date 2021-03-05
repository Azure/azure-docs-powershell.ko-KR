---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 1e563126bb57986bed752184340808991f7e2a00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974848"
---
# <span data-ttu-id="7d726-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7d726-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="7d726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d726-102">SYNOPSIS</span></span>
<span data-ttu-id="7d726-103">eventhub consumergroup을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="7d726-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d726-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d726-105">설명</span><span class="sxs-lookup"><span data-stu-id="7d726-105">DESCRIPTION</span></span>
<span data-ttu-id="7d726-106">eventhub consumergroup을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="7d726-107">예제</span><span class="sxs-lookup"><span data-stu-id="7d726-107">EXAMPLES</span></span>

### <span data-ttu-id="7d726-108">예제 1 원격 분석 조차도에서 eventhub consumergroup 제거</span><span class="sxs-lookup"><span data-stu-id="7d726-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="7d726-109">"myiothub"라는 IotHub에서 myconsumergroup이라는 consumergroup을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7d726-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d726-110">PARAMETERS</span></span>

### <span data-ttu-id="7d726-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d726-111">-DefaultProfile</span></span>
<span data-ttu-id="7d726-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7d726-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d726-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="7d726-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="7d726-114">EventHub ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d726-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7d726-115">-Name</span></span>
<span data-ttu-id="7d726-116">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="7d726-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="7d726-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d726-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d726-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7d726-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7d726-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7d726-119">-Confirm</span></span>
<span data-ttu-id="7d726-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d726-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d726-121">-WhatIf</span></span>
<span data-ttu-id="7d726-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d726-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d726-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d726-124">CommonParameters</span></span>
<span data-ttu-id="7d726-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d726-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d726-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d726-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d726-127">입력</span><span class="sxs-lookup"><span data-stu-id="7d726-127">INPUTS</span></span>

### <span data-ttu-id="7d726-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7d726-128">System.String</span></span>

## <span data-ttu-id="7d726-129">출력</span><span class="sxs-lookup"><span data-stu-id="7d726-129">OUTPUTS</span></span>

### <span data-ttu-id="7d726-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7d726-130">System.String</span></span>

## <span data-ttu-id="7d726-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d726-131">NOTES</span></span>

## <span data-ttu-id="7d726-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d726-132">RELATED LINKS</span></span>
