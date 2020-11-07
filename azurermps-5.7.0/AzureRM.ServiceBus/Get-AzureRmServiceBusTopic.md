---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 56f41802687938bf7575049eadc59ab7b049ac2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703991"
---
# <span data-ttu-id="7f6c6-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7f6c6-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="7f6c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6c6-103">지정 된 Service Bus 항목에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f6c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f6c6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f6c6-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6c6-106">**AzureRmServiceBusTopic** cmdlet은 지정 된 Service Bus 네임 스페이스에 대 한 항목 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7f6c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7f6c6-107">EXAMPLES</span></span>

### <span data-ttu-id="7f6c6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f6c6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM
```
<span data-ttu-id="7f6c6-109">지정 된 Service Bus 네임 스페이스에 대 한 지정 된 항목의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="7f6c6-110">변수</span><span class="sxs-lookup"><span data-stu-id="7f6c6-110">PARAMETERS</span></span>

### <span data-ttu-id="7f6c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6c6-111">-DefaultProfile</span></span>
<span data-ttu-id="7f6c6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c6-113">-이름</span><span class="sxs-lookup"><span data-stu-id="7f6c6-113">-Name</span></span>
<span data-ttu-id="7f6c6-114">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-114">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c6-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7f6c6-115">-Namespace</span></span>
<span data-ttu-id="7f6c6-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f6c6-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6c6-119">CommonParameters</span></span>
<span data-ttu-id="7f6c6-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6c6-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6c6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6c6-122">입력</span><span class="sxs-lookup"><span data-stu-id="7f6c6-122">INPUTS</span></span>

### <span data-ttu-id="7f6c6-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f6c6-123">-ResourceGroup</span></span>
 <span data-ttu-id="7f6c6-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7f6c6-124">System.String</span></span>
 

### <span data-ttu-id="7f6c6-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7f6c6-125">-NamespaceName</span></span>
 <span data-ttu-id="7f6c6-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7f6c6-126">System.String</span></span>
 

### <span data-ttu-id="7f6c6-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7f6c6-127">-TopicName</span></span>
 <span data-ttu-id="7f6c6-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7f6c6-128">System.String</span></span>

## <span data-ttu-id="7f6c6-129">출력</span><span class="sxs-lookup"><span data-stu-id="7f6c6-129">OUTPUTS</span></span>

### <span data-ttu-id="7f6c6-130">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="7f6c6-130">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="7f6c6-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7f6c6-131">NOTES</span></span>

## <span data-ttu-id="7f6c6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f6c6-132">RELATED LINKS</span></span>

