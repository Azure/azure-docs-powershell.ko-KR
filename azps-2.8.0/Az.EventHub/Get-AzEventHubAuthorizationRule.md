---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 66e32c19001586972cb408e61397545fb1c25d44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696498"
---
# <span data-ttu-id="217a4-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="217a4-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="217a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="217a4-102">SYNOPSIS</span></span>
<span data-ttu-id="217a4-103">권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="217a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="217a4-104">SYNTAX</span></span>

### <span data-ttu-id="217a4-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="217a4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="217a4-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="217a4-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="217a4-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="217a4-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="217a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="217a4-108">DESCRIPTION</span></span>
<span data-ttu-id="217a4-109">Get-AzEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보나 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="217a4-110">권한 부여 규칙의 이름을 제공 하는 경우 해당 단일 인증 규칙의 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="217a4-111">권한 부여 규칙의 이름을 제공 하지 않으면 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="217a4-112">(재해 복구) 별칭 이름이 제공 되 면 별칭에 대 한 네임 스페이스의 권한 부여 규칙에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="217a4-113">예제의</span><span class="sxs-lookup"><span data-stu-id="217a4-113">EXAMPLES</span></span>

### <span data-ttu-id="217a4-114">예제 1.0-네임 스페이스에 대 한 AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="217a4-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="217a4-115">\` \` 네임 스페이스 MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="217a4-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="217a4-116">예제 1.1-네임 스페이스에 대 한 AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="217a4-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="217a4-117">네임 스페이스 MyNamespaceName의 모든 권한 부여 규칙 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="217a4-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="217a4-118">예제 2.0-EventHub에 대 한 AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="217a4-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="217a4-119">\` \` \` \` 네임 스페이스 MyNamespaceName로 범위가 지정 된 이벤트 허브 MyEventHubName에서 \` 권한 부여 규칙 MyAuthRuleName를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="217a4-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="217a4-120">예제 2.1-EventHub에 대 한 AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="217a4-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="217a4-121">\` \` MyNamespaceName 네임 스페이스의 범위를 지정 하는 이벤트 허브 MyEventHubName의 목록 인증 규칙을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="217a4-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="217a4-122">예제 3.0-별칭에 대 한 AuthorizationRule (GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="217a4-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="217a4-123">\` \` 네임 스페이스 MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="217a4-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="217a4-124">예제 3.1-별칭에 대 한 AuthorizationRules (GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="217a4-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="217a4-125">\` \` 네임 스페이스 MyNamespaceName의 모든 권한 부여 규칙 MyAuthRuleName 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="217a4-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="217a4-126">변수</span><span class="sxs-lookup"><span data-stu-id="217a4-126">PARAMETERS</span></span>

### <span data-ttu-id="217a4-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="217a4-127">-AliasName</span></span>
<span data-ttu-id="217a4-128">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="217a4-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217a4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217a4-129">-DefaultProfile</span></span>
<span data-ttu-id="217a4-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="217a4-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="217a4-131">-Eventhub</span></span>
<span data-ttu-id="217a4-132">Eventhub 이름</span><span class="sxs-lookup"><span data-stu-id="217a4-132">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217a4-133">-이름</span><span class="sxs-lookup"><span data-stu-id="217a4-133">-Name</span></span>
<span data-ttu-id="217a4-134">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="217a4-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217a4-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="217a4-135">-Namespace</span></span>
<span data-ttu-id="217a4-136">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="217a4-136">Namespace Name</span></span>

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

### <span data-ttu-id="217a4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217a4-137">-ResourceGroupName</span></span>
<span data-ttu-id="217a4-138">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="217a4-138">Resource Group Name</span></span>

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

### <span data-ttu-id="217a4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217a4-139">CommonParameters</span></span>
<span data-ttu-id="217a4-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="217a4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217a4-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217a4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217a4-142">입력</span><span class="sxs-lookup"><span data-stu-id="217a4-142">INPUTS</span></span>

### <span data-ttu-id="217a4-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="217a4-143">System.String</span></span>

## <span data-ttu-id="217a4-144">출력</span><span class="sxs-lookup"><span data-stu-id="217a4-144">OUTPUTS</span></span>

### <span data-ttu-id="217a4-145">Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="217a4-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="217a4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="217a4-146">NOTES</span></span>

## <span data-ttu-id="217a4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="217a4-147">RELATED LINKS</span></span>
