---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217539"
---
# <span data-ttu-id="5325a-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="5325a-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="5325a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5325a-102">SYNOPSIS</span></span>
<span data-ttu-id="5325a-103">확장 리소스의 범위에서 적응 네트워크 Hardenings 리소스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="5325a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5325a-104">SYNTAX</span></span>

### <span data-ttu-id="5325a-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5325a-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="5325a-106">설명은</span><span class="sxs-lookup"><span data-stu-id="5325a-106">DESCRIPTION</span></span>
<span data-ttu-id="5325a-107">적응 네트워크 Hardenings Azure 보안 센터에서 자동으로 계산 되며,이 cmdlet을 사용 하 여 확장 리소스의 범위 내에서 적응 네트워크 Hardenings 리소스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="5325a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5325a-108">EXAMPLES</span></span>

### <span data-ttu-id="5325a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="5325a-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="5325a-110">확장 리소스의 범위에서 적응 네트워크 Hardenings 리소스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="5325a-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="5325a-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="5325a-112">단일 적응 네트워크 Hardenings 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="5325a-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="5325a-113">변수</span><span class="sxs-lookup"><span data-stu-id="5325a-113">PARAMETERS</span></span>

### <span data-ttu-id="5325a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5325a-114">-DefaultProfile</span></span>
<span data-ttu-id="5325a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5325a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5325a-116">-ResourceGroupName</span></span>
<span data-ttu-id="5325a-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-117">Resource group name.</span></span>

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

### <span data-ttu-id="5325a-118">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="5325a-118">-ResourceName</span></span>
<span data-ttu-id="5325a-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-119">Resource name.</span></span>

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

### <span data-ttu-id="5325a-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="5325a-120">-ResourceNamespace</span></span>
<span data-ttu-id="5325a-121">리소스의 네임 스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="5325a-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5325a-122">-ResourceType</span></span>
<span data-ttu-id="5325a-123">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-123">The type of the resource.</span></span>

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

### <span data-ttu-id="5325a-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="5325a-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="5325a-125">적응 네트워크 강화 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="5325a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5325a-126">-SubscriptionId</span></span>
<span data-ttu-id="5325a-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="5325a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5325a-128">CommonParameters</span></span>
<span data-ttu-id="5325a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5325a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5325a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5325a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5325a-131">입력</span><span class="sxs-lookup"><span data-stu-id="5325a-131">INPUTS</span></span>

### <span data-ttu-id="5325a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5325a-132">System.String</span></span>

## <span data-ttu-id="5325a-133">출력</span><span class="sxs-lookup"><span data-stu-id="5325a-133">OUTPUTS</span></span>

### <span data-ttu-id="5325a-134">AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="5325a-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="5325a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5325a-135">NOTES</span></span>

## <span data-ttu-id="5325a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5325a-136">RELATED LINKS</span></span>