---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205016"
---
# <span data-ttu-id="712a1-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="712a1-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="712a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="712a1-102">SYNOPSIS</span></span>
<span data-ttu-id="712a1-103">Cognitive Services 계정의 NetworkRule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="712a1-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="712a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="712a1-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="712a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="712a1-105">DESCRIPTION</span></span>
<span data-ttu-id="712a1-106">**Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet은 Cognitive Services 계정의 NetworkRule 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="712a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="712a1-107">EXAMPLES</span></span>

### <span data-ttu-id="712a1-108">예제 1: NetworkRule의 모든 속성 업데이트, JSON으로 입력 규칙</span><span class="sxs-lookup"><span data-stu-id="712a1-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="712a1-109">이 명령은 NetworkRule의 모든 속성을 업데이트하고 JSON을 사용하여 규칙을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="712a1-110">예제 2: NetworkRule의 우회 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="712a1-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="712a1-111">이 명령은 NetworkRule의 우회 속성을 업데이트합니다(다른 속성은 변경되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="712a1-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="712a1-112">예제 3: Cognitive Services 계정의 NetworkRule 규칙 정리</span><span class="sxs-lookup"><span data-stu-id="712a1-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="712a1-113">이 명령은 Cognitive Services 계정의 NetworkRule 규칙을 정리합니다(다른 속성은 변경되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="712a1-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="712a1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="712a1-114">PARAMETERS</span></span>

### <span data-ttu-id="712a1-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="712a1-115">-DefaultAction</span></span>
<span data-ttu-id="712a1-116">Cognitive Services 계정 NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="712a1-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="712a1-117">기본값. `Deny`</span><span class="sxs-lookup"><span data-stu-id="712a1-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712a1-118">-DefaultProfile</span></span>
<span data-ttu-id="712a1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712a1-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="712a1-120">-IpRule</span></span>
<span data-ttu-id="712a1-121">Cognitive Services 계정 NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="712a1-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="712a1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="712a1-122">-Name</span></span>
<span data-ttu-id="712a1-123">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="712a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="712a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="712a1-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="712a1-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="712a1-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="712a1-127">Cognitive Services 계정 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="712a1-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="712a1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="712a1-128">-Confirm</span></span>
<span data-ttu-id="712a1-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="712a1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="712a1-130">-WhatIf</span></span>
<span data-ttu-id="712a1-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="712a1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="712a1-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="712a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712a1-133">CommonParameters</span></span>
<span data-ttu-id="712a1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="712a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712a1-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="712a1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712a1-136">입력</span><span class="sxs-lookup"><span data-stu-id="712a1-136">INPUTS</span></span>

### <span data-ttu-id="712a1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="712a1-137">System.String</span></span>

### <span data-ttu-id="712a1-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="712a1-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="712a1-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="712a1-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="712a1-140">출력</span><span class="sxs-lookup"><span data-stu-id="712a1-140">OUTPUTS</span></span>

### <span data-ttu-id="712a1-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="712a1-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="712a1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="712a1-142">NOTES</span></span>

## <span data-ttu-id="712a1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="712a1-143">RELATED LINKS</span></span>
