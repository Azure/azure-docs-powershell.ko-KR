---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308675"
---
# <span data-ttu-id="2b0ca-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2b0ca-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="2b0ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0ca-103">지정 된 큐 또는 항목 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0ca-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="2b0ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b0ca-104">SYNTAX</span></span>

### <span data-ttu-id="2b0ca-105">QueueCheckNameAvailabilitySet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b0ca-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b0ca-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2b0ca-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b0ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2b0ca-107">DESCRIPTION</span></span>
<span data-ttu-id="2b0ca-108">제공 된 큐 또는 항목 이름에 대 한 AzServiceBusNameAvailability Cmdlet 검사의 사용 가능 여부를 **테스트** 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0ca-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="2b0ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2b0ca-109">EXAMPLES</span></span>

### <span data-ttu-id="2b0ca-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b0ca-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="2b0ca-111">제공 된 $nameQueue 이름이 Availabile 경우 True를 반환 하 고 제공 된 $nameQueue 이름을 사용할 수 없는 경우 False를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0ca-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="2b0ca-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2b0ca-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="2b0ca-113">제공 된 $nameTopic 이름이 Availabile 경우 True를 반환 하 고 제공 된 $nameTopic 이름을 사용할 수 없는 경우 False를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0ca-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="2b0ca-114">변수</span><span class="sxs-lookup"><span data-stu-id="2b0ca-114">PARAMETERS</span></span>

### <span data-ttu-id="2b0ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b0ca-115">-DefaultProfile</span></span>
<span data-ttu-id="2b0ca-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b0ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b0ca-117">-이름</span><span class="sxs-lookup"><span data-stu-id="2b0ca-117">-Name</span></span>
<span data-ttu-id="2b0ca-118">이름 사용 가능성을 확인 하기 위한 큐 이름</span><span class="sxs-lookup"><span data-stu-id="2b0ca-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="2b0ca-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b0ca-119">-Namespace</span></span>
<span data-ttu-id="2b0ca-120">Servicebus 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="2b0ca-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="2b0ca-121">-큐</span><span class="sxs-lookup"><span data-stu-id="2b0ca-121">-Queue</span></span>
<span data-ttu-id="2b0ca-122">큐 이름에 대 한 이름 사용 가능성을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="2b0ca-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="2b0ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b0ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b0ca-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2b0ca-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2b0ca-125">-주제</span><span class="sxs-lookup"><span data-stu-id="2b0ca-125">-Topic</span></span>
<span data-ttu-id="2b0ca-126">주제 이름에 대 한 이름 사용 가능성을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="2b0ca-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="2b0ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0ca-127">CommonParameters</span></span>
<span data-ttu-id="2b0ca-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b0ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2b0ca-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b0ca-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0ca-130">입력</span><span class="sxs-lookup"><span data-stu-id="2b0ca-130">INPUTS</span></span>

### <span data-ttu-id="2b0ca-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b0ca-131">System.String</span></span>

## <span data-ttu-id="2b0ca-132">출력</span><span class="sxs-lookup"><span data-stu-id="2b0ca-132">OUTPUTS</span></span>

### <span data-ttu-id="2b0ca-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2b0ca-133">System.Boolean</span></span>

## <span data-ttu-id="2b0ca-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2b0ca-134">NOTES</span></span>

## <span data-ttu-id="2b0ca-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b0ca-135">RELATED LINKS</span></span>
