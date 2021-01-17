---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376692"
---
# <span data-ttu-id="88bc0-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="88bc0-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="88bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="88bc0-103">권한 부여 규칙의 세부 정보를 얻거나 권한 부여 규칙 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="88bc0-104">구문</span><span class="sxs-lookup"><span data-stu-id="88bc0-104">SYNTAX</span></span>

### <span data-ttu-id="88bc0-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="88bc0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88bc0-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="88bc0-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88bc0-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="88bc0-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88bc0-108">설명</span><span class="sxs-lookup"><span data-stu-id="88bc0-108">DESCRIPTION</span></span>
<span data-ttu-id="88bc0-109">Get-AzEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보 또는 지정된 이벤트 허브에 대한 모든 권한 부여 규칙 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="88bc0-110">권한 부여 규칙의 이름이 제공된 경우 해당 단일 권한 부여 규칙의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="88bc0-111">권한 부여 규칙의 이름이 제공되지 않으면 지정된 이벤트 허브에 대한 모든 권한 부여 규칙 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="88bc0-112">(재해 복구) 별칭 이름이 제공되면 구성된 별칭에 대한 네임스페이스의 권한 부여 규칙 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="88bc0-113">예제</span><span class="sxs-lookup"><span data-stu-id="88bc0-113">EXAMPLES</span></span>

### <span data-ttu-id="88bc0-114">예제 1: 네임스페이스에 대한 AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="88bc0-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="88bc0-115">\`MyNamespaceName 네임스페이스에서 MyAuthRuleName 권한 부여 규칙을 \` \` \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="88bc0-116">예제 2: 네임스페이스에 대한 AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="88bc0-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="88bc0-117">MyNamespaceName 네임스페이스의 모든 권한 부여 규칙 목록을 \` \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="88bc0-118">예제 3: EventHub에 대한 AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="88bc0-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="88bc0-119">MyNamespaceName 네임스페이스로 범위가 지정되는 이벤트 허브 \` \` \` MyEventHubName에서 \` \` MyAuthRuleName 권한 부여 규칙을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="88bc0-120">예제 4: EventHub에 대한 AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="88bc0-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="88bc0-121">MyNamespaceName 네임스페이스로 범위가 지정되는 이벤트 허브 \` MyEventHubName에서 목록 권한 부여 \` \` 규칙을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="88bc0-122">예제 5: 별칭에 대한 AuthorizationRule(GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="88bc0-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="88bc0-123">\`MyNamespaceName 네임스페이스에서 MyAuthRuleName 권한 부여 규칙을 \` \` \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="88bc0-124">예제 6: 별칭에 대한 AuthorizationRules(GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="88bc0-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="88bc0-125">MyNamespaceName 네임스페이스의 모든 권한 부여 규칙 \` \` \` MyAuthRuleName 목록을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="88bc0-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88bc0-126">PARAMETERS</span></span>

### <span data-ttu-id="88bc0-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="88bc0-127">-AliasName</span></span>
<span data-ttu-id="88bc0-128">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="88bc0-128">Alias Name</span></span>

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

### <span data-ttu-id="88bc0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bc0-129">-DefaultProfile</span></span>
<span data-ttu-id="88bc0-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88bc0-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="88bc0-131">-Eventhub</span></span>
<span data-ttu-id="88bc0-132">Eventhub 이름</span><span class="sxs-lookup"><span data-stu-id="88bc0-132">Eventhub Name</span></span>

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

### <span data-ttu-id="88bc0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="88bc0-133">-Name</span></span>
<span data-ttu-id="88bc0-134">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="88bc0-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="88bc0-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="88bc0-135">-Namespace</span></span>
<span data-ttu-id="88bc0-136">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="88bc0-136">Namespace Name</span></span>

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

### <span data-ttu-id="88bc0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88bc0-137">-ResourceGroupName</span></span>
<span data-ttu-id="88bc0-138">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="88bc0-138">Resource Group Name</span></span>

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

### <span data-ttu-id="88bc0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bc0-139">CommonParameters</span></span>
<span data-ttu-id="88bc0-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88bc0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bc0-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88bc0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bc0-142">입력</span><span class="sxs-lookup"><span data-stu-id="88bc0-142">INPUTS</span></span>

### <span data-ttu-id="88bc0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="88bc0-143">System.String</span></span>

## <span data-ttu-id="88bc0-144">출력</span><span class="sxs-lookup"><span data-stu-id="88bc0-144">OUTPUTS</span></span>

### <span data-ttu-id="88bc0-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="88bc0-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="88bc0-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88bc0-146">NOTES</span></span>

## <span data-ttu-id="88bc0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88bc0-147">RELATED LINKS</span></span>
