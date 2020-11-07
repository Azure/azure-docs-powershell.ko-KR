---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 8523fd6698e2fcdc4212b68a93269d60bc642628
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699501"
---
# <span data-ttu-id="2c83a-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2c83a-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="2c83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c83a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c83a-103">지정 된 릴레이 엔터티에서 HybridConnection의 권한 부여 규칙을 제거 합니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2c83a-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2c83a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c83a-104">SYNTAX</span></span>

### <span data-ttu-id="2c83a-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c83a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c83a-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c83a-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c83a-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c83a-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c83a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c83a-108">DESCRIPTION</span></span>
<span data-ttu-id="2c83a-109">**AzRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔티티의 권한 부여 규칙 (Namespace/WcfRelay/HybridConnection)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2c83a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2c83a-110">EXAMPLES</span></span>

### <span data-ttu-id="2c83a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c83a-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="2c83a-112">네임 스페이스의 권한 부여 규칙을 제거 합니다 `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2c83a-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2c83a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2c83a-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="2c83a-114">`AuthoRule1`네임 스페이스에서 WcfRelay의 권한 부여 규칙을 제거 합니다 `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2c83a-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2c83a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="2c83a-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="2c83a-116">`AuthoRule1`네임 스페이스에서 HybridConnection의 권한 부여 규칙을 제거 합니다 `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="2c83a-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="2c83a-117">변수</span><span class="sxs-lookup"><span data-stu-id="2c83a-117">PARAMETERS</span></span>

### <span data-ttu-id="2c83a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c83a-118">-DefaultProfile</span></span>
<span data-ttu-id="2c83a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c83a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2c83a-120">-Force</span></span>
<span data-ttu-id="2c83a-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c83a-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2c83a-122">-HybridConnection</span></span>
<span data-ttu-id="2c83a-123">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2c83a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="2c83a-124">-Name</span></span>
<span data-ttu-id="2c83a-125">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2c83a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c83a-126">-Namespace</span></span>
<span data-ttu-id="2c83a-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-127">Namespace Name.</span></span>

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

### <span data-ttu-id="2c83a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c83a-128">-PassThru</span></span>
<span data-ttu-id="2c83a-129">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="2c83a-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2c83a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c83a-130">-ResourceGroupName</span></span>
<span data-ttu-id="2c83a-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c83a-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2c83a-132">-WcfRelay</span></span>
<span data-ttu-id="2c83a-133">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2c83a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="2c83a-134">-Confirm</span></span>
<span data-ttu-id="2c83a-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c83a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c83a-136">-WhatIf</span></span>
<span data-ttu-id="2c83a-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c83a-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c83a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c83a-139">CommonParameters</span></span>
<span data-ttu-id="2c83a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c83a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c83a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c83a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c83a-142">입력</span><span class="sxs-lookup"><span data-stu-id="2c83a-142">INPUTS</span></span>

### <span data-ttu-id="2c83a-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c83a-143">System.String</span></span>

## <span data-ttu-id="2c83a-144">출력</span><span class="sxs-lookup"><span data-stu-id="2c83a-144">OUTPUTS</span></span>

### <span data-ttu-id="2c83a-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2c83a-145">System.Boolean</span></span>

## <span data-ttu-id="2c83a-146">상속자</span><span class="sxs-lookup"><span data-stu-id="2c83a-146">NOTES</span></span>

## <span data-ttu-id="2c83a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c83a-147">RELATED LINKS</span></span>
