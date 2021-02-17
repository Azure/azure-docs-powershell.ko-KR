---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208344"
---
# <span data-ttu-id="5ecbe-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="5ecbe-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="5ecbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ecbe-102">SYNOPSIS</span></span>
<span data-ttu-id="5ecbe-103">확장된 리소스의 범위에서 적응 네트워크 보안 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="5ecbe-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ecbe-104">SYNTAX</span></span>

### <span data-ttu-id="5ecbe-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5ecbe-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="5ecbe-106">설명</span><span class="sxs-lookup"><span data-stu-id="5ecbe-106">DESCRIPTION</span></span>
<span data-ttu-id="5ecbe-107">적응 네트워크 강화는 Azure Security Center에서 자동으로 계산됩니다. 이 cmdlet을 사용하여 확장된 리소스 범위에서 적응 네트워크 강화 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="5ecbe-108">예제</span><span class="sxs-lookup"><span data-stu-id="5ecbe-108">EXAMPLES</span></span>

### <span data-ttu-id="5ecbe-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ecbe-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="5ecbe-110">확장된 리소스의 범위에서 적응 네트워크 보안 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="5ecbe-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="5ecbe-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="5ecbe-112">단일 Adaptive Network Hardenings 리소스 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="5ecbe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ecbe-113">PARAMETERS</span></span>

### <span data-ttu-id="5ecbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ecbe-114">-DefaultProfile</span></span>
<span data-ttu-id="5ecbe-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ecbe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ecbe-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ecbe-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-117">Resource group name.</span></span>

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

### <span data-ttu-id="5ecbe-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5ecbe-118">-ResourceName</span></span>
<span data-ttu-id="5ecbe-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-119">Resource name.</span></span>

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

### <span data-ttu-id="5ecbe-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="5ecbe-120">-ResourceNamespace</span></span>
<span data-ttu-id="5ecbe-121">리소스의 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="5ecbe-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5ecbe-122">-ResourceType</span></span>
<span data-ttu-id="5ecbe-123">리소스의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-123">The type of the resource.</span></span>

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

### <span data-ttu-id="5ecbe-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="5ecbe-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="5ecbe-125">적응 네트워크 보안 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ecbe-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ecbe-126">-SubscriptionId</span></span>
<span data-ttu-id="5ecbe-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="5ecbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ecbe-128">CommonParameters</span></span>
<span data-ttu-id="5ecbe-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ecbe-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5ecbe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ecbe-131">입력</span><span class="sxs-lookup"><span data-stu-id="5ecbe-131">INPUTS</span></span>

### <span data-ttu-id="5ecbe-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5ecbe-132">System.String</span></span>

## <span data-ttu-id="5ecbe-133">출력</span><span class="sxs-lookup"><span data-stu-id="5ecbe-133">OUTPUTS</span></span>

### <span data-ttu-id="5ecbe-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="5ecbe-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="5ecbe-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ecbe-135">NOTES</span></span>

## <span data-ttu-id="5ecbe-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ecbe-136">RELATED LINKS</span></span>