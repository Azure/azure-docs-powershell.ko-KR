---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033764"
---
# <span data-ttu-id="9acd2-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9acd2-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="9acd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9acd2-102">SYNOPSIS</span></span>
<span data-ttu-id="9acd2-103">인지 서비스 계정의 NetWorkRule 속성에서 IpRules 또는 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="9acd2-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9acd2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9acd2-104">SYNTAX</span></span>

### <span data-ttu-id="9acd2-105">NetWorkRuleString (기본값)</span><span class="sxs-lookup"><span data-stu-id="9acd2-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9acd2-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="9acd2-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9acd2-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9acd2-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9acd2-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="9acd2-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9acd2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9acd2-109">DESCRIPTION</span></span>
<span data-ttu-id="9acd2-110">**AzCognitiveServicesAccountNetworkRule** Cmdlet은 인지 서비스 계정의 networkrule 속성에서 IpRules 또는 VirtualNetworkRules을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="9acd2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9acd2-111">EXAMPLES</span></span>

### <span data-ttu-id="9acd2-112">예제 1: IPAddressOrRange를 사용 하 여 여러 IpRules 제거</span><span class="sxs-lookup"><span data-stu-id="9acd2-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="9acd2-113">이 명령은 IPAddressOrRange로 여러 IpRules를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="9acd2-114">예제 2: JSON을 사용 하 여 VirtualNetworkRule 개체 입력을 사용 하 여 VirtualNetworkRule 제거</span><span class="sxs-lookup"><span data-stu-id="9acd2-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="9acd2-115">이 명령은 JSON에서 VirtualNetworkRule 개체 입력을 사용 하 여 VirtualNetworkRule를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="9acd2-116">예제 3: 파이프라인을 사용 하 여 첫 번째 IpRule 제거</span><span class="sxs-lookup"><span data-stu-id="9acd2-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="9acd2-117">이 명령은 파이프라인을 사용 하 여 첫 번째 IpRule를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="9acd2-118">예제 4: VirtualNetworkResourceID를 사용 하 여 여러 VirtualNetworkRules 제거</span><span class="sxs-lookup"><span data-stu-id="9acd2-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="9acd2-119">이 명령은 VirtualNetworkResourceID로 여러 VirtualNetworkRules를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="9acd2-120">변수</span><span class="sxs-lookup"><span data-stu-id="9acd2-120">PARAMETERS</span></span>

### <span data-ttu-id="9acd2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acd2-121">-DefaultProfile</span></span>
<span data-ttu-id="9acd2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9acd2-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9acd2-123">-IpAddressOrRange</span></span>
<span data-ttu-id="9acd2-124">인지 서비스 계정 네트워크 규칙 IpRules IpAddressOrRange in 문자열.</span><span class="sxs-lookup"><span data-stu-id="9acd2-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="9acd2-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="9acd2-125">-IpRule</span></span>
<span data-ttu-id="9acd2-126">인지 서비스 계정 네트워크 규칙 IpRules.</span><span class="sxs-lookup"><span data-stu-id="9acd2-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="9acd2-127">-이름</span><span class="sxs-lookup"><span data-stu-id="9acd2-127">-Name</span></span>
<span data-ttu-id="9acd2-128">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="9acd2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9acd2-129">-ResourceGroupName</span></span>
<span data-ttu-id="9acd2-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="9acd2-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9acd2-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9acd2-132">인지 서비스 계정 네트워크 규칙 VirtualNetworkRules VirtualNetworkResourceId in 문자열.</span><span class="sxs-lookup"><span data-stu-id="9acd2-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="9acd2-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9acd2-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="9acd2-134">인지 서비스 계정 네트워크 규칙 VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="9acd2-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="9acd2-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9acd2-135">-Confirm</span></span>
<span data-ttu-id="9acd2-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9acd2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9acd2-137">-WhatIf</span></span>
<span data-ttu-id="9acd2-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9acd2-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9acd2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acd2-140">CommonParameters</span></span>
<span data-ttu-id="9acd2-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acd2-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9acd2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acd2-143">입력</span><span class="sxs-lookup"><span data-stu-id="9acd2-143">INPUTS</span></span>

### <span data-ttu-id="9acd2-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9acd2-144">System.String</span></span>

### <span data-ttu-id="9acd2-145">CognitiveServices를 PSIpRule []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="9acd2-146">CognitiveServices를 PSVirtualNetworkRule []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9acd2-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="9acd2-147">출력</span><span class="sxs-lookup"><span data-stu-id="9acd2-147">OUTPUTS</span></span>

### <span data-ttu-id="9acd2-148">CognitiveServices. PSVirtualNetworkRule/. \*</span><span class="sxs-lookup"><span data-stu-id="9acd2-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="9acd2-149">CognitiveServices. PSIpRule/. \*</span><span class="sxs-lookup"><span data-stu-id="9acd2-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="9acd2-150">상속자</span><span class="sxs-lookup"><span data-stu-id="9acd2-150">NOTES</span></span>

## <span data-ttu-id="9acd2-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9acd2-151">RELATED LINKS</span></span>
