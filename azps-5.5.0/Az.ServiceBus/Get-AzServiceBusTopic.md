---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208149"
---
# <span data-ttu-id="49b2c-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="49b2c-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="49b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="49b2c-103">지정된 Service Bus 항목에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="49b2c-104">구문</span><span class="sxs-lookup"><span data-stu-id="49b2c-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b2c-105">설명</span><span class="sxs-lookup"><span data-stu-id="49b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="49b2c-106">**Get-AzServiceBusTopic** cmdlet은 지정된 Service Bus 네임스페이스에 대한 토픽 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="49b2c-107">예제</span><span class="sxs-lookup"><span data-stu-id="49b2c-107">EXAMPLES</span></span>

### <span data-ttu-id="49b2c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="49b2c-108">Example 1</span></span>
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

<span data-ttu-id="49b2c-109">지정된 Service Bus 네임스페이스에 대해 지정된 토픽에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="49b2c-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="49b2c-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="49b2c-111">주어진 Service Bus 네임스페이스에 대한 토픽 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="49b2c-112">기본적으로 100개 이상의 토픽이 반환됩니다. 100개가 넘는 토픽이 반환되는 경우 -MaxCount 매개 변수를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="49b2c-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="49b2c-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="49b2c-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="49b2c-114">주어진 Service Bus 네임스페이스에 대한 처음 150개 항목의 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="49b2c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b2c-115">PARAMETERS</span></span>

### <span data-ttu-id="49b2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b2c-116">-DefaultProfile</span></span>
<span data-ttu-id="49b2c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b2c-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="49b2c-118">-MaxCount</span></span>
<span data-ttu-id="49b2c-119">반환할 최대 토픽 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="49b2c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="49b2c-120">-Name</span></span>
<span data-ttu-id="49b2c-121">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="49b2c-121">Topic Name</span></span>

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

### <span data-ttu-id="49b2c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="49b2c-122">-Namespace</span></span>
<span data-ttu-id="49b2c-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="49b2c-123">Namespace Name</span></span>

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

### <span data-ttu-id="49b2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="49b2c-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="49b2c-125">The name of the resource group</span></span>

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

### <span data-ttu-id="49b2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b2c-126">CommonParameters</span></span>
<span data-ttu-id="49b2c-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49b2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b2c-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="49b2c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b2c-129">입력</span><span class="sxs-lookup"><span data-stu-id="49b2c-129">INPUTS</span></span>

### <span data-ttu-id="49b2c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="49b2c-130">System.String</span></span>

## <span data-ttu-id="49b2c-131">출력</span><span class="sxs-lookup"><span data-stu-id="49b2c-131">OUTPUTS</span></span>

### <span data-ttu-id="49b2c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="49b2c-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="49b2c-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49b2c-133">NOTES</span></span>

## <span data-ttu-id="49b2c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49b2c-134">RELATED LINKS</span></span>
