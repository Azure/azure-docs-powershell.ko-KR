---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495055"
---
# <span data-ttu-id="a53e2-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="a53e2-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="a53e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a53e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a53e2-103">요청에 나열된 NSG에 대해 주어진 규칙을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="a53e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="a53e2-104">SYNTAX</span></span>

### <span data-ttu-id="a53e2-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="a53e2-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a53e2-106">설명</span><span class="sxs-lookup"><span data-stu-id="a53e2-106">DESCRIPTION</span></span>
<span data-ttu-id="a53e2-107">적응 네트워크 강화는 Azure Security Center에서 자동으로 계산됩니다. 이 cmdlet을 사용하여 요청에 나열된 NSG에 대해 주어진 규칙을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="a53e2-108">예제</span><span class="sxs-lookup"><span data-stu-id="a53e2-108">EXAMPLES</span></span>

### <span data-ttu-id="a53e2-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a53e2-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="a53e2-110">요청에 나열된 NSG에 대해 주어진 규칙을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="a53e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a53e2-111">PARAMETERS</span></span>

### <span data-ttu-id="a53e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a53e2-112">-DefaultProfile</span></span>
<span data-ttu-id="a53e2-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a53e2-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="a53e2-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="a53e2-115">적응 네트워크 보안 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a53e2-116">-ResourceGroupName</span></span>
<span data-ttu-id="a53e2-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a53e2-118">-ResourceName</span></span>
<span data-ttu-id="a53e2-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="a53e2-120">-ResourceNamespace</span></span>
<span data-ttu-id="a53e2-121">리소스의 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a53e2-122">-ResourceType</span></span>
<span data-ttu-id="a53e2-123">리소스의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a53e2-124">-SubscriptionId</span></span>
<span data-ttu-id="a53e2-125">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-126">-Rules</span><span class="sxs-lookup"><span data-stu-id="a53e2-126">-Rules</span></span>
<span data-ttu-id="a53e2-127">적용할 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="a53e2-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="a53e2-129">적응 네트워크 강화 규칙에서 만든 보안 규칙으로 업데이트될 효과적인 네트워크 보안 그룹의 Azure 리소스 신분입니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53e2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a53e2-130">-PassThru</span></span>
<span data-ttu-id="a53e2-131">성공 또는 실패를 나타내는 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="a53e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53e2-132">CommonParameters</span></span>
<span data-ttu-id="a53e2-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a53e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53e2-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a53e2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53e2-135">입력</span><span class="sxs-lookup"><span data-stu-id="a53e2-135">INPUTS</span></span>

### <span data-ttu-id="a53e2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a53e2-136">System.String</span></span>

### <span data-ttu-id="a53e2-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="a53e2-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="a53e2-138">출력</span><span class="sxs-lookup"><span data-stu-id="a53e2-138">OUTPUTS</span></span>

### <span data-ttu-id="a53e2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a53e2-139">System.Boolean</span></span>

## <span data-ttu-id="a53e2-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a53e2-140">NOTES</span></span>

## <span data-ttu-id="a53e2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a53e2-141">RELATED LINKS</span></span>