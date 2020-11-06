---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537235"
---
# <span data-ttu-id="4832f-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4832f-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4832f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4832f-102">SYNOPSIS</span></span>
<span data-ttu-id="4832f-103">지정 된 이벤트 허브 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4832f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4832f-104">SYNTAX</span></span>

### <span data-ttu-id="4832f-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4832f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4832f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4832f-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4832f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4832f-107">DESCRIPTION</span></span>
<span data-ttu-id="4832f-108">Remove-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정한 권한 부여 규칙을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="4832f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4832f-109">EXAMPLES</span></span>

### <span data-ttu-id="4832f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4832f-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="4832f-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="4832f-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="4832f-112">\` \` 이벤트 허브 MyEventHubName에서 권한 부여 규칙 MyAuthRuleName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="4832f-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="4832f-113">변수</span><span class="sxs-lookup"><span data-stu-id="4832f-113">PARAMETERS</span></span>

### <span data-ttu-id="4832f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4832f-114">-ResourceGroupName</span></span>
<span data-ttu-id="4832f-115">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-115">Resource group name.</span></span>

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

### <span data-ttu-id="4832f-116">-확인</span><span class="sxs-lookup"><span data-stu-id="4832f-116">-Confirm</span></span>
<span data-ttu-id="4832f-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4832f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4832f-118">-WhatIf</span></span>
<span data-ttu-id="4832f-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4832f-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4832f-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4832f-121">-EventHub</span></span>
<span data-ttu-id="4832f-122">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="4832f-122">EventHub Name.</span></span>

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

### <span data-ttu-id="4832f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4832f-123">-Force</span></span>
<span data-ttu-id="4832f-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4832f-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4832f-125">-Name</span></span>
<span data-ttu-id="4832f-126">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="4832f-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4832f-127">-Namespace</span></span>
<span data-ttu-id="4832f-128">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4832f-128">Namespace Name.</span></span>

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

### <span data-ttu-id="4832f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4832f-129">-PassThru</span></span>
<span data-ttu-id="4832f-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="4832f-130">{{Fill PassThru Description}}</span></span>

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

## <span data-ttu-id="4832f-131">입력</span><span class="sxs-lookup"><span data-stu-id="4832f-131">INPUTS</span></span>

### <span data-ttu-id="4832f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4832f-132">System.String</span></span>

## <span data-ttu-id="4832f-133">출력</span><span class="sxs-lookup"><span data-stu-id="4832f-133">OUTPUTS</span></span>

### <span data-ttu-id="4832f-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4832f-134">System.Boolean</span></span>

## <span data-ttu-id="4832f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4832f-135">NOTES</span></span>

## <span data-ttu-id="4832f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4832f-136">RELATED LINKS</span></span>

