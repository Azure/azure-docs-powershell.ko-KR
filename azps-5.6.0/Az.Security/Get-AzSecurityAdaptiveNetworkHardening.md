---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: 87b53048ede0a5b2484da18ccd0a2f6a531aa92b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008571"
---
# <span data-ttu-id="23d24-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="23d24-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="23d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d24-102">SYNOPSIS</span></span>
<span data-ttu-id="23d24-103">확장된 리소스의 범위에서 Adaptive Network Hardenings 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="23d24-104">구문</span><span class="sxs-lookup"><span data-stu-id="23d24-104">SYNTAX</span></span>

### <span data-ttu-id="23d24-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="23d24-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="23d24-106">설명</span><span class="sxs-lookup"><span data-stu-id="23d24-106">DESCRIPTION</span></span>
<span data-ttu-id="23d24-107">적응형 네트워크 강화는 Azure Security Center에서 자동으로 계산되며, 이 cmdlet을 사용하여 확장된 리소스 범위의 Adaptive Network Hardenings 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="23d24-108">예제</span><span class="sxs-lookup"><span data-stu-id="23d24-108">EXAMPLES</span></span>

### <span data-ttu-id="23d24-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="23d24-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="23d24-110">확장된 리소스의 범위에서 Adaptive Network Hardenings 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="23d24-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="23d24-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="23d24-112">단일 Adaptive Network Hardenings 리소스 사용</span><span class="sxs-lookup"><span data-stu-id="23d24-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="23d24-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="23d24-113">PARAMETERS</span></span>

### <span data-ttu-id="23d24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d24-114">-DefaultProfile</span></span>
<span data-ttu-id="23d24-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d24-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d24-116">-ResourceGroupName</span></span>
<span data-ttu-id="23d24-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-117">Resource group name.</span></span>

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

### <span data-ttu-id="23d24-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="23d24-118">-ResourceName</span></span>
<span data-ttu-id="23d24-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-119">Resource name.</span></span>

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

### <span data-ttu-id="23d24-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="23d24-120">-ResourceNamespace</span></span>
<span data-ttu-id="23d24-121">리소스의 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="23d24-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="23d24-122">-ResourceType</span></span>
<span data-ttu-id="23d24-123">리소스의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-123">The type of the resource.</span></span>

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

### <span data-ttu-id="23d24-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="23d24-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="23d24-125">적응 네트워크 경화 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="23d24-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23d24-126">-SubscriptionId</span></span>
<span data-ttu-id="23d24-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="23d24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d24-128">CommonParameters</span></span>
<span data-ttu-id="23d24-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23d24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d24-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="23d24-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d24-131">입력</span><span class="sxs-lookup"><span data-stu-id="23d24-131">INPUTS</span></span>

### <span data-ttu-id="23d24-132">System.String</span><span class="sxs-lookup"><span data-stu-id="23d24-132">System.String</span></span>

## <span data-ttu-id="23d24-133">출력</span><span class="sxs-lookup"><span data-stu-id="23d24-133">OUTPUTS</span></span>

### <span data-ttu-id="23d24-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="23d24-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="23d24-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23d24-135">NOTES</span></span>

## <span data-ttu-id="23d24-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23d24-136">RELATED LINKS</span></span>