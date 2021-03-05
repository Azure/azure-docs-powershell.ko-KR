---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 1284780428fdaacfc255faf2ac640565eec44950
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000480"
---
# <span data-ttu-id="6aa7e-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6aa7e-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="6aa7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa7e-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa7e-103">주어진 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)에서 HybridConnection의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6aa7e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6aa7e-104">SYNTAX</span></span>

### <span data-ttu-id="6aa7e-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6aa7e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa7e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa7e-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa7e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6aa7e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aa7e-108">설명</span><span class="sxs-lookup"><span data-stu-id="6aa7e-108">DESCRIPTION</span></span>
<span data-ttu-id="6aa7e-109">**Remove-AzRelayAuthorizationRule** cmdlet은 주어진 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)의 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6aa7e-110">예제</span><span class="sxs-lookup"><span data-stu-id="6aa7e-110">EXAMPLES</span></span>

### <span data-ttu-id="6aa7e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6aa7e-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="6aa7e-112">네임스페이스의 권한 `AuthoRule1` 부여 규칙을 `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="6aa7e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6aa7e-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="6aa7e-114">네임스페이스에서 `AuthoRule1` WcfRelay의 권한 부여 `TestWcfRelay` 규칙을 `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="6aa7e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6aa7e-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="6aa7e-116">네임스페이스에서 `AuthoRule1` HybridConnection의 권한 부여 `TestHybridConnection` 규칙을 `TestNameSpace-Relay1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="6aa7e-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6aa7e-117">PARAMETERS</span></span>

### <span data-ttu-id="6aa7e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa7e-118">-DefaultProfile</span></span>
<span data-ttu-id="6aa7e-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa7e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6aa7e-120">-Force</span></span>
<span data-ttu-id="6aa7e-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6aa7e-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6aa7e-122">-HybridConnection</span></span>
<span data-ttu-id="6aa7e-123">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="6aa7e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6aa7e-124">-Name</span></span>
<span data-ttu-id="6aa7e-125">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6aa7e-126">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6aa7e-126">-Namespace</span></span>
<span data-ttu-id="6aa7e-127">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-127">Namespace Name.</span></span>

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

### <span data-ttu-id="6aa7e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aa7e-128">-PassThru</span></span>
<span data-ttu-id="6aa7e-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6aa7e-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6aa7e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa7e-130">-ResourceGroupName</span></span>
<span data-ttu-id="6aa7e-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="6aa7e-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6aa7e-132">-WcfRelay</span></span>
<span data-ttu-id="6aa7e-133">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6aa7e-134">-확인</span><span class="sxs-lookup"><span data-stu-id="6aa7e-134">-Confirm</span></span>
<span data-ttu-id="6aa7e-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa7e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa7e-136">-WhatIf</span></span>
<span data-ttu-id="6aa7e-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aa7e-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa7e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa7e-139">CommonParameters</span></span>
<span data-ttu-id="6aa7e-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa7e-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6aa7e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa7e-142">입력</span><span class="sxs-lookup"><span data-stu-id="6aa7e-142">INPUTS</span></span>

### <span data-ttu-id="6aa7e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6aa7e-143">System.String</span></span>

## <span data-ttu-id="6aa7e-144">출력</span><span class="sxs-lookup"><span data-stu-id="6aa7e-144">OUTPUTS</span></span>

### <span data-ttu-id="6aa7e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6aa7e-145">System.Boolean</span></span>

## <span data-ttu-id="6aa7e-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6aa7e-146">NOTES</span></span>

## <span data-ttu-id="6aa7e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6aa7e-147">RELATED LINKS</span></span>
