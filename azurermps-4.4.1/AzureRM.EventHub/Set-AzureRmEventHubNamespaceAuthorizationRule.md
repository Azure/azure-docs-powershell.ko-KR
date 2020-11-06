---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538180"
---
# <span data-ttu-id="479c9-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="479c9-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="479c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="479c9-102">SYNOPSIS</span></span>
<span data-ttu-id="479c9-103">지정 된 이벤트 허브 네임 스페이스에 대 한 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="479c9-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="479c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="479c9-105">DESCRIPTION</span></span>
<span data-ttu-id="479c9-106">Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet은 지정 된 이벤트 허브 네임 스페이스에 대 한 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="479c9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="479c9-107">EXAMPLES</span></span>

### <span data-ttu-id="479c9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="479c9-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="479c9-109">\` \` 관리 권한을 부여 하도록 권한 부여 규칙 MyAuthRuleName를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="479c9-110">변수</span><span class="sxs-lookup"><span data-stu-id="479c9-110">PARAMETERS</span></span>

### <span data-ttu-id="479c9-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="479c9-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="479c9-112">인증 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-112">The authorization rule name.</span></span>
<span data-ttu-id="479c9-113">-AuthruleObj가 지정 되지 않은 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479c9-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="479c9-114">-AuthRuleObj</span></span>
<span data-ttu-id="479c9-115">이벤트 허브 네임 스페이스 권한 부여 규칙 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479c9-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="479c9-116">-NamespaceName</span></span>
<span data-ttu-id="479c9-117">이벤트 허브 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-117">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479c9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479c9-118">-ResourceGroupName</span></span>
<span data-ttu-id="479c9-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-119">Resource group name.</span></span>

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

### <span data-ttu-id="479c9-120">-권한</span><span class="sxs-lookup"><span data-stu-id="479c9-120">-Rights</span></span>
<span data-ttu-id="479c9-121">-AuthruleObj가 지정 되지 않은 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="479c9-122">권리가 예를 들어 @ ("수신", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="479c9-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479c9-123">-확인</span><span class="sxs-lookup"><span data-stu-id="479c9-123">-Confirm</span></span>
<span data-ttu-id="479c9-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="479c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479c9-125">-WhatIf</span></span>
<span data-ttu-id="479c9-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="479c9-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="479c9-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="479c9-128">입력</span><span class="sxs-lookup"><span data-stu-id="479c9-128">INPUTS</span></span>

### <span data-ttu-id="479c9-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="479c9-129">System.String</span></span>

## <span data-ttu-id="479c9-130">출력</span><span class="sxs-lookup"><span data-stu-id="479c9-130">OUTPUTS</span></span>

### <span data-ttu-id="479c9-131">Microsoft. \*. a. a.</span><span class="sxs-lookup"><span data-stu-id="479c9-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="479c9-132">상속자</span><span class="sxs-lookup"><span data-stu-id="479c9-132">NOTES</span></span>

## <span data-ttu-id="479c9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="479c9-133">RELATED LINKS</span></span>

