---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219203"
---
# <span data-ttu-id="15df7-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="15df7-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="15df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15df7-102">SYNOPSIS</span></span>
<span data-ttu-id="15df7-103">인지 서비스 계정의 NetworkRule 속성에 IpRules 또는 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="15df7-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="15df7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15df7-104">SYNTAX</span></span>

### <span data-ttu-id="15df7-105">NetWorkRuleString (기본값)</span><span class="sxs-lookup"><span data-stu-id="15df7-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15df7-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="15df7-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15df7-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="15df7-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15df7-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="15df7-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15df7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="15df7-109">DESCRIPTION</span></span>
<span data-ttu-id="15df7-110">**AzCognitiveServicesAccountNetworkRule** Cmdlet은 인지 서비스 계정의 networkrule 속성에 IpRules 또는 VirtualNetworkRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="15df7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="15df7-111">EXAMPLES</span></span>

### <span data-ttu-id="15df7-112">예제 1: IpAddressOrRange를 사용 하 여 여러 IpRules 추가</span><span class="sxs-lookup"><span data-stu-id="15df7-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="15df7-113">이 명령은 IpAddressOrRange로 여러 IpRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="15df7-114">예제 2: VirtualNetworkResourceID를 사용 하 여 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="15df7-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="15df7-115">이 명령은 VirtualNetworkResourceID를 사용 하 여 VirtualNetworkRule를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="15df7-116">예제 3: 다른 계정의 VirtualNetworkRule 개체를 사용 하 여 VirtualNetworkRules 추가</span><span class="sxs-lookup"><span data-stu-id="15df7-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="15df7-117">이 명령은 다른 계정의 VirtualNetworkRule 개체를 사용 하 여 VirtualNetworkRules를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="15df7-118">예제 4: IpRule 개체를 사용 하 여 여러 IpRule 추가, JSON으로 입력</span><span class="sxs-lookup"><span data-stu-id="15df7-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="15df7-119">이 명령은 IpRule 개체를 사용 하 여 여러 IpRule를 추가 하 고 JSON으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="15df7-120">변수</span><span class="sxs-lookup"><span data-stu-id="15df7-120">PARAMETERS</span></span>

### <span data-ttu-id="15df7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15df7-121">-DefaultProfile</span></span>
<span data-ttu-id="15df7-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15df7-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="15df7-123">-IpAddressOrRange</span></span>
<span data-ttu-id="15df7-124">인지 서비스 계정 네트워크 규칙 IpRules IpAddressOrRange in 문자열.</span><span class="sxs-lookup"><span data-stu-id="15df7-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="15df7-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="15df7-125">-IpRule</span></span>
<span data-ttu-id="15df7-126">인지 서비스 계정 네트워크 규칙 IpRules.</span><span class="sxs-lookup"><span data-stu-id="15df7-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="15df7-127">-이름</span><span class="sxs-lookup"><span data-stu-id="15df7-127">-Name</span></span>
<span data-ttu-id="15df7-128">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="15df7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15df7-129">-ResourceGroupName</span></span>
<span data-ttu-id="15df7-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="15df7-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="15df7-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="15df7-132">인지 서비스 계정 네트워크 규칙 VirtualNetworkRules VirtualNetworkResourceId in 문자열.</span><span class="sxs-lookup"><span data-stu-id="15df7-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="15df7-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="15df7-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="15df7-134">인지 서비스 계정 네트워크 규칙 VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="15df7-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="15df7-135">-확인</span><span class="sxs-lookup"><span data-stu-id="15df7-135">-Confirm</span></span>
<span data-ttu-id="15df7-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15df7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15df7-137">-WhatIf</span></span>
<span data-ttu-id="15df7-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15df7-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15df7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15df7-140">CommonParameters</span></span>
<span data-ttu-id="15df7-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15df7-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15df7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15df7-143">입력</span><span class="sxs-lookup"><span data-stu-id="15df7-143">INPUTS</span></span>

### <span data-ttu-id="15df7-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15df7-144">System.String</span></span>

### <span data-ttu-id="15df7-145">CognitiveServices를 PSIpRule []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="15df7-146">CognitiveServices를 PSVirtualNetworkRule []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="15df7-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="15df7-147">출력</span><span class="sxs-lookup"><span data-stu-id="15df7-147">OUTPUTS</span></span>

### <span data-ttu-id="15df7-148">CognitiveServices. PSVirtualNetworkRule/. \*</span><span class="sxs-lookup"><span data-stu-id="15df7-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="15df7-149">CognitiveServices. PSIpRule/. \*</span><span class="sxs-lookup"><span data-stu-id="15df7-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="15df7-150">상속자</span><span class="sxs-lookup"><span data-stu-id="15df7-150">NOTES</span></span>

## <span data-ttu-id="15df7-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15df7-151">RELATED LINKS</span></span>
