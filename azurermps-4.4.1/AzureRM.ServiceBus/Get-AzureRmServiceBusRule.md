---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: e09e4f19a63eef1cd4b87760239d4456afee70fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527296"
---
# <span data-ttu-id="1f6f0-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="1f6f0-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="1f6f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6f0-103">항목의 지정 된 구독에 대해 지정 된 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f6f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f6f0-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f6f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6f0-106">**AzureRmServiceBusRule** cmdlet은 항목의 지정 된 구독에서 지정 된 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="1f6f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1f6f0-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6f0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f6f0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="1f6f0-109">지정 된 구독에 대해 지정 된 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="1f6f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="1f6f0-110">PARAMETERS</span></span>

### <span data-ttu-id="1f6f0-111">-이름</span><span class="sxs-lookup"><span data-stu-id="1f6f0-111">-Name</span></span>
<span data-ttu-id="1f6f0-112">규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-112">Rule Name.</span></span>

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

### <span data-ttu-id="1f6f0-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f6f0-113">-Namespace</span></span>
<span data-ttu-id="1f6f0-114">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-114">Namespace Name.</span></span>

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

### <span data-ttu-id="1f6f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="1f6f0-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-116">The name of the resource group</span></span>

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

### <span data-ttu-id="1f6f0-117">-구독</span><span class="sxs-lookup"><span data-stu-id="1f6f0-117">-Subscription</span></span>
<span data-ttu-id="1f6f0-118">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-118">Subscription Name.</span></span>

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

### <span data-ttu-id="1f6f0-119">-주제</span><span class="sxs-lookup"><span data-stu-id="1f6f0-119">-Topic</span></span>
<span data-ttu-id="1f6f0-120">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-120">Topic Name.</span></span>

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

### <span data-ttu-id="1f6f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6f0-121">-DefaultProfile</span></span>
<span data-ttu-id="1f6f0-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6f0-123">CommonParameters</span></span>
<span data-ttu-id="1f6f0-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6f0-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6f0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6f0-126">입력</span><span class="sxs-lookup"><span data-stu-id="1f6f0-126">INPUTS</span></span>

### <span data-ttu-id="1f6f0-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f6f0-127">System.String</span></span>

## <span data-ttu-id="1f6f0-128">출력</span><span class="sxs-lookup"><span data-stu-id="1f6f0-128">OUTPUTS</span></span>

### <span data-ttu-id="1f6f0-129">ServiceBus.-\*.</span><span class="sxs-lookup"><span data-stu-id="1f6f0-129">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="1f6f0-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1f6f0-130">NOTES</span></span>

## <span data-ttu-id="1f6f0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f6f0-131">RELATED LINKS</span></span>

