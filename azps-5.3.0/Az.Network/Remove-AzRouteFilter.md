---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496620"
---
# <span data-ttu-id="44a60-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44a60-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="44a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44a60-102">SYNOPSIS</span></span>
<span data-ttu-id="44a60-103">경로 필터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-103">Removes a route filter.</span></span>

## <span data-ttu-id="44a60-104">구문</span><span class="sxs-lookup"><span data-stu-id="44a60-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44a60-105">설명</span><span class="sxs-lookup"><span data-stu-id="44a60-105">DESCRIPTION</span></span>
<span data-ttu-id="44a60-106">**Remove-AzRouteFilter** cmdlet은 경로 필터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="44a60-107">예제</span><span class="sxs-lookup"><span data-stu-id="44a60-107">EXAMPLES</span></span>

### <span data-ttu-id="44a60-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="44a60-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="44a60-109">이 명령은 ResourceGroup01이라는 리소스 그룹에서 RouteFilter01이라는 경로 필터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="44a60-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44a60-110">PARAMETERS</span></span>

### <span data-ttu-id="44a60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a60-111">-DefaultProfile</span></span>
<span data-ttu-id="44a60-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44a60-113">-Force</span><span class="sxs-lookup"><span data-stu-id="44a60-113">-Force</span></span>
<span data-ttu-id="44a60-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="44a60-115">-Name</span><span class="sxs-lookup"><span data-stu-id="44a60-115">-Name</span></span>
<span data-ttu-id="44a60-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a60-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44a60-117">-PassThru</span></span>
<span data-ttu-id="44a60-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="44a60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a60-119">-ResourceGroupName</span></span>
<span data-ttu-id="44a60-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a60-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44a60-121">-Confirm</span></span>
<span data-ttu-id="44a60-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44a60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44a60-123">-WhatIf</span></span>
<span data-ttu-id="44a60-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="44a60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44a60-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44a60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a60-126">CommonParameters</span></span>
<span data-ttu-id="44a60-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44a60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a60-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44a60-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a60-129">입력</span><span class="sxs-lookup"><span data-stu-id="44a60-129">INPUTS</span></span>

### <span data-ttu-id="44a60-130">System.String</span><span class="sxs-lookup"><span data-stu-id="44a60-130">System.String</span></span>

## <span data-ttu-id="44a60-131">출력</span><span class="sxs-lookup"><span data-stu-id="44a60-131">OUTPUTS</span></span>

### <span data-ttu-id="44a60-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44a60-132">System.Boolean</span></span>

## <span data-ttu-id="44a60-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44a60-133">NOTES</span></span>

## <span data-ttu-id="44a60-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44a60-134">RELATED LINKS</span></span>

[<span data-ttu-id="44a60-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44a60-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="44a60-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44a60-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="44a60-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="44a60-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="44a60-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44a60-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="44a60-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44a60-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="44a60-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44a60-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="44a60-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44a60-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="44a60-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44a60-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
