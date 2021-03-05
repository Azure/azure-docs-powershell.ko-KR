---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 0c6fa8b973af2f2ab4a9c8547dddffda18eb15c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990901"
---
# <span data-ttu-id="10a98-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="10a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a98-102">SYNOPSIS</span></span>
<span data-ttu-id="10a98-103">경로 필터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-103">Updates a route filter.</span></span>

## <span data-ttu-id="10a98-104">구문</span><span class="sxs-lookup"><span data-stu-id="10a98-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a98-105">설명</span><span class="sxs-lookup"><span data-stu-id="10a98-105">DESCRIPTION</span></span>
<span data-ttu-id="10a98-106">**Set-AzApplicationGateway** cmdlet은 경로 필터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="10a98-107">예제</span><span class="sxs-lookup"><span data-stu-id="10a98-107">EXAMPLES</span></span>

### <span data-ttu-id="10a98-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="10a98-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="10a98-109">이 명령은 경로 필터를 $rf 설정으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="10a98-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="10a98-110">PARAMETERS</span></span>

### <span data-ttu-id="10a98-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10a98-111">-AsJob</span></span>
<span data-ttu-id="10a98-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="10a98-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10a98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a98-113">-DefaultProfile</span></span>
<span data-ttu-id="10a98-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a98-115">-Force</span><span class="sxs-lookup"><span data-stu-id="10a98-115">-Force</span></span>
<span data-ttu-id="10a98-116">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="10a98-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-117">-RouteFilter</span></span>
<span data-ttu-id="10a98-118">The RouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-118">The RouteFilter</span></span>

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

### <span data-ttu-id="10a98-119">-확인</span><span class="sxs-lookup"><span data-stu-id="10a98-119">-Confirm</span></span>
<span data-ttu-id="10a98-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a98-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a98-121">-WhatIf</span></span>
<span data-ttu-id="10a98-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10a98-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a98-124">CommonParameters</span></span>
<span data-ttu-id="10a98-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10a98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a98-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="10a98-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a98-127">입력</span><span class="sxs-lookup"><span data-stu-id="10a98-127">INPUTS</span></span>

### <span data-ttu-id="10a98-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="10a98-129">출력</span><span class="sxs-lookup"><span data-stu-id="10a98-129">OUTPUTS</span></span>

### <span data-ttu-id="10a98-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="10a98-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10a98-131">NOTES</span></span>

## <span data-ttu-id="10a98-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10a98-132">RELATED LINKS</span></span>

[<span data-ttu-id="10a98-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="10a98-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="10a98-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="10a98-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="10a98-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a98-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="10a98-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a98-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="10a98-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a98-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="10a98-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a98-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="10a98-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10a98-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
