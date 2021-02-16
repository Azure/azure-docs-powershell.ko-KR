---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178932"
---
# <span data-ttu-id="0a60b-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0a60b-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="0a60b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a60b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a60b-103">주어진 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에서 HybridConnection의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="0a60b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a60b-104">SYNTAX</span></span>

### <span data-ttu-id="0a60b-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a60b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a60b-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a60b-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a60b-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a60b-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a60b-108">설명</span><span class="sxs-lookup"><span data-stu-id="0a60b-108">DESCRIPTION</span></span>
<span data-ttu-id="0a60b-109">**Remove-AzRelayAuthorizationRule** cmdlet은 주어진 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="0a60b-110">예제</span><span class="sxs-lookup"><span data-stu-id="0a60b-110">EXAMPLES</span></span>

### <span data-ttu-id="0a60b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a60b-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="0a60b-112">네임스페이스의 권한 부여 `AuthoRule1` 규칙을 `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="0a60b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0a60b-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="0a60b-114">네임스페이스에서 `AuthoRule1` WcfRelay의 권한 부여 `TestWcfRelay` 규칙을 `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="0a60b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="0a60b-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="0a60b-116">네임스페이스에서 `AuthoRule1` HybridConnection의 권한 부여 `TestHybridConnection` 규칙을 `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="0a60b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a60b-117">PARAMETERS</span></span>

### <span data-ttu-id="0a60b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a60b-118">-DefaultProfile</span></span>
<span data-ttu-id="0a60b-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a60b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0a60b-120">-Force</span></span>
<span data-ttu-id="0a60b-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a60b-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="0a60b-122">-HybridConnection</span></span>
<span data-ttu-id="0a60b-123">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a60b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0a60b-124">-Name</span></span>
<span data-ttu-id="0a60b-125">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a60b-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0a60b-126">-Namespace</span></span>
<span data-ttu-id="0a60b-127">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a60b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a60b-128">-PassThru</span></span>
<span data-ttu-id="0a60b-129">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="0a60b-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0a60b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a60b-130">-ResourceGroupName</span></span>
<span data-ttu-id="0a60b-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a60b-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="0a60b-132">-WcfRelay</span></span>
<span data-ttu-id="0a60b-133">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a60b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a60b-134">-Confirm</span></span>
<span data-ttu-id="0a60b-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a60b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a60b-136">-WhatIf</span></span>
<span data-ttu-id="0a60b-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0a60b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a60b-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a60b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a60b-139">CommonParameters</span></span>
<span data-ttu-id="0a60b-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a60b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a60b-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a60b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a60b-142">입력</span><span class="sxs-lookup"><span data-stu-id="0a60b-142">INPUTS</span></span>

### <span data-ttu-id="0a60b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0a60b-143">System.String</span></span>

## <span data-ttu-id="0a60b-144">출력</span><span class="sxs-lookup"><span data-stu-id="0a60b-144">OUTPUTS</span></span>

### <span data-ttu-id="0a60b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a60b-145">System.Boolean</span></span>

## <span data-ttu-id="0a60b-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a60b-146">NOTES</span></span>

## <span data-ttu-id="0a60b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a60b-147">RELATED LINKS</span></span>