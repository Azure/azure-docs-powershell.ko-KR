---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: ddccdb907dac89466a81be62e104202a3e59a672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533296"
---
# <span data-ttu-id="e82ff-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e82ff-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="e82ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e82ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e82ff-103">지정 된 Service Bus 항목에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e82ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e82ff-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e82ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e82ff-105">DESCRIPTION</span></span>
<span data-ttu-id="e82ff-106">**AzureRmServiceBusTopic** cmdlet은 지정 된 Service Bus 네임 스페이스에 대 한 항목 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e82ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e82ff-107">EXAMPLES</span></span>

### <span data-ttu-id="e82ff-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e82ff-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

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

<span data-ttu-id="e82ff-109">지정 된 Service Bus 네임 스페이스에 대 한 지정 된 항목의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="e82ff-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e82ff-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="e82ff-111">지정 된 Service Bus 네임 스페이스에 대 한 항목의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="e82ff-112">기본적으로 100 항목이 반환 되는 경우 100 항목이 더 있으면-MaxCount 매개 변수를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="e82ff-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="e82ff-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="e82ff-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="e82ff-114">지정 된 Service Bus 네임 스페이스에 대 한 첫 번째 150 항목의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="e82ff-115">변수</span><span class="sxs-lookup"><span data-stu-id="e82ff-115">PARAMETERS</span></span>

### <span data-ttu-id="e82ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82ff-116">-DefaultProfile</span></span>
<span data-ttu-id="e82ff-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e82ff-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e82ff-118">-MaxCount</span></span>
<span data-ttu-id="e82ff-119">반환할 항목의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="e82ff-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e82ff-120">-Name</span></span>
<span data-ttu-id="e82ff-121">주제 이름</span><span class="sxs-lookup"><span data-stu-id="e82ff-121">Topic Name</span></span>

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

### <span data-ttu-id="e82ff-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e82ff-122">-Namespace</span></span>
<span data-ttu-id="e82ff-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e82ff-123">Namespace Name</span></span>

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

### <span data-ttu-id="e82ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="e82ff-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-125">The name of the resource group</span></span>

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

### <span data-ttu-id="e82ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82ff-126">CommonParameters</span></span>
<span data-ttu-id="e82ff-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e82ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82ff-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82ff-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82ff-129">입력</span><span class="sxs-lookup"><span data-stu-id="e82ff-129">INPUTS</span></span>

### <span data-ttu-id="e82ff-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e82ff-130">System.String</span></span>

## <span data-ttu-id="e82ff-131">출력</span><span class="sxs-lookup"><span data-stu-id="e82ff-131">OUTPUTS</span></span>

### <span data-ttu-id="e82ff-132">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="e82ff-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e82ff-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e82ff-133">NOTES</span></span>

## <span data-ttu-id="e82ff-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e82ff-134">RELATED LINKS</span></span>
