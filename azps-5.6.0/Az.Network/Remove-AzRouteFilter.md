---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 0b75cdb63d2a8bb3c01a93a90ee01db096cf7fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976619"
---
# <span data-ttu-id="93de6-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93de6-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="93de6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93de6-102">SYNOPSIS</span></span>
<span data-ttu-id="93de6-103">경로 필터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-103">Removes a route filter.</span></span>

## <span data-ttu-id="93de6-104">구문</span><span class="sxs-lookup"><span data-stu-id="93de6-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93de6-105">설명</span><span class="sxs-lookup"><span data-stu-id="93de6-105">DESCRIPTION</span></span>
<span data-ttu-id="93de6-106">**Remove-AzRouteFilter** cmdlet은 경로 필터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="93de6-107">예제</span><span class="sxs-lookup"><span data-stu-id="93de6-107">EXAMPLES</span></span>

### <span data-ttu-id="93de6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="93de6-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="93de6-109">명령은 ResourceGroup01이라는 리소스 그룹에서 RouteFilter01이라는 경로 필터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="93de6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="93de6-110">PARAMETERS</span></span>

### <span data-ttu-id="93de6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93de6-111">-DefaultProfile</span></span>
<span data-ttu-id="93de6-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93de6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="93de6-113">-Force</span></span>
<span data-ttu-id="93de6-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="93de6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="93de6-115">-Name</span></span>
<span data-ttu-id="93de6-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-116">The resource name.</span></span>

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

### <span data-ttu-id="93de6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93de6-117">-PassThru</span></span>
<span data-ttu-id="93de6-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="93de6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93de6-119">-ResourceGroupName</span></span>
<span data-ttu-id="93de6-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-120">The resource group name.</span></span>

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

### <span data-ttu-id="93de6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="93de6-121">-Confirm</span></span>
<span data-ttu-id="93de6-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93de6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93de6-123">-WhatIf</span></span>
<span data-ttu-id="93de6-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93de6-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93de6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93de6-126">CommonParameters</span></span>
<span data-ttu-id="93de6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93de6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93de6-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93de6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93de6-129">입력</span><span class="sxs-lookup"><span data-stu-id="93de6-129">INPUTS</span></span>

### <span data-ttu-id="93de6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="93de6-130">System.String</span></span>

## <span data-ttu-id="93de6-131">출력</span><span class="sxs-lookup"><span data-stu-id="93de6-131">OUTPUTS</span></span>

### <span data-ttu-id="93de6-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93de6-132">System.Boolean</span></span>

## <span data-ttu-id="93de6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93de6-133">NOTES</span></span>

## <span data-ttu-id="93de6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93de6-134">RELATED LINKS</span></span>

[<span data-ttu-id="93de6-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93de6-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="93de6-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93de6-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="93de6-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93de6-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="93de6-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93de6-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="93de6-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93de6-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="93de6-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93de6-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="93de6-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93de6-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="93de6-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93de6-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
