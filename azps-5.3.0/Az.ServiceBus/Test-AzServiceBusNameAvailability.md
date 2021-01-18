---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494812"
---
# <span data-ttu-id="896b0-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="896b0-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="896b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="896b0-102">SYNOPSIS</span></span>
<span data-ttu-id="896b0-103">주어진 큐 또는 토픽 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="896b0-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="896b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="896b0-104">SYNTAX</span></span>

### <span data-ttu-id="896b0-105">QueueCheckNameAvailabilitySet(기본값)</span><span class="sxs-lookup"><span data-stu-id="896b0-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="896b0-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="896b0-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="896b0-107">설명</span><span class="sxs-lookup"><span data-stu-id="896b0-107">DESCRIPTION</span></span>
<span data-ttu-id="896b0-108">**Test-AzServiceBusNameAvailability** Cmdlet은 제공된 큐 또는 토픽 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="896b0-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="896b0-109">예제</span><span class="sxs-lookup"><span data-stu-id="896b0-109">EXAMPLES</span></span>

### <span data-ttu-id="896b0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="896b0-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="896b0-111">제공된 $nameQueue 이름이 사용 가능한 경우 True를 반환하거나 제공된 $nameQueue 이름을 사용할 수 없는 경우 False를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="896b0-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="896b0-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="896b0-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="896b0-113">제공된 $nameTopic 이름이 사용 가능한 경우 True를 반환하거나 제공된 $nameTopic 사용할 수 없는 경우 False를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="896b0-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="896b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="896b0-114">PARAMETERS</span></span>

### <span data-ttu-id="896b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896b0-115">-DefaultProfile</span></span>
<span data-ttu-id="896b0-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="896b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="896b0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="896b0-117">-Name</span></span>
<span data-ttu-id="896b0-118">이름 가용성을 확인할 큐 이름</span><span class="sxs-lookup"><span data-stu-id="896b0-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="896b0-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="896b0-119">-Namespace</span></span>
<span data-ttu-id="896b0-120">Servicebus 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="896b0-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="896b0-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="896b0-121">-Queue</span></span>
<span data-ttu-id="896b0-122">큐 이름에 대한 이름 가용성을 확인</span><span class="sxs-lookup"><span data-stu-id="896b0-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="896b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="896b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="896b0-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="896b0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="896b0-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="896b0-125">-Topic</span></span>
<span data-ttu-id="896b0-126">토픽 이름에 대한 이름 가용성을 확인</span><span class="sxs-lookup"><span data-stu-id="896b0-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="896b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896b0-127">CommonParameters</span></span>
<span data-ttu-id="896b0-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="896b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="896b0-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="896b0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896b0-130">입력</span><span class="sxs-lookup"><span data-stu-id="896b0-130">INPUTS</span></span>

### <span data-ttu-id="896b0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="896b0-131">System.String</span></span>

## <span data-ttu-id="896b0-132">출력</span><span class="sxs-lookup"><span data-stu-id="896b0-132">OUTPUTS</span></span>

### <span data-ttu-id="896b0-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="896b0-133">System.Boolean</span></span>

## <span data-ttu-id="896b0-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="896b0-134">NOTES</span></span>

## <span data-ttu-id="896b0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="896b0-135">RELATED LINKS</span></span>
