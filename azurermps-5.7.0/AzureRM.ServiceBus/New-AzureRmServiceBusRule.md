---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703219"
---
# <span data-ttu-id="491ac-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="491ac-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="491ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="491ac-102">SYNOPSIS</span></span>
<span data-ttu-id="491ac-103">항목의 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="491ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="491ac-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="491ac-105">DESCRIPTION</span></span>
<span data-ttu-id="491ac-106">**AzureRmServiceBusRule** cmdlet은 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="491ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="491ac-107">EXAMPLES</span></span>

### <span data-ttu-id="491ac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="491ac-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="491ac-109">New-AzureRmServiceBusRule cmdlet은 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="491ac-110">변수</span><span class="sxs-lookup"><span data-stu-id="491ac-110">PARAMETERS</span></span>

### <span data-ttu-id="491ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491ac-111">-DefaultProfile</span></span>
<span data-ttu-id="491ac-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="491ac-113">-이름</span><span class="sxs-lookup"><span data-stu-id="491ac-113">-Name</span></span>
<span data-ttu-id="491ac-114">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="491ac-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491ac-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="491ac-115">-Namespace</span></span>
<span data-ttu-id="491ac-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-116">Namespace Name.</span></span>

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

### <span data-ttu-id="491ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="491ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="491ac-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-118">The name of the resource group</span></span>

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

### <span data-ttu-id="491ac-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="491ac-119">-SqlExpression</span></span>
<span data-ttu-id="491ac-120">Sql Fillter 식</span><span class="sxs-lookup"><span data-stu-id="491ac-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491ac-121">-구독</span><span class="sxs-lookup"><span data-stu-id="491ac-121">-Subscription</span></span>
<span data-ttu-id="491ac-122">구독 이름</span><span class="sxs-lookup"><span data-stu-id="491ac-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="491ac-123">-주제</span><span class="sxs-lookup"><span data-stu-id="491ac-123">-Topic</span></span>
<span data-ttu-id="491ac-124">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-124">Topic Name.</span></span>

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

### <span data-ttu-id="491ac-125">-확인</span><span class="sxs-lookup"><span data-stu-id="491ac-125">-Confirm</span></span>
<span data-ttu-id="491ac-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491ac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491ac-127">-WhatIf</span></span>
<span data-ttu-id="491ac-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="491ac-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491ac-130">CommonParameters</span></span>
<span data-ttu-id="491ac-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="491ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491ac-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491ac-133">입력</span><span class="sxs-lookup"><span data-stu-id="491ac-133">INPUTS</span></span>

### <span data-ttu-id="491ac-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="491ac-134">System.String</span></span>

## <span data-ttu-id="491ac-135">출력</span><span class="sxs-lookup"><span data-stu-id="491ac-135">OUTPUTS</span></span>

### <span data-ttu-id="491ac-136">ServiceBus. Ps규칙 특성을</span><span class="sxs-lookup"><span data-stu-id="491ac-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="491ac-137">상속자</span><span class="sxs-lookup"><span data-stu-id="491ac-137">NOTES</span></span>

## <span data-ttu-id="491ac-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="491ac-138">RELATED LINKS</span></span>

