---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534664"
---
# <span data-ttu-id="cd52b-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="cd52b-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="cd52b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd52b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd52b-103">항목의 지정 된 구독에 대해 지정 된 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd52b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd52b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd52b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd52b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd52b-106">**AzureRmServiceBusRule** cmdlet은 항목의 지정 된 구독에서 지정 된 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="cd52b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd52b-107">EXAMPLES</span></span>

### <span data-ttu-id="cd52b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd52b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="cd52b-109">지정 된 구독에 대해 지정 된 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="cd52b-110">변수</span><span class="sxs-lookup"><span data-stu-id="cd52b-110">PARAMETERS</span></span>

### <span data-ttu-id="cd52b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd52b-111">-DefaultProfile</span></span>
<span data-ttu-id="cd52b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd52b-113">-이름</span><span class="sxs-lookup"><span data-stu-id="cd52b-113">-Name</span></span>
<span data-ttu-id="cd52b-114">규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd52b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cd52b-115">-Namespace</span></span>
<span data-ttu-id="cd52b-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="cd52b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd52b-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd52b-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-118">The name of the resource group</span></span>

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

### <span data-ttu-id="cd52b-119">-구독</span><span class="sxs-lookup"><span data-stu-id="cd52b-119">-Subscription</span></span>
<span data-ttu-id="cd52b-120">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd52b-121">-주제</span><span class="sxs-lookup"><span data-stu-id="cd52b-121">-Topic</span></span>
<span data-ttu-id="cd52b-122">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-122">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd52b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd52b-123">CommonParameters</span></span>
<span data-ttu-id="cd52b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd52b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd52b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd52b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd52b-126">입력</span><span class="sxs-lookup"><span data-stu-id="cd52b-126">INPUTS</span></span>

### <span data-ttu-id="cd52b-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd52b-127">System.String</span></span>

## <span data-ttu-id="cd52b-128">출력</span><span class="sxs-lookup"><span data-stu-id="cd52b-128">OUTPUTS</span></span>

### <span data-ttu-id="cd52b-129">ServiceBus. Ps규칙 특성을</span><span class="sxs-lookup"><span data-stu-id="cd52b-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="cd52b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="cd52b-130">NOTES</span></span>

## <span data-ttu-id="cd52b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd52b-131">RELATED LINKS</span></span>

