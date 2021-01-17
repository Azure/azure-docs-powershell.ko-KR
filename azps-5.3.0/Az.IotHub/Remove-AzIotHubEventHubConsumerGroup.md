---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386695"
---
# <span data-ttu-id="48515-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="48515-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="48515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48515-102">SYNOPSIS</span></span>
<span data-ttu-id="48515-103">eventhub 소비자group을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="48515-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="48515-104">구문</span><span class="sxs-lookup"><span data-stu-id="48515-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48515-105">설명</span><span class="sxs-lookup"><span data-stu-id="48515-105">DESCRIPTION</span></span>
<span data-ttu-id="48515-106">eventhub 소비자group을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="48515-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="48515-107">예제</span><span class="sxs-lookup"><span data-stu-id="48515-107">EXAMPLES</span></span>

### <span data-ttu-id="48515-108">예제 1 원격 분석 eventhub에서 eventhub 소비자group 제거</span><span class="sxs-lookup"><span data-stu-id="48515-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="48515-109">"myiothub"라는 IotHub에서 myconsumergroup이라는 consumergroup을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="48515-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="48515-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48515-110">PARAMETERS</span></span>

### <span data-ttu-id="48515-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48515-111">-DefaultProfile</span></span>
<span data-ttu-id="48515-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="48515-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48515-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="48515-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="48515-114">EventHub ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48515-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="48515-115">-Name</span><span class="sxs-lookup"><span data-stu-id="48515-115">-Name</span></span>
<span data-ttu-id="48515-116">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="48515-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="48515-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48515-117">-ResourceGroupName</span></span>
<span data-ttu-id="48515-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="48515-118">Resource Group Name</span></span>

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

### <span data-ttu-id="48515-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48515-119">-Confirm</span></span>
<span data-ttu-id="48515-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48515-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48515-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48515-121">-WhatIf</span></span>
<span data-ttu-id="48515-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="48515-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48515-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48515-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48515-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48515-124">CommonParameters</span></span>
<span data-ttu-id="48515-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48515-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48515-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="48515-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48515-127">입력</span><span class="sxs-lookup"><span data-stu-id="48515-127">INPUTS</span></span>

### <span data-ttu-id="48515-128">System.String</span><span class="sxs-lookup"><span data-stu-id="48515-128">System.String</span></span>

## <span data-ttu-id="48515-129">출력</span><span class="sxs-lookup"><span data-stu-id="48515-129">OUTPUTS</span></span>

### <span data-ttu-id="48515-130">System.String</span><span class="sxs-lookup"><span data-stu-id="48515-130">System.String</span></span>

## <span data-ttu-id="48515-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48515-131">NOTES</span></span>

## <span data-ttu-id="48515-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48515-132">RELATED LINKS</span></span>
