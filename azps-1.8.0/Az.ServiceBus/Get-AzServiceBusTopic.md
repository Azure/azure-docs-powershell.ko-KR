---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: ff3ab640de435898f665f0994a63f904decda5cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699193"
---
# <span data-ttu-id="0ae59-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0ae59-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="0ae59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae59-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae59-103">지정 된 Service Bus 항목에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="0ae59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ae59-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ae59-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ae59-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae59-106">**AzServiceBusTopic** cmdlet은 지정 된 Service Bus 네임 스페이스에 대 한 항목 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0ae59-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ae59-107">EXAMPLES</span></span>

### <span data-ttu-id="0ae59-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ae59-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="0ae59-109">지정 된 Service Bus 네임 스페이스에 대 한 지정 된 항목의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="0ae59-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="0ae59-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="0ae59-111">지정 된 Service Bus 네임 스페이스에 대 한 항목의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="0ae59-112">기본적으로 100 항목이 반환 되는 경우 100 항목이 더 있으면-MaxCount 매개 변수를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ae59-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="0ae59-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="0ae59-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="0ae59-114">지정 된 Service Bus 네임 스페이스에 대 한 첫 번째 150 항목의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="0ae59-115">변수</span><span class="sxs-lookup"><span data-stu-id="0ae59-115">PARAMETERS</span></span>

### <span data-ttu-id="0ae59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae59-116">-DefaultProfile</span></span>
<span data-ttu-id="0ae59-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae59-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0ae59-118">-MaxCount</span></span>
<span data-ttu-id="0ae59-119">반환할 항목의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="0ae59-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0ae59-120">-Name</span></span>
<span data-ttu-id="0ae59-121">주제 이름</span><span class="sxs-lookup"><span data-stu-id="0ae59-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae59-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0ae59-122">-Namespace</span></span>
<span data-ttu-id="0ae59-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="0ae59-123">Namespace Name</span></span>

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

### <span data-ttu-id="0ae59-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae59-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ae59-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-125">The name of the resource group</span></span>

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

### <span data-ttu-id="0ae59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae59-126">CommonParameters</span></span>
<span data-ttu-id="0ae59-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae59-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae59-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae59-129">입력</span><span class="sxs-lookup"><span data-stu-id="0ae59-129">INPUTS</span></span>

### <span data-ttu-id="0ae59-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ae59-130">System.String</span></span>

## <span data-ttu-id="0ae59-131">출력</span><span class="sxs-lookup"><span data-stu-id="0ae59-131">OUTPUTS</span></span>

### <span data-ttu-id="0ae59-132">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="0ae59-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="0ae59-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0ae59-133">NOTES</span></span>

## <span data-ttu-id="0ae59-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae59-134">RELATED LINKS</span></span>
