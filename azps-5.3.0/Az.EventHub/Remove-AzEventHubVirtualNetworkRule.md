---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493029"
---
# <span data-ttu-id="dcec4-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dcec4-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="dcec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcec4-102">SYNOPSIS</span></span>
<span data-ttu-id="dcec4-103">네임스페이스의 NetworkRuleSet에 대해 단일 주어진 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="dcec4-104">구문</span><span class="sxs-lookup"><span data-stu-id="dcec4-104">SYNTAX</span></span>

### <span data-ttu-id="dcec4-105">VirtualNetworkRulePropertiesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dcec4-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcec4-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcec4-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcec4-107">설명</span><span class="sxs-lookup"><span data-stu-id="dcec4-107">DESCRIPTION</span></span>
<span data-ttu-id="dcec4-108">네임스페이스의 NetworkRuleSet에 대해 단일 주어진 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="dcec4-109">예제</span><span class="sxs-lookup"><span data-stu-id="dcec4-109">EXAMPLES</span></span>

### <span data-ttu-id="dcec4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dcec4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="dcec4-111">네임스페이스의 NetworkRuleSet에 대해 단일 주어진 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="dcec4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="dcec4-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="dcec4-113">주어진 네임스페이스에 $virtualruleset NetworkRuleSet의 $virtualruleset 1을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="dcec4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcec4-114">PARAMETERS</span></span>

### <span data-ttu-id="dcec4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcec4-115">-AsJob</span></span>
<span data-ttu-id="dcec4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dcec4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcec4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcec4-117">-DefaultProfile</span></span>
<span data-ttu-id="dcec4-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcec4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dcec4-119">-Name</span></span>
<span data-ttu-id="dcec4-120">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="dcec4-120">Namespace Name</span></span>

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

### <span data-ttu-id="dcec4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcec4-121">-PassThru</span></span>
<span data-ttu-id="dcec4-122">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="dcec4-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dcec4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcec4-123">-ResourceGroupName</span></span>
<span data-ttu-id="dcec4-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dcec4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dcec4-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dcec4-125">-SubnetId</span></span>
<span data-ttu-id="dcec4-126">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dcec4-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec4-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="dcec4-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="dcec4-128">IPRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="dcec4-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcec4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcec4-129">-Confirm</span></span>
<span data-ttu-id="dcec4-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcec4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcec4-131">-WhatIf</span></span>
<span data-ttu-id="dcec4-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dcec4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcec4-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcec4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcec4-134">CommonParameters</span></span>
<span data-ttu-id="dcec4-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dcec4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dcec4-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcec4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcec4-137">입력</span><span class="sxs-lookup"><span data-stu-id="dcec4-137">INPUTS</span></span>

### <span data-ttu-id="dcec4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dcec4-138">System.String</span></span>

### <span data-ttu-id="dcec4-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="dcec4-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="dcec4-140">출력</span><span class="sxs-lookup"><span data-stu-id="dcec4-140">OUTPUTS</span></span>

### <span data-ttu-id="dcec4-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="dcec4-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="dcec4-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dcec4-142">NOTES</span></span>

## <span data-ttu-id="dcec4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcec4-143">RELATED LINKS</span></span>