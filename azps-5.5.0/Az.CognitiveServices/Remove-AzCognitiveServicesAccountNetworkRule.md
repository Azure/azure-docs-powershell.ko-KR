---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205021"
---
# <span data-ttu-id="e695c-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e695c-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="e695c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e695c-102">SYNOPSIS</span></span>
<span data-ttu-id="e695c-103">Cognitive Services 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="e695c-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e695c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e695c-104">SYNTAX</span></span>

### <span data-ttu-id="e695c-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="e695c-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e695c-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e695c-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e695c-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e695c-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e695c-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="e695c-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e695c-109">설명</span><span class="sxs-lookup"><span data-stu-id="e695c-109">DESCRIPTION</span></span>
<span data-ttu-id="e695c-110">**Remove-AzCognitiveServicesAccountNetworkRule** cmdlet은 Cognitive Services 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e695c-111">예제</span><span class="sxs-lookup"><span data-stu-id="e695c-111">EXAMPLES</span></span>

### <span data-ttu-id="e695c-112">예제 1: IPAddressOrRange를 사용하여 여러 IpRules 제거</span><span class="sxs-lookup"><span data-stu-id="e695c-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="e695c-113">이 명령은 IPAddressOrRange를 사용하여 여러 IpRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="e695c-114">예제 2: JSON을 사용하여 VirtualNetworkRule 개체 입력으로 VirtualNetworkRule 제거</span><span class="sxs-lookup"><span data-stu-id="e695c-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="e695c-115">이 명령은 JSON을 사용하여 VirtualNetworkRule 개체 입력을 사용하여 VirtualNetworkRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="e695c-116">예제 3: 파이프라인을 사용하여 첫 번째 IpRule 제거</span><span class="sxs-lookup"><span data-stu-id="e695c-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="e695c-117">이 명령은 파이프라인이 있는 첫 번째 IpRule을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="e695c-118">예제 4: VirtualNetworkResourceID를 사용하여 여러 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="e695c-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="e695c-119">이 명령은 VirtualNetworkResourceID를 사용하여 여러 VirtualNetworkRules를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="e695c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e695c-120">PARAMETERS</span></span>

### <span data-ttu-id="e695c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e695c-121">-DefaultProfile</span></span>
<span data-ttu-id="e695c-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e695c-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e695c-123">-IpAddressOrRange</span></span>
<span data-ttu-id="e695c-124">Cognitive Services 계정 NetworkRule IpRules IpAddressOrRange(문자열).</span><span class="sxs-lookup"><span data-stu-id="e695c-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e695c-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e695c-125">-IpRule</span></span>
<span data-ttu-id="e695c-126">Cognitive Services 계정 NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="e695c-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e695c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e695c-127">-Name</span></span>
<span data-ttu-id="e695c-128">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-128">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e695c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e695c-129">-ResourceGroupName</span></span>
<span data-ttu-id="e695c-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e695c-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e695c-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e695c-132">Cognitive Services 계정 NetworkRule VirtualNetworkRules VirtualNetworkResourceId(문자열).</span><span class="sxs-lookup"><span data-stu-id="e695c-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e695c-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e695c-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="e695c-134">Cognitive Services 계정 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="e695c-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e695c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e695c-135">-Confirm</span></span>
<span data-ttu-id="e695c-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e695c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e695c-137">-WhatIf</span></span>
<span data-ttu-id="e695c-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e695c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e695c-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e695c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e695c-140">CommonParameters</span></span>
<span data-ttu-id="e695c-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e695c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e695c-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e695c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e695c-143">입력</span><span class="sxs-lookup"><span data-stu-id="e695c-143">INPUTS</span></span>

### <span data-ttu-id="e695c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e695c-144">System.String</span></span>

### <span data-ttu-id="e695c-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="e695c-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="e695c-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="e695c-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="e695c-147">출력</span><span class="sxs-lookup"><span data-stu-id="e695c-147">OUTPUTS</span></span>

### <span data-ttu-id="e695c-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e695c-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="e695c-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="e695c-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="e695c-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e695c-150">NOTES</span></span>

## <span data-ttu-id="e695c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e695c-151">RELATED LINKS</span></span>
