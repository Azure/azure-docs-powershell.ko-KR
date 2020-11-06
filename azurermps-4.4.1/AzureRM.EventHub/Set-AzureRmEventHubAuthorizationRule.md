---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532272"
---
# <span data-ttu-id="88613-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="88613-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="88613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88613-102">SYNOPSIS</span></span>
<span data-ttu-id="88613-103">이벤트 허브에서 지정 된 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="88613-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88613-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88613-104">SYNTAX</span></span>

### <span data-ttu-id="88613-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="88613-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="88613-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="88613-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="88613-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="88613-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="88613-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="88613-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="88613-109">설명은</span><span class="sxs-lookup"><span data-stu-id="88613-109">DESCRIPTION</span></span>
<span data-ttu-id="88613-110">Set-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정 된 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="88613-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="88613-111">예제의</span><span class="sxs-lookup"><span data-stu-id="88613-111">EXAMPLES</span></span>

### <span data-ttu-id="88613-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="88613-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="88613-113">\` \` \` \` 네임 스페이스 MyNamespaceName으로 범위가 지정 된 이벤트 허브 MyEventHubName에 대 한 관리 권한을 부여 하도록 권한 \` 부여 규칙 MyAuthRuleName를 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="88613-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="88613-114">변수</span><span class="sxs-lookup"><span data-stu-id="88613-114">PARAMETERS</span></span>

### <span data-ttu-id="88613-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88613-115">-ResourceGroupName</span></span>
<span data-ttu-id="88613-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88613-116">Resource group name.</span></span>

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

### <span data-ttu-id="88613-117">-권한</span><span class="sxs-lookup"><span data-stu-id="88613-117">-Rights</span></span>
<span data-ttu-id="88613-118">' AuthruleObj '가 지정 되지 않은 경우 필수 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="88613-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="88613-119">권리가 예를 들어 @ ("수신", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="88613-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88613-120">-확인</span><span class="sxs-lookup"><span data-stu-id="88613-120">-Confirm</span></span>
<span data-ttu-id="88613-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88613-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88613-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88613-122">-WhatIf</span></span>
<span data-ttu-id="88613-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88613-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88613-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88613-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88613-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="88613-125">-EventHub</span></span>
<span data-ttu-id="88613-126">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="88613-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88613-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88613-127">-InputObject</span></span>
<span data-ttu-id="88613-128">{{Fill InputObject 설명}}</span><span class="sxs-lookup"><span data-stu-id="88613-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88613-129">-이름</span><span class="sxs-lookup"><span data-stu-id="88613-129">-Name</span></span>
<span data-ttu-id="88613-130">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88613-130">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88613-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88613-131">-Namespace</span></span>
<span data-ttu-id="88613-132">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88613-132">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="88613-133">입력</span><span class="sxs-lookup"><span data-stu-id="88613-133">INPUTS</span></span>

### <span data-ttu-id="88613-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88613-134">System.String</span></span>

## <span data-ttu-id="88613-135">출력</span><span class="sxs-lookup"><span data-stu-id="88613-135">OUTPUTS</span></span>

### <span data-ttu-id="88613-136">Microsoft. \*. a. a.</span><span class="sxs-lookup"><span data-stu-id="88613-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="88613-137">상속자</span><span class="sxs-lookup"><span data-stu-id="88613-137">NOTES</span></span>

## <span data-ttu-id="88613-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88613-138">RELATED LINKS</span></span>

