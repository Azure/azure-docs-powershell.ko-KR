---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703377"
---
# <span data-ttu-id="b1c38-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b1c38-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b1c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1c38-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c38-103">네임 스페이스 또는 eventhub에 대 한 새 이벤트 허브 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1c38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1c38-104">SYNTAX</span></span>

### <span data-ttu-id="b1c38-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1c38-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b1c38-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1c38-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b1c38-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b1c38-107">DESCRIPTION</span></span>
<span data-ttu-id="b1c38-108">New-AzureRmEventHubAuthorizationRule cmdlet은 새 이벤트 허브 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b1c38-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b1c38-109">EXAMPLES</span></span>

### <span data-ttu-id="b1c38-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1c38-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b1c38-111">\` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 MyNamespaceName 네임 스페이스에 대 한 수신 대기 및 보내기 권한을 부여 하 MyAuthRuleName 권한 부여 규칙을 만듭니다 \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="b1c38-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b1c38-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b1c38-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b1c38-113">\` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName의 이벤트 허브 MyEventHubName에 대 한 수신 \` 대기 및 \` 보내기 권한을 부여 \` MyAuthRuleName는 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b1c38-114">변수</span><span class="sxs-lookup"><span data-stu-id="b1c38-114">PARAMETERS</span></span>

### <span data-ttu-id="b1c38-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c38-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1c38-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-116">Resource group name.</span></span>

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

### <span data-ttu-id="b1c38-117">-권한</span><span class="sxs-lookup"><span data-stu-id="b1c38-117">-Rights</span></span>
<span data-ttu-id="b1c38-118">권리가 예를 들어 @ ("듣기", "Send", "관리").</span><span class="sxs-lookup"><span data-stu-id="b1c38-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c38-119">-확인</span><span class="sxs-lookup"><span data-stu-id="b1c38-119">-Confirm</span></span>
<span data-ttu-id="b1c38-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c38-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c38-121">-WhatIf</span></span>
<span data-ttu-id="b1c38-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c38-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c38-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b1c38-124">-EventHub</span></span>
<span data-ttu-id="b1c38-125">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="b1c38-125">EventHub Name.</span></span>

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

### <span data-ttu-id="b1c38-126">-이름</span><span class="sxs-lookup"><span data-stu-id="b1c38-126">-Name</span></span>
<span data-ttu-id="b1c38-127">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-127">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b1c38-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b1c38-128">-Namespace</span></span>
<span data-ttu-id="b1c38-129">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1c38-129">Namespace Name.</span></span>

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

## <span data-ttu-id="b1c38-130">입력</span><span class="sxs-lookup"><span data-stu-id="b1c38-130">INPUTS</span></span>

### <span data-ttu-id="b1c38-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1c38-131">System.String</span></span>

## <span data-ttu-id="b1c38-132">출력</span><span class="sxs-lookup"><span data-stu-id="b1c38-132">OUTPUTS</span></span>

### <span data-ttu-id="b1c38-133">Microsoft. \*. a. a.</span><span class="sxs-lookup"><span data-stu-id="b1c38-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b1c38-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b1c38-134">NOTES</span></span>

## <span data-ttu-id="b1c38-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1c38-135">RELATED LINKS</span></span>

