---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496471"
---
# <span data-ttu-id="d371b-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="d371b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d371b-102">SYNOPSIS</span></span>
<span data-ttu-id="d371b-103">경로 필터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-103">Updates a route filter.</span></span>

## <span data-ttu-id="d371b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d371b-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d371b-105">설명</span><span class="sxs-lookup"><span data-stu-id="d371b-105">DESCRIPTION</span></span>
<span data-ttu-id="d371b-106">**Set-AzApplicationGateway** cmdlet은 경로 필터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="d371b-107">예제</span><span class="sxs-lookup"><span data-stu-id="d371b-107">EXAMPLES</span></span>

### <span data-ttu-id="d371b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d371b-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="d371b-109">이 명령은 경로 필터를 경로 변수의 설정으로 $rf 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="d371b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d371b-110">PARAMETERS</span></span>

### <span data-ttu-id="d371b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d371b-111">-AsJob</span></span>
<span data-ttu-id="d371b-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d371b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d371b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d371b-113">-DefaultProfile</span></span>
<span data-ttu-id="d371b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d371b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d371b-115">-Force</span></span>
<span data-ttu-id="d371b-116">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d371b-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-117">-RouteFilter</span></span>
<span data-ttu-id="d371b-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d371b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d371b-119">-Confirm</span></span>
<span data-ttu-id="d371b-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d371b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d371b-121">-WhatIf</span></span>
<span data-ttu-id="d371b-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d371b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d371b-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d371b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d371b-124">CommonParameters</span></span>
<span data-ttu-id="d371b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d371b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d371b-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d371b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d371b-127">입력</span><span class="sxs-lookup"><span data-stu-id="d371b-127">INPUTS</span></span>

### <span data-ttu-id="d371b-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d371b-129">출력</span><span class="sxs-lookup"><span data-stu-id="d371b-129">OUTPUTS</span></span>

### <span data-ttu-id="d371b-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d371b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d371b-131">NOTES</span></span>

## <span data-ttu-id="d371b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d371b-132">RELATED LINKS</span></span>

[<span data-ttu-id="d371b-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="d371b-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="d371b-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d371b-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="d371b-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d371b-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d371b-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d371b-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d371b-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d371b-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d371b-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d371b-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="d371b-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d371b-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
