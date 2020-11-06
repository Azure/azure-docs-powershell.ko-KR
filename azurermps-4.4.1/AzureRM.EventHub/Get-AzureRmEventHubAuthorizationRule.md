---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537268"
---
# <span data-ttu-id="17a86-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="17a86-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="17a86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17a86-102">SYNOPSIS</span></span>
<span data-ttu-id="17a86-103">권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17a86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17a86-104">SYNTAX</span></span>

### <span data-ttu-id="17a86-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="17a86-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="17a86-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="17a86-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="17a86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="17a86-107">DESCRIPTION</span></span>
<span data-ttu-id="17a86-108">Get-AzureRmEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보나 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="17a86-109">권한 부여 규칙의 이름을 제공 하는 경우 해당 단일 인증 규칙의 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="17a86-110">권한 부여 규칙의 이름을 제공 하지 않으면 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="17a86-111">예제의</span><span class="sxs-lookup"><span data-stu-id="17a86-111">EXAMPLES</span></span>

### <span data-ttu-id="17a86-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="17a86-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="17a86-113">\` \` \` \` 네임 스페이스 MyNamespaceName로 범위가 지정 된 이벤트 허브 MyEventHubName에서 \` 권한 부여 규칙 MyAuthRuleName를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="17a86-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="17a86-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="17a86-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="17a86-115">\` \` MyNamespaceName 네임 스페이스의 범위를 지정 하는 이벤트 허브 MyEventHubName의 모든 권한 부여 규칙 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="17a86-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="17a86-116">변수</span><span class="sxs-lookup"><span data-stu-id="17a86-116">PARAMETERS</span></span>

### <span data-ttu-id="17a86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a86-117">-ResourceGroupName</span></span>
<span data-ttu-id="17a86-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-118">Resource group name.</span></span>

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

### <span data-ttu-id="17a86-119">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="17a86-119">-Eventhub</span></span>
<span data-ttu-id="17a86-120">Eventhub 이름.</span><span class="sxs-lookup"><span data-stu-id="17a86-120">Eventhub Name.</span></span>

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

### <span data-ttu-id="17a86-121">-이름</span><span class="sxs-lookup"><span data-stu-id="17a86-121">-Name</span></span>
<span data-ttu-id="17a86-122">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17a86-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="17a86-123">-Namespace</span></span>
<span data-ttu-id="17a86-124">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17a86-124">Namespace Name.</span></span>

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

## <span data-ttu-id="17a86-125">입력</span><span class="sxs-lookup"><span data-stu-id="17a86-125">INPUTS</span></span>

### <span data-ttu-id="17a86-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17a86-126">System.String</span></span>

## <span data-ttu-id="17a86-127">출력</span><span class="sxs-lookup"><span data-stu-id="17a86-127">OUTPUTS</span></span>

### <span data-ttu-id="17a86-128">System.webserver. List ' 1 [[Microsoft Azure.]. a n [[0.0.1.0]. SharedAccessAuthorizationRuleAttributes, Microsoft Azure. 명령. EventHub, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="17a86-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="17a86-129">상속자</span><span class="sxs-lookup"><span data-stu-id="17a86-129">NOTES</span></span>

## <span data-ttu-id="17a86-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17a86-130">RELATED LINKS</span></span>

