---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711489"
---
# <span data-ttu-id="00eba-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="00eba-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="00eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00eba-102">SYNOPSIS</span></span>
<span data-ttu-id="00eba-103">항목의 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00eba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00eba-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="00eba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00eba-105">DESCRIPTION</span></span>
<span data-ttu-id="00eba-106">**AzureRmServiceBusRule** cmdlet은 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="00eba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00eba-107">EXAMPLES</span></span>

### <span data-ttu-id="00eba-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00eba-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="00eba-109">**AzureRmServiceBusRule** cmdlet은 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="00eba-110">변수</span><span class="sxs-lookup"><span data-stu-id="00eba-110">PARAMETERS</span></span>

### <span data-ttu-id="00eba-111">-확인</span><span class="sxs-lookup"><span data-stu-id="00eba-111">-Confirm</span></span>
<span data-ttu-id="00eba-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00eba-113">-이름</span><span class="sxs-lookup"><span data-stu-id="00eba-113">-Name</span></span>
<span data-ttu-id="00eba-114">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="00eba-114">Rule Name</span></span>

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

### <span data-ttu-id="00eba-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="00eba-115">-Namespace</span></span>
<span data-ttu-id="00eba-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-116">Namespace Name.</span></span>

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

### <span data-ttu-id="00eba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00eba-117">-ResourceGroupName</span></span>
<span data-ttu-id="00eba-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-118">The name of the resource group</span></span>

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

### <span data-ttu-id="00eba-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="00eba-119">-SqlExpression</span></span>
<span data-ttu-id="00eba-120">Sql Fillter 식</span><span class="sxs-lookup"><span data-stu-id="00eba-120">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="00eba-121">-구독</span><span class="sxs-lookup"><span data-stu-id="00eba-121">-Subscription</span></span>
<span data-ttu-id="00eba-122">구독 이름</span><span class="sxs-lookup"><span data-stu-id="00eba-122">Subscription Name</span></span>

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

### <span data-ttu-id="00eba-123">-주제</span><span class="sxs-lookup"><span data-stu-id="00eba-123">-Topic</span></span>
<span data-ttu-id="00eba-124">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-124">Topic Name.</span></span>

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

### <span data-ttu-id="00eba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00eba-125">-WhatIf</span></span>
<span data-ttu-id="00eba-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00eba-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00eba-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="00eba-128">입력</span><span class="sxs-lookup"><span data-stu-id="00eba-128">INPUTS</span></span>

### <span data-ttu-id="00eba-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00eba-129">System.String</span></span>


## <span data-ttu-id="00eba-130">출력</span><span class="sxs-lookup"><span data-stu-id="00eba-130">OUTPUTS</span></span>

### <span data-ttu-id="00eba-131">ServiceBus.-\*.</span><span class="sxs-lookup"><span data-stu-id="00eba-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="00eba-132">상속자</span><span class="sxs-lookup"><span data-stu-id="00eba-132">NOTES</span></span>

## <span data-ttu-id="00eba-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00eba-133">RELATED LINKS</span></span>

