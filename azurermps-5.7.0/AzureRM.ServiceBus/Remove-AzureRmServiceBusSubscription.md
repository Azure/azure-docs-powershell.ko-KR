---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 80b3a5ce4cb38222993e69181519a864c578cf67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534652"
---
# <span data-ttu-id="ff8a7-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ff8a7-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="ff8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff8a7-103">지정 된 Service Bus 네임 스페이스에서 주제에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff8a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff8a7-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff8a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ff8a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ff8a7-106">**AzureRmServiceBusSubscription** cmdlet은 지정 된 Service Bus 네임 스페이스의 주제에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ff8a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ff8a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ff8a7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff8a7-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="ff8a7-109">`SB-TopicSubscription-Example1` `SB-Topic_exampl1` 지정 된 Service Bus 네임 스페이스의 주제에 대 한 구독을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="ff8a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="ff8a7-110">PARAMETERS</span></span>

### <span data-ttu-id="ff8a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff8a7-111">-DefaultProfile</span></span>
<span data-ttu-id="ff8a7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff8a7-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ff8a7-113">-Name</span></span>
<span data-ttu-id="ff8a7-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff8a7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff8a7-115">-Namespace</span></span>
<span data-ttu-id="ff8a7-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ff8a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff8a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff8a7-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-118">The name of the resource group</span></span>

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

### <span data-ttu-id="ff8a7-119">-주제</span><span class="sxs-lookup"><span data-stu-id="ff8a7-119">-Topic</span></span>
<span data-ttu-id="ff8a7-120">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff8a7-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ff8a7-121">-Confirm</span></span>
<span data-ttu-id="ff8a7-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff8a7-123">-WhatIf</span></span>
<span data-ttu-id="ff8a7-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff8a7-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff8a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff8a7-126">CommonParameters</span></span>
<span data-ttu-id="ff8a7-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff8a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff8a7-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff8a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff8a7-129">입력</span><span class="sxs-lookup"><span data-stu-id="ff8a7-129">INPUTS</span></span>

### <span data-ttu-id="ff8a7-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff8a7-130">-ResourceGroup</span></span>
 <span data-ttu-id="ff8a7-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff8a7-131">System.String</span></span>

### <span data-ttu-id="ff8a7-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ff8a7-132">-NamespaceName</span></span>
 <span data-ttu-id="ff8a7-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff8a7-133">System.String</span></span>

### <span data-ttu-id="ff8a7-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ff8a7-134">-TopicName</span></span>
 <span data-ttu-id="ff8a7-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff8a7-135">System.String</span></span>

### <span data-ttu-id="ff8a7-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ff8a7-136">-SubscriptionName</span></span>
 <span data-ttu-id="ff8a7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff8a7-137">System.String</span></span>

## <span data-ttu-id="ff8a7-138">출력</span><span class="sxs-lookup"><span data-stu-id="ff8a7-138">OUTPUTS</span></span>

### <span data-ttu-id="ff8a7-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ff8a7-139">System.Boolean</span></span>

## <span data-ttu-id="ff8a7-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ff8a7-140">NOTES</span></span>

## <span data-ttu-id="ff8a7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff8a7-141">RELATED LINKS</span></span>

