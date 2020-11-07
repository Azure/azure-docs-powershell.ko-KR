---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883018"
---
# <span data-ttu-id="f9def-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9def-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f9def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9def-102">SYNOPSIS</span></span>
<span data-ttu-id="f9def-103">경로 필터에 경로 필터 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9def-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9def-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9def-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f9def-105">DESCRIPTION</span></span>
<span data-ttu-id="f9def-106">Add-AzureRmRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 경로 필터 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="f9def-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f9def-107">EXAMPLES</span></span>

### <span data-ttu-id="f9def-108">--------------------------예제 1: 경로 필터에 경로 필터 규칙 추가--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9def-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="f9def-109">첫 번째 명령은 Get-AzureRmRouteFilter cmdlet을 사용 하 여 routefilter01 이라는 경로 필터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="f9def-110">명령이 $RouteFilter 변수에 필터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="f9def-111">변수</span><span class="sxs-lookup"><span data-stu-id="f9def-111">PARAMETERS</span></span>

### <span data-ttu-id="f9def-112">-Access</span><span class="sxs-lookup"><span data-stu-id="f9def-112">-Access</span></span>
<span data-ttu-id="f9def-113">경로 필터 규칙의 액세스를 지정 하 고, 유효한 값은 거부 또는 허용입니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f9def-114">-CommunityList</span></span>
<span data-ttu-id="f9def-115">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="f9def-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9def-116">-DefaultProfile</span></span>
<span data-ttu-id="f9def-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f9def-118">-Force</span></span>
<span data-ttu-id="f9def-119">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="f9def-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f9def-120">-Name</span></span>
<span data-ttu-id="f9def-121">경로 필터에 추가할 경로 필터 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9def-122">-RouteFilter</span></span>
<span data-ttu-id="f9def-123">이 cmdlet이 경로 필터 규칙을 추가 하는 경로 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f9def-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="f9def-125">경로 필터 규칙 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="f9def-126">유효한 값은 다음과 같습니다. 커뮤니티</span><span class="sxs-lookup"><span data-stu-id="f9def-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f9def-127">-Confirm</span></span>
<span data-ttu-id="f9def-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9def-129">-WhatIf</span></span>
<span data-ttu-id="f9def-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9def-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9def-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9def-132">CommonParameters</span></span>
<span data-ttu-id="f9def-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9def-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9def-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9def-135">입력</span><span class="sxs-lookup"><span data-stu-id="f9def-135">INPUTS</span></span>

### <span data-ttu-id="f9def-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9def-136">PSRouteFilter</span></span>
<span data-ttu-id="f9def-137">' RouteFilter ' 매개 변수는 파이프라인에서 ' PSRouteFilter ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9def-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="f9def-138">출력</span><span class="sxs-lookup"><span data-stu-id="f9def-138">OUTPUTS</span></span>

### <span data-ttu-id="f9def-139">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f9def-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f9def-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f9def-140">NOTES</span></span>
<span data-ttu-id="f9def-141">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="f9def-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f9def-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9def-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9def-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9def-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="f9def-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9def-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)







[<span data-ttu-id="f9def-145">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9def-145">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

