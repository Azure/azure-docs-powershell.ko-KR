---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213327"
---
# <span data-ttu-id="a5b8a-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5b8a-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="a5b8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b8a-103">네임 스페이스의 네트워크 규칙 집합에 대해 지정 된 단일 VirtualNetworkRule 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="a5b8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5b8a-104">SYNTAX</span></span>

### <span data-ttu-id="a5b8a-105">VirtualNetworkRulePropertiesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5b8a-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b8a-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b8a-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b8a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5b8a-107">DESCRIPTION</span></span>
<span data-ttu-id="a5b8a-108">네임 스페이스의 네트워크 규칙 집합에 대해 지정 된 단일 VirtualNetworkRule 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="a5b8a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5b8a-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b8a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5b8a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="a5b8a-111">네임 스페이스의 네트워크 규칙 집합에 대해 지정 된 단일 VirtualNetworkRule 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="a5b8a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a5b8a-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="a5b8a-113">지정 된 네임 스페이스에 대 한 NetworkRuleSet의 집합 1 개를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="a5b8a-114">변수</span><span class="sxs-lookup"><span data-stu-id="a5b8a-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b8a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5b8a-115">-AsJob</span></span>
<span data-ttu-id="a5b8a-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5b8a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5b8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b8a-117">-DefaultProfile</span></span>
<span data-ttu-id="a5b8a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b8a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a5b8a-119">-Name</span></span>
<span data-ttu-id="a5b8a-120">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="a5b8a-120">Namespace Name</span></span>

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

### <span data-ttu-id="a5b8a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5b8a-121">-PassThru</span></span>
<span data-ttu-id="a5b8a-122">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a5b8a-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a5b8a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b8a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5b8a-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a5b8a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a5b8a-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a5b8a-125">-SubnetId</span></span>
<span data-ttu-id="a5b8a-126">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a5b8a-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="a5b8a-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="a5b8a-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="a5b8a-128">IPRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="a5b8a-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b8a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a5b8a-129">-Confirm</span></span>
<span data-ttu-id="a5b8a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b8a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b8a-131">-WhatIf</span></span>
<span data-ttu-id="a5b8a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b8a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b8a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b8a-134">CommonParameters</span></span>
<span data-ttu-id="a5b8a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a5b8a-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b8a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b8a-137">입력</span><span class="sxs-lookup"><span data-stu-id="a5b8a-137">INPUTS</span></span>

### <span data-ttu-id="a5b8a-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5b8a-138">System.String</span></span>

### <span data-ttu-id="a5b8a-139">ServiceBus. PSNWRuleSetVirtualNetworkRulesAttributes/.</span><span class="sxs-lookup"><span data-stu-id="a5b8a-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="a5b8a-140">출력</span><span class="sxs-lookup"><span data-stu-id="a5b8a-140">OUTPUTS</span></span>

### <span data-ttu-id="a5b8a-141">ServiceBus를 호출 합니다. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a5b8a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a5b8a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a5b8a-142">NOTES</span></span>

## <span data-ttu-id="a5b8a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5b8a-143">RELATED LINKS</span></span>
