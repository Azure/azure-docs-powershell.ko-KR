---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875660"
---
# <span data-ttu-id="cf85a-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf85a-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="cf85a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf85a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf85a-103">경로 필터에 경로 필터 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="cf85a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf85a-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf85a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cf85a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf85a-106">Add-AzRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 경로 필터 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="cf85a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cf85a-107">EXAMPLES</span></span>

### <span data-ttu-id="cf85a-108">--------------------------예제 1: 경로 필터에 경로 필터 규칙 추가--------------------------</span><span class="sxs-lookup"><span data-stu-id="cf85a-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="cf85a-109">첫 번째 명령은 Get-AzRouteFilter cmdlet을 사용 하 여 routefilter01 이라는 경로 필터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="cf85a-110">명령이 $RouteFilter 변수에 필터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="cf85a-111">변수</span><span class="sxs-lookup"><span data-stu-id="cf85a-111">PARAMETERS</span></span>

### <span data-ttu-id="cf85a-112">-Access</span><span class="sxs-lookup"><span data-stu-id="cf85a-112">-Access</span></span>
<span data-ttu-id="cf85a-113">경로 필터 규칙의 액세스를 지정 하 고, 유효한 값은 거부 또는 허용입니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="cf85a-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="cf85a-114">-CommunityList</span></span>
<span data-ttu-id="cf85a-115">경로 필터가 필터링 할 커뮤니티 값 목록</span><span class="sxs-lookup"><span data-stu-id="cf85a-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="cf85a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf85a-116">-DefaultProfile</span></span>
<span data-ttu-id="cf85a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf85a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cf85a-118">-Force</span></span>
<span data-ttu-id="cf85a-119">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="cf85a-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="cf85a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="cf85a-120">-Name</span></span>
<span data-ttu-id="cf85a-121">경로 필터에 추가할 경로 필터 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="cf85a-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf85a-122">-RouteFilter</span></span>
<span data-ttu-id="cf85a-123">이 cmdlet이 경로 필터 규칙을 추가 하는 경로 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="cf85a-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="cf85a-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="cf85a-125">경로 필터 규칙 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="cf85a-126">유효한 값은 다음과 같습니다. 커뮤니티</span><span class="sxs-lookup"><span data-stu-id="cf85a-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="cf85a-127">-확인</span><span class="sxs-lookup"><span data-stu-id="cf85a-127">-Confirm</span></span>
<span data-ttu-id="cf85a-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf85a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf85a-129">-WhatIf</span></span>
<span data-ttu-id="cf85a-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf85a-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf85a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf85a-132">CommonParameters</span></span>
<span data-ttu-id="cf85a-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf85a-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf85a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf85a-135">입력</span><span class="sxs-lookup"><span data-stu-id="cf85a-135">INPUTS</span></span>

### <span data-ttu-id="cf85a-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf85a-136">PSRouteFilter</span></span>
<span data-ttu-id="cf85a-137">' RouteFilter ' 매개 변수는 파이프라인에서 ' PSRouteFilter ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf85a-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="cf85a-138">출력</span><span class="sxs-lookup"><span data-stu-id="cf85a-138">OUTPUTS</span></span>

### <span data-ttu-id="cf85a-139">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cf85a-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cf85a-140">상속자</span><span class="sxs-lookup"><span data-stu-id="cf85a-140">NOTES</span></span>
<span data-ttu-id="cf85a-141">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="cf85a-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cf85a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf85a-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf85a-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf85a-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cf85a-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf85a-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="cf85a-145">새로운 AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="cf85a-145">New-AzRouteFilterRuleConfigConfig</span></span>](./New-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="cf85a-146">제거-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="cf85a-146">Remove-AzRouteFilterRuleConfigConfig</span></span>](./Remove-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="cf85a-147">Set-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="cf85a-147">Set-AzRouteFilterRuleConfigConfig</span></span>](./Set-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="cf85a-148">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf85a-148">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

