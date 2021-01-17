---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494857"
---
# <span data-ttu-id="957fd-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="957fd-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="957fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957fd-102">SYNOPSIS</span></span>
<span data-ttu-id="957fd-103">지정된 리소스 그룹에서 Service Bus 네임스페이스 또는 큐 또는 토픽의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="957fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="957fd-104">SYNTAX</span></span>

### <span data-ttu-id="957fd-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="957fd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="957fd-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="957fd-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="957fd-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="957fd-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="957fd-108">설명</span><span class="sxs-lookup"><span data-stu-id="957fd-108">DESCRIPTION</span></span>
<span data-ttu-id="957fd-109">**Remove-AzServiceBusAuthorizationRule** cmdlet은 지정된 리소스 그룹에 대한 Service Bus 네임스페이스 또는 큐 또는 토픽의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="957fd-110">예제</span><span class="sxs-lookup"><span data-stu-id="957fd-110">EXAMPLES</span></span>

### <span data-ttu-id="957fd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="957fd-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="957fd-112">지정된 리소스 그룹에서 네임스페이스의 `SBAuthoRule1` `SB-Example1` 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="957fd-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="957fd-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="957fd-114">지정된 리소스 `SBAuthoRule1` 그룹에서 `SBQueue` 큐의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="957fd-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="957fd-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="957fd-116">지정된 리소스 `SBAuthoRule1` 그룹에서 `SBTopic` 토픽의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="957fd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="957fd-117">PARAMETERS</span></span>

### <span data-ttu-id="957fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957fd-118">-DefaultProfile</span></span>
<span data-ttu-id="957fd-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="957fd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="957fd-120">-Force</span></span>
<span data-ttu-id="957fd-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="957fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="957fd-122">-InputObject</span></span>
<span data-ttu-id="957fd-123">ServiceBus AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="957fd-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="957fd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="957fd-124">-Name</span></span>
<span data-ttu-id="957fd-125">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="957fd-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957fd-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="957fd-126">-Namespace</span></span>
<span data-ttu-id="957fd-127">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="957fd-127">Namespace Name</span></span>

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

### <span data-ttu-id="957fd-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="957fd-128">-PassThru</span></span>
<span data-ttu-id="957fd-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="957fd-130">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="957fd-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="957fd-131">-Queue</span></span>
<span data-ttu-id="957fd-132">큐 이름</span><span class="sxs-lookup"><span data-stu-id="957fd-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957fd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957fd-133">-ResourceGroupName</span></span>
<span data-ttu-id="957fd-134">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="957fd-134">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957fd-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="957fd-135">-Topic</span></span>
<span data-ttu-id="957fd-136">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="957fd-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957fd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="957fd-137">-Confirm</span></span>
<span data-ttu-id="957fd-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="957fd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957fd-139">-WhatIf</span></span>
<span data-ttu-id="957fd-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="957fd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="957fd-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="957fd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957fd-142">CommonParameters</span></span>
<span data-ttu-id="957fd-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="957fd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957fd-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="957fd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957fd-145">입력</span><span class="sxs-lookup"><span data-stu-id="957fd-145">INPUTS</span></span>

### <span data-ttu-id="957fd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="957fd-146">System.String</span></span>

### <span data-ttu-id="957fd-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="957fd-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="957fd-148">출력</span><span class="sxs-lookup"><span data-stu-id="957fd-148">OUTPUTS</span></span>

### <span data-ttu-id="957fd-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="957fd-149">System.Boolean</span></span>

## <span data-ttu-id="957fd-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="957fd-150">NOTES</span></span>

## <span data-ttu-id="957fd-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="957fd-151">RELATED LINKS</span></span>
