---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177804"
---
# <span data-ttu-id="1a468-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1a468-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="1a468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a468-102">SYNOPSIS</span></span>
<span data-ttu-id="1a468-103">Cognitive Services 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="1a468-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1a468-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a468-104">SYNTAX</span></span>

### <span data-ttu-id="1a468-105">NetWorkRuleString(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a468-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a468-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1a468-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a468-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1a468-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a468-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="1a468-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a468-109">설명</span><span class="sxs-lookup"><span data-stu-id="1a468-109">DESCRIPTION</span></span>
<span data-ttu-id="1a468-110">**Add-AzCognitiveServicesAccountNetworkRule** cmdlet은 Cognitive Services 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1a468-111">예제</span><span class="sxs-lookup"><span data-stu-id="1a468-111">EXAMPLES</span></span>

### <span data-ttu-id="1a468-112">예제 1: IpAddressOrRange를 통해 여러 IpRules 추가</span><span class="sxs-lookup"><span data-stu-id="1a468-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="1a468-113">이 명령은 IpAddressOrRange를 사용하여 여러 IpRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="1a468-114">예제 2: VirtualNetworkResourceID를 통해 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="1a468-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="1a468-115">이 명령은 VirtualNetworkResourceID를 사용하여 VirtualNetworkRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="1a468-116">예제 3: 다른 계정에서 VirtualNetworkRule 개체를 사용하여 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="1a468-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="1a468-117">이 명령은 다른 계정의 VirtualNetworkRule 개체를 사용하여 VirtualNetworkRules를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="1a468-118">예제 4: JSON을 사용하여 입력한 IpRule 개체와 함께 여러 IpRule 추가</span><span class="sxs-lookup"><span data-stu-id="1a468-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="1a468-119">이 명령은 JSON을 사용하여 입력한 IpRule 개체와 함께 여러 IpRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="1a468-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a468-120">PARAMETERS</span></span>

### <span data-ttu-id="1a468-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a468-121">-DefaultProfile</span></span>
<span data-ttu-id="1a468-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a468-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1a468-123">-IpAddressOrRange</span></span>
<span data-ttu-id="1a468-124">Cognitive Services 계정 NetworkRule IpRules IpAddressOrRange(문자열).</span><span class="sxs-lookup"><span data-stu-id="1a468-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="1a468-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="1a468-125">-IpRule</span></span>
<span data-ttu-id="1a468-126">Cognitive Services 계정 NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="1a468-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="1a468-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1a468-127">-Name</span></span>
<span data-ttu-id="1a468-128">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="1a468-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a468-129">-ResourceGroupName</span></span>
<span data-ttu-id="1a468-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="1a468-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1a468-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1a468-132">Cognitive Services 계정 NetworkRule VirtualNetworkRules VirtualNetworkResourceId(문자열).</span><span class="sxs-lookup"><span data-stu-id="1a468-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="1a468-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1a468-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="1a468-134">Cognitive Services 계정 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="1a468-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="1a468-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a468-135">-Confirm</span></span>
<span data-ttu-id="1a468-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a468-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a468-137">-WhatIf</span></span>
<span data-ttu-id="1a468-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1a468-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a468-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a468-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a468-140">CommonParameters</span></span>
<span data-ttu-id="1a468-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a468-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a468-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a468-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a468-143">입력</span><span class="sxs-lookup"><span data-stu-id="1a468-143">INPUTS</span></span>

### <span data-ttu-id="1a468-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1a468-144">System.String</span></span>

### <span data-ttu-id="1a468-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="1a468-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1a468-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="1a468-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1a468-147">출력</span><span class="sxs-lookup"><span data-stu-id="1a468-147">OUTPUTS</span></span>

### <span data-ttu-id="1a468-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1a468-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="1a468-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="1a468-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="1a468-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a468-150">NOTES</span></span>

## <span data-ttu-id="1a468-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a468-151">RELATED LINKS</span></span>
