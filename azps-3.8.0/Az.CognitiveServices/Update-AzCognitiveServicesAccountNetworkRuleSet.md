---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 5c01b692e47c3d246982be353093c436a91d6b64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033761"
---
# <span data-ttu-id="80d18-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="80d18-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="80d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d18-102">SYNOPSIS</span></span>
<span data-ttu-id="80d18-103">인지 서비스 계정의 NetworkRule 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="80d18-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="80d18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80d18-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80d18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80d18-105">DESCRIPTION</span></span>
<span data-ttu-id="80d18-106">**AzCognitiveServicesAccountNetworkRuleSet** Cmdlet은 인지 서비스 계정의 networkrule 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="80d18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80d18-107">EXAMPLES</span></span>

### <span data-ttu-id="80d18-108">예제 1: NetworkRule의 모든 속성 업데이트, JSON을 사용 하 여 입력 규칙</span><span class="sxs-lookup"><span data-stu-id="80d18-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="80d18-109">이 명령은 모든 NetworkRule의 속성, JSON으로 입력 하는 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="80d18-110">예제 2: NetworkRule의 업데이트 무시 속성</span><span class="sxs-lookup"><span data-stu-id="80d18-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="80d18-111">이 명령은 NetworkRule의 Bypass 속성을 업데이트 합니다 (다른 속성은 변경 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="80d18-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="80d18-112">예제 3: 인지 서비스 계정의 NetworkRule 규칙 정리</span><span class="sxs-lookup"><span data-stu-id="80d18-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="80d18-113">이 명령은 인지 서비스 계정의 NetworkRule 규칙을 정리 합니다 (다른 속성은 변경 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="80d18-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="80d18-114">변수</span><span class="sxs-lookup"><span data-stu-id="80d18-114">PARAMETERS</span></span>

### <span data-ttu-id="80d18-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="80d18-115">-DefaultAction</span></span>
<span data-ttu-id="80d18-116">인지 서비스 계정 네트워크 규칙 DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="80d18-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

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

### <span data-ttu-id="80d18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d18-117">-DefaultProfile</span></span>
<span data-ttu-id="80d18-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80d18-119">-IpRule</span><span class="sxs-lookup"><span data-stu-id="80d18-119">-IpRule</span></span>
<span data-ttu-id="80d18-120">인지 서비스 계정 네트워크 규칙 IpRules.</span><span class="sxs-lookup"><span data-stu-id="80d18-120">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="80d18-121">-이름</span><span class="sxs-lookup"><span data-stu-id="80d18-121">-Name</span></span>
<span data-ttu-id="80d18-122">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-122">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="80d18-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d18-123">-ResourceGroupName</span></span>
<span data-ttu-id="80d18-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="80d18-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="80d18-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="80d18-126">인지 서비스 계정 네트워크 규칙 VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="80d18-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="80d18-127">-확인</span><span class="sxs-lookup"><span data-stu-id="80d18-127">-Confirm</span></span>
<span data-ttu-id="80d18-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d18-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d18-129">-WhatIf</span></span>
<span data-ttu-id="80d18-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d18-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d18-132">CommonParameters</span></span>
<span data-ttu-id="80d18-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d18-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80d18-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d18-135">입력</span><span class="sxs-lookup"><span data-stu-id="80d18-135">INPUTS</span></span>

### <span data-ttu-id="80d18-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80d18-136">System.String</span></span>

### <span data-ttu-id="80d18-137">CognitiveServices를 PSIpRule []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="80d18-138">CognitiveServices를 PSVirtualNetworkRule []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="80d18-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="80d18-139">출력</span><span class="sxs-lookup"><span data-stu-id="80d18-139">OUTPUTS</span></span>

### <span data-ttu-id="80d18-140">CognitiveServices. a m m 네트워크 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="80d18-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="80d18-141">상속자</span><span class="sxs-lookup"><span data-stu-id="80d18-141">NOTES</span></span>

## <span data-ttu-id="80d18-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80d18-142">RELATED LINKS</span></span>
