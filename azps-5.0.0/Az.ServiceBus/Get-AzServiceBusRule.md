---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226662"
---
# <span data-ttu-id="9e4c9-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9e4c9-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="9e4c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4c9-103">항목의 지정 된 구독에서 기존 규칙의 정의를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="9e4c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e4c9-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e4c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="9e4c9-106">**AzServiceBusRule** cmdlet은 항목의 지정 된 구독에서 지정 된 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="9e4c9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e4c9-107">EXAMPLES</span></span>

### <span data-ttu-id="9e4c9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e4c9-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="9e4c9-109">지정 된 구독에 대해 지정 된 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="9e4c9-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e4c9-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="9e4c9-111">지정 된 구독에 대 한 규칙 설명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="9e4c9-112">기본적으로 100 규칙이 반환 되 고, 반환 되는 100 규칙이 더 있으면-MaxCount 매개 변수를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="9e4c9-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="9e4c9-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="9e4c9-114">지정 된 구독에 대 한 첫 번째 150 규칙 설명의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="9e4c9-115">변수</span><span class="sxs-lookup"><span data-stu-id="9e4c9-115">PARAMETERS</span></span>

### <span data-ttu-id="9e4c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4c9-116">-DefaultProfile</span></span>
<span data-ttu-id="9e4c9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4c9-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9e4c9-118">-MaxCount</span></span>
<span data-ttu-id="9e4c9-119">반환할 최대 규칙 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c9-120">-이름</span><span class="sxs-lookup"><span data-stu-id="9e4c9-120">-Name</span></span>
<span data-ttu-id="9e4c9-121">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="9e4c9-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c9-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e4c9-122">-Namespace</span></span>
<span data-ttu-id="9e4c9-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="9e4c9-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e4c9-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-125">The name of the resource group</span></span>

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

### <span data-ttu-id="9e4c9-126">-구독</span><span class="sxs-lookup"><span data-stu-id="9e4c9-126">-Subscription</span></span>
<span data-ttu-id="9e4c9-127">구독 이름</span><span class="sxs-lookup"><span data-stu-id="9e4c9-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c9-128">-주제</span><span class="sxs-lookup"><span data-stu-id="9e4c9-128">-Topic</span></span>
<span data-ttu-id="9e4c9-129">주제 이름</span><span class="sxs-lookup"><span data-stu-id="9e4c9-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4c9-130">CommonParameters</span></span>
<span data-ttu-id="9e4c9-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e4c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4c9-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4c9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4c9-133">입력</span><span class="sxs-lookup"><span data-stu-id="9e4c9-133">INPUTS</span></span>

### <span data-ttu-id="9e4c9-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e4c9-134">System.String</span></span>

## <span data-ttu-id="9e4c9-135">출력</span><span class="sxs-lookup"><span data-stu-id="9e4c9-135">OUTPUTS</span></span>

### <span data-ttu-id="9e4c9-136">ServiceBus. Ps규칙 특성을</span><span class="sxs-lookup"><span data-stu-id="9e4c9-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9e4c9-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9e4c9-137">NOTES</span></span>

## <span data-ttu-id="9e4c9-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e4c9-138">RELATED LINKS</span></span>
