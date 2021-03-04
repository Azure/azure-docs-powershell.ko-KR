---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: b97acb269ee38dc937c5deffb0b3e054b0222c4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961568"
---
# <span data-ttu-id="ff076-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ff076-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="ff076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff076-102">SYNOPSIS</span></span>
<span data-ttu-id="ff076-103">주어진 큐 또는 토픽 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="ff076-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff076-104">SYNTAX</span></span>

### <span data-ttu-id="ff076-105">QueueCheckNameAvailabilitySet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff076-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff076-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ff076-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff076-107">설명</span><span class="sxs-lookup"><span data-stu-id="ff076-107">DESCRIPTION</span></span>
<span data-ttu-id="ff076-108">**Test-AzServiceBusNameAvailability** Cmdlet에서 제공된 큐 이름 또는 토픽의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="ff076-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="ff076-109">예제</span><span class="sxs-lookup"><span data-stu-id="ff076-109">EXAMPLES</span></span>

### <span data-ttu-id="ff076-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff076-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="ff076-111">제공된 $nameQueue 이름이 Availabile인 경우 True를 반환하거나 제공된 $nameQueue 이름을 사용할 수 없는 경우 False를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="ff076-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ff076-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="ff076-113">제공된 $nameTopic 이름이 Availabile인 경우 True를 반환하거나 제공된 $nameTopic 이름을 사용할 수 없는 경우 False를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="ff076-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff076-114">PARAMETERS</span></span>

### <span data-ttu-id="ff076-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff076-115">-DefaultProfile</span></span>
<span data-ttu-id="ff076-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff076-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ff076-117">-Name</span></span>
<span data-ttu-id="ff076-118">이름 가용성을 검사하는 큐 이름</span><span class="sxs-lookup"><span data-stu-id="ff076-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="ff076-119">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ff076-119">-Namespace</span></span>
<span data-ttu-id="ff076-120">Servicebus 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ff076-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff076-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="ff076-121">-Queue</span></span>
<span data-ttu-id="ff076-122">큐 이름에 대한 이름 가용성을 확인</span><span class="sxs-lookup"><span data-stu-id="ff076-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff076-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff076-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff076-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ff076-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff076-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="ff076-125">-Topic</span></span>
<span data-ttu-id="ff076-126">토픽 이름에 대한 이름 가용성을 확인</span><span class="sxs-lookup"><span data-stu-id="ff076-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff076-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff076-127">CommonParameters</span></span>
<span data-ttu-id="ff076-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ff076-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ff076-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff076-130">입력</span><span class="sxs-lookup"><span data-stu-id="ff076-130">INPUTS</span></span>

### <span data-ttu-id="ff076-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ff076-131">System.String</span></span>

## <span data-ttu-id="ff076-132">출력</span><span class="sxs-lookup"><span data-stu-id="ff076-132">OUTPUTS</span></span>

### <span data-ttu-id="ff076-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff076-133">System.Boolean</span></span>

## <span data-ttu-id="ff076-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff076-134">NOTES</span></span>

## <span data-ttu-id="ff076-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff076-135">RELATED LINKS</span></span>
