---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204101"
---
# <span data-ttu-id="09bf6-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="09bf6-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="09bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="09bf6-103">지정된 이벤트 허브 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="09bf6-104">구문</span><span class="sxs-lookup"><span data-stu-id="09bf6-104">SYNTAX</span></span>

### <span data-ttu-id="09bf6-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="09bf6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09bf6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="09bf6-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09bf6-107">설명</span><span class="sxs-lookup"><span data-stu-id="09bf6-107">DESCRIPTION</span></span>
<span data-ttu-id="09bf6-108">이 Remove-AzEventHubAuthorizationRule cmdlet은 지정된 이벤트 허브에서 지정된 권한 부여 규칙을 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="09bf6-109">예제</span><span class="sxs-lookup"><span data-stu-id="09bf6-109">EXAMPLES</span></span>

### <span data-ttu-id="09bf6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="09bf6-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="09bf6-111">네임스페이스 \` \` \` MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="09bf6-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="09bf6-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="09bf6-113">이벤트 허브 \` \` \` MyEventHubName에서 MyAuthRuleName 권한 부여 규칙을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="09bf6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09bf6-114">PARAMETERS</span></span>

### <span data-ttu-id="09bf6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bf6-115">-DefaultProfile</span></span>
<span data-ttu-id="09bf6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09bf6-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="09bf6-117">-EventHub</span></span>
<span data-ttu-id="09bf6-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="09bf6-118">EventHub Name</span></span>

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

### <span data-ttu-id="09bf6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="09bf6-119">-Force</span></span>
<span data-ttu-id="09bf6-120">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="09bf6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="09bf6-121">-Name</span></span>
<span data-ttu-id="09bf6-122">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="09bf6-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="09bf6-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="09bf6-123">-Namespace</span></span>
<span data-ttu-id="09bf6-124">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="09bf6-124">Namespace Name</span></span>

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

### <span data-ttu-id="09bf6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09bf6-125">-PassThru</span></span>
<span data-ttu-id="09bf6-126">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="09bf6-127">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="09bf6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09bf6-128">-ResourceGroupName</span></span>
<span data-ttu-id="09bf6-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="09bf6-129">Resource Group Name</span></span>

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

### <span data-ttu-id="09bf6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09bf6-130">-Confirm</span></span>
<span data-ttu-id="09bf6-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09bf6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09bf6-132">-WhatIf</span></span>
<span data-ttu-id="09bf6-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="09bf6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09bf6-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09bf6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bf6-135">CommonParameters</span></span>
<span data-ttu-id="09bf6-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09bf6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bf6-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="09bf6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bf6-138">입력</span><span class="sxs-lookup"><span data-stu-id="09bf6-138">INPUTS</span></span>

### <span data-ttu-id="09bf6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="09bf6-139">System.String</span></span>

## <span data-ttu-id="09bf6-140">출력</span><span class="sxs-lookup"><span data-stu-id="09bf6-140">OUTPUTS</span></span>

### <span data-ttu-id="09bf6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="09bf6-141">System.Boolean</span></span>

## <span data-ttu-id="09bf6-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09bf6-142">NOTES</span></span>

## <span data-ttu-id="09bf6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09bf6-143">RELATED LINKS</span></span>
