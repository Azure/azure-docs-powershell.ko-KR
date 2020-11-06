---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: a41ddb9ee845bce0687448d0745904b9cec9ba05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531649"
---
# <span data-ttu-id="25ea8-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="25ea8-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="25ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="25ea8-103">지정 된 리소스 그룹에서 Service Bus 네임 스페이스 또는 큐 또는 주제의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25ea8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25ea8-104">SYNTAX</span></span>

### <span data-ttu-id="25ea8-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="25ea8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25ea8-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="25ea8-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25ea8-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="25ea8-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25ea8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="25ea8-108">DESCRIPTION</span></span>
<span data-ttu-id="25ea8-109">**AzureRmServiceBusAuthorizationRule** cmdlet은 지정 된 리소스 그룹에 대 한 Service Bus 네임 스페이스 또는 큐 또는 항목의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="25ea8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="25ea8-110">EXAMPLES</span></span>

### <span data-ttu-id="25ea8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="25ea8-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="25ea8-112">`SBAuthoRule1`지정 된 리소스 그룹에서 네임 스페이스의 권한 부여 규칙을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="25ea8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="25ea8-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="25ea8-114">`SBAuthoRule1`지정 된 리소스 그룹에서 큐의 권한 부여 규칙을 제거 `SBQueue` 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="25ea8-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="25ea8-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="25ea8-116">지정 된 리소스 그룹의 주제에 대 한 권한 부여 규칙을 제거 `SBAuthoRule1` `SBTopic` 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="25ea8-117">변수</span><span class="sxs-lookup"><span data-stu-id="25ea8-117">PARAMETERS</span></span>

### <span data-ttu-id="25ea8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ea8-118">-DefaultProfile</span></span>
<span data-ttu-id="25ea8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25ea8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="25ea8-120">-Force</span></span>
<span data-ttu-id="25ea8-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25ea8-122">-InputObject</span></span>
<span data-ttu-id="25ea8-123">ServiceBus AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="25ea8-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-124">-이름</span><span class="sxs-lookup"><span data-stu-id="25ea8-124">-Name</span></span>
<span data-ttu-id="25ea8-125">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="25ea8-125">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25ea8-126">-Namespace</span></span>
<span data-ttu-id="25ea8-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="25ea8-127">Namespace Name</span></span>

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

### <span data-ttu-id="25ea8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ea8-128">-PassThru</span></span>
<span data-ttu-id="25ea8-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25ea8-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-131">-큐</span><span class="sxs-lookup"><span data-stu-id="25ea8-131">-Queue</span></span>
<span data-ttu-id="25ea8-132">큐 이름</span><span class="sxs-lookup"><span data-stu-id="25ea8-132">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ea8-133">-ResourceGroupName</span></span>
<span data-ttu-id="25ea8-134">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="25ea8-134">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-135">-주제</span><span class="sxs-lookup"><span data-stu-id="25ea8-135">-Topic</span></span>
<span data-ttu-id="25ea8-136">주제 이름</span><span class="sxs-lookup"><span data-stu-id="25ea8-136">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ea8-137">-확인</span><span class="sxs-lookup"><span data-stu-id="25ea8-137">-Confirm</span></span>
<span data-ttu-id="25ea8-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ea8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ea8-139">-WhatIf</span></span>
<span data-ttu-id="25ea8-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ea8-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ea8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ea8-142">CommonParameters</span></span>
<span data-ttu-id="25ea8-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25ea8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="25ea8-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ea8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ea8-145">입력</span><span class="sxs-lookup"><span data-stu-id="25ea8-145">INPUTS</span></span>

### <span data-ttu-id="25ea8-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="25ea8-146">System.String</span></span>
<span data-ttu-id="25ea8-147">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="25ea8-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="25ea8-148">출력</span><span class="sxs-lookup"><span data-stu-id="25ea8-148">OUTPUTS</span></span>

### <span data-ttu-id="25ea8-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="25ea8-149">System.Boolean</span></span>


## <span data-ttu-id="25ea8-150">상속자</span><span class="sxs-lookup"><span data-stu-id="25ea8-150">NOTES</span></span>

## <span data-ttu-id="25ea8-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25ea8-151">RELATED LINKS</span></span>
