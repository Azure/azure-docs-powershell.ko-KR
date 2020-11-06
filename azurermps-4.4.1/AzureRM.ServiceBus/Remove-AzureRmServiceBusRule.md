---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 287a0b82c9236841b613ac52a7a07ccf8adb4811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529139"
---
# <span data-ttu-id="9b6e2-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9b6e2-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="9b6e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6e2-103">지정 된 구독에 대 한 speficied 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b6e2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b6e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6e2-106">**AzureRmServiceBusRule** cmdlet은 지정 된 항목의 구독에 대 한 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="9b6e2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b6e2-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6e2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b6e2-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="9b6e2-109">`SBRule`지정 된 항목의 구독에 대 한 규칙을 제거 `SBSubscription` `SBTopic` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="9b6e2-110">변수</span><span class="sxs-lookup"><span data-stu-id="9b6e2-110">PARAMETERS</span></span>

### <span data-ttu-id="9b6e2-111">-확인</span><span class="sxs-lookup"><span data-stu-id="9b6e2-111">-Confirm</span></span>
<span data-ttu-id="9b6e2-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e2-113">-이름</span><span class="sxs-lookup"><span data-stu-id="9b6e2-113">-Name</span></span>
<span data-ttu-id="9b6e2-114">규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-114">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b6e2-115">-Namespace</span></span>
<span data-ttu-id="9b6e2-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-116">Namespace Name.</span></span>

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

### <span data-ttu-id="9b6e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b6e2-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-118">The name of the resource group</span></span>

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

### <span data-ttu-id="9b6e2-119">-구독</span><span class="sxs-lookup"><span data-stu-id="9b6e2-119">-Subscription</span></span>
<span data-ttu-id="9b6e2-120">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-120">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e2-121">-주제</span><span class="sxs-lookup"><span data-stu-id="9b6e2-121">-Topic</span></span>
<span data-ttu-id="9b6e2-122">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-122">Topic Name.</span></span>

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

### <span data-ttu-id="9b6e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6e2-123">-WhatIf</span></span>
<span data-ttu-id="9b6e2-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6e2-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6e2-126">-DefaultProfile</span></span>
<span data-ttu-id="9b6e2-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6e2-128">-Force</span><span class="sxs-lookup"><span data-stu-id="9b6e2-128">-Force</span></span>
<span data-ttu-id="9b6e2-129">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-129">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b6e2-130">-PassThru</span></span>
<span data-ttu-id="9b6e2-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="9b6e2-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6e2-132">CommonParameters</span></span>
<span data-ttu-id="9b6e2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b6e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6e2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6e2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6e2-135">입력</span><span class="sxs-lookup"><span data-stu-id="9b6e2-135">INPUTS</span></span>

### <span data-ttu-id="9b6e2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b6e2-136">System.String</span></span>

## <span data-ttu-id="9b6e2-137">출력</span><span class="sxs-lookup"><span data-stu-id="9b6e2-137">OUTPUTS</span></span>

### <span data-ttu-id="9b6e2-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9b6e2-138">System.Boolean</span></span>

## <span data-ttu-id="9b6e2-139">상속자</span><span class="sxs-lookup"><span data-stu-id="9b6e2-139">NOTES</span></span>

## <span data-ttu-id="9b6e2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b6e2-140">RELATED LINKS</span></span>

