---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529140"
---
# <span data-ttu-id="f1d1f-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="f1d1f-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="f1d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d1f-103">지정 된 Service Bus 네임 스페이스에서 주제에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1d1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1d1f-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f1d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d1f-106">**AzureRmServiceBusSubscription** cmdlet은 지정 된 Service Bus 네임 스페이스의 주제에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f1d1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f1d1f-107">EXAMPLES</span></span>

### <span data-ttu-id="f1d1f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1d1f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="f1d1f-109">`SB-TopicSubscription-Example1` `SB-Topic_exampl1` 지정 된 Service Bus 네임 스페이스의 주제에 대 한 구독을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f1d1f-110">변수</span><span class="sxs-lookup"><span data-stu-id="f1d1f-110">PARAMETERS</span></span>

### <span data-ttu-id="f1d1f-111">-확인</span><span class="sxs-lookup"><span data-stu-id="f1d1f-111">-Confirm</span></span>
<span data-ttu-id="f1d1f-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d1f-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d1f-113">-WhatIf</span></span>
<span data-ttu-id="f1d1f-114">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d1f-115">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d1f-116">-DefaultProfile</span></span>
<span data-ttu-id="f1d1f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d1f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f1d1f-118">-Name</span></span>
<span data-ttu-id="f1d1f-119">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d1f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1d1f-120">-Namespace</span></span>
<span data-ttu-id="f1d1f-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1d1f-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d1f-124">-주제</span><span class="sxs-lookup"><span data-stu-id="f1d1f-124">-Topic</span></span>
<span data-ttu-id="f1d1f-125">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d1f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d1f-126">CommonParameters</span></span>
<span data-ttu-id="f1d1f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d1f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d1f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d1f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d1f-129">입력</span><span class="sxs-lookup"><span data-stu-id="f1d1f-129">INPUTS</span></span>

### <span data-ttu-id="f1d1f-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1d1f-130">-ResourceGroup</span></span>
 <span data-ttu-id="f1d1f-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1d1f-131">System.String</span></span>

### <span data-ttu-id="f1d1f-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f1d1f-132">-NamespaceName</span></span>
 <span data-ttu-id="f1d1f-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1d1f-133">System.String</span></span>

### <span data-ttu-id="f1d1f-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="f1d1f-134">-TopicName</span></span>
 <span data-ttu-id="f1d1f-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1d1f-135">System.String</span></span>

### <span data-ttu-id="f1d1f-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f1d1f-136">-SubscriptionName</span></span>
 <span data-ttu-id="f1d1f-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1d1f-137">System.String</span></span>

## <span data-ttu-id="f1d1f-138">출력</span><span class="sxs-lookup"><span data-stu-id="f1d1f-138">OUTPUTS</span></span>

### <span data-ttu-id="f1d1f-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f1d1f-139">System.Boolean</span></span>

## <span data-ttu-id="f1d1f-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f1d1f-140">NOTES</span></span>

## <span data-ttu-id="f1d1f-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1d1f-141">RELATED LINKS</span></span>

