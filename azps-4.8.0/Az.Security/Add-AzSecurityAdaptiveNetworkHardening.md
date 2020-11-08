---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204368"
---
# <span data-ttu-id="0e84d-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="0e84d-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="0e84d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e84d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e84d-103">요청에 나열 된 NSG (s)에 대 한 지정 된 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="0e84d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e84d-104">SYNTAX</span></span>

### <span data-ttu-id="0e84d-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e84d-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e84d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="0e84d-106">DESCRIPTION</span></span>
<span data-ttu-id="0e84d-107">적응 네트워크 Hardenings Azure 보안 센터에서 자동으로 계산 되며,이 cmdlet을 사용 하 여 요청에 나열 된 NSG (s)에 지정 된 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="0e84d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0e84d-108">EXAMPLES</span></span>

### <span data-ttu-id="0e84d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e84d-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="0e84d-110">요청에 나열 된 NSG (s)에 대 한 지정 된 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="0e84d-111">변수</span><span class="sxs-lookup"><span data-stu-id="0e84d-111">PARAMETERS</span></span>

### <span data-ttu-id="0e84d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e84d-112">-DefaultProfile</span></span>
<span data-ttu-id="0e84d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e84d-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="0e84d-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="0e84d-115">적응 네트워크 강화 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="0e84d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e84d-116">-ResourceGroupName</span></span>
<span data-ttu-id="0e84d-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-117">Resource group name.</span></span>

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

### <span data-ttu-id="0e84d-118">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="0e84d-118">-ResourceName</span></span>
<span data-ttu-id="0e84d-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-119">Resource name.</span></span>

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

### <span data-ttu-id="0e84d-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="0e84d-120">-ResourceNamespace</span></span>
<span data-ttu-id="0e84d-121">리소스의 네임 스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="0e84d-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0e84d-122">-ResourceType</span></span>
<span data-ttu-id="0e84d-123">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-123">The type of the resource.</span></span>

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

### <span data-ttu-id="0e84d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e84d-124">-SubscriptionId</span></span>
<span data-ttu-id="0e84d-125">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="0e84d-126">-규칙</span><span class="sxs-lookup"><span data-stu-id="0e84d-126">-Rules</span></span>
<span data-ttu-id="0e84d-127">적용할 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="0e84d-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="0e84d-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="0e84d-129">적응 네트워크 강화 규칙에서 생성 된 보안 규칙으로 업데이트 되는 효과적인 네트워크 보안 그룹의 Azure 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="0e84d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e84d-130">-PassThru</span></span>
<span data-ttu-id="0e84d-131">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="0e84d-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="0e84d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e84d-132">CommonParameters</span></span>
<span data-ttu-id="0e84d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e84d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e84d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e84d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e84d-135">입력</span><span class="sxs-lookup"><span data-stu-id="0e84d-135">INPUTS</span></span>

### <span data-ttu-id="0e84d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e84d-136">System.String</span></span>

### <span data-ttu-id="0e84d-137">AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="0e84d-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="0e84d-138">출력</span><span class="sxs-lookup"><span data-stu-id="0e84d-138">OUTPUTS</span></span>

### <span data-ttu-id="0e84d-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0e84d-139">System.Boolean</span></span>

## <span data-ttu-id="0e84d-140">상속자</span><span class="sxs-lookup"><span data-stu-id="0e84d-140">NOTES</span></span>

## <span data-ttu-id="0e84d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e84d-141">RELATED LINKS</span></span>