---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: fe2f405e07bc20437b9c0b47b8e551039b90b500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965051"
---
# <span data-ttu-id="5c0ae-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5c0ae-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="5c0ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0ae-103">Cognitive Services 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="5c0ae-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5c0ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c0ae-104">SYNTAX</span></span>

### <span data-ttu-id="5c0ae-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c0ae-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c0ae-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="5c0ae-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c0ae-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5c0ae-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c0ae-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="5c0ae-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c0ae-109">설명</span><span class="sxs-lookup"><span data-stu-id="5c0ae-109">DESCRIPTION</span></span>
<span data-ttu-id="5c0ae-110">**Add-AzCognitiveServicesAccountNetworkRule** cmdlet은 Cognitive Services 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5c0ae-111">예제</span><span class="sxs-lookup"><span data-stu-id="5c0ae-111">EXAMPLES</span></span>

### <span data-ttu-id="5c0ae-112">예제 1: IpAddressOrRange를 통해 여러 IpRules 추가</span><span class="sxs-lookup"><span data-stu-id="5c0ae-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="5c0ae-113">이 명령은 IpAddressOrRange를 사용하여 여러 IpRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="5c0ae-114">예제 2: VirtualNetworkResourceID를 통해 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="5c0ae-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="5c0ae-115">이 명령은 VirtualNetworkResourceID를 사용하여 VirtualNetworkRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="5c0ae-116">예제 3: 다른 계정의 VirtualNetworkRule 개체로 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="5c0ae-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="5c0ae-117">이 명령은 다른 계정의 VirtualNetworkRule 개체로 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="5c0ae-118">예제 4: IpRule 개체로 여러 IpRule 추가, JSON을 사용하여 입력</span><span class="sxs-lookup"><span data-stu-id="5c0ae-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="5c0ae-119">이 명령은 IpRule 개체가 있는 여러 IpRule을 추가하고 JSON을 사용하여 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="5c0ae-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c0ae-120">PARAMETERS</span></span>

### <span data-ttu-id="5c0ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0ae-121">-DefaultProfile</span></span>
<span data-ttu-id="5c0ae-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c0ae-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5c0ae-123">-IpAddressOrRange</span></span>
<span data-ttu-id="5c0ae-124">Cognitive Services 계정 NetworkRule IpRules IPAddressOrRange 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="5c0ae-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="5c0ae-125">-IpRule</span></span>
<span data-ttu-id="5c0ae-126">Cognitive Services 계정 NetworkRule IPRules.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="5c0ae-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5c0ae-127">-Name</span></span>
<span data-ttu-id="5c0ae-128">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="5c0ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="5c0ae-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c0ae-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5c0ae-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5c0ae-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="5c0ae-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5c0ae-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="5c0ae-134">Cognitive Services 계정 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="5c0ae-135">-확인</span><span class="sxs-lookup"><span data-stu-id="5c0ae-135">-Confirm</span></span>
<span data-ttu-id="5c0ae-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0ae-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0ae-137">-WhatIf</span></span>
<span data-ttu-id="5c0ae-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0ae-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0ae-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0ae-140">CommonParameters</span></span>
<span data-ttu-id="5c0ae-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c0ae-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0ae-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c0ae-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0ae-143">입력</span><span class="sxs-lookup"><span data-stu-id="5c0ae-143">INPUTS</span></span>

### <span data-ttu-id="5c0ae-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5c0ae-144">System.String</span></span>

### <span data-ttu-id="5c0ae-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="5c0ae-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="5c0ae-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="5c0ae-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="5c0ae-147">출력</span><span class="sxs-lookup"><span data-stu-id="5c0ae-147">OUTPUTS</span></span>

### <span data-ttu-id="5c0ae-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5c0ae-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="5c0ae-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="5c0ae-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="5c0ae-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c0ae-150">NOTES</span></span>

## <span data-ttu-id="5c0ae-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c0ae-151">RELATED LINKS</span></span>
