---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 8f48cf6fb5b3c4489a116ef0f7ee5a32649d96ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869681"
---
# <span data-ttu-id="4d07a-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4d07a-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="4d07a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d07a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d07a-103">경로 필터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-103">Removes a route filter.</span></span>

## <span data-ttu-id="4d07a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d07a-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d07a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4d07a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d07a-106">**AzRouteFilter** cmdlet은 경로 필터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="4d07a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4d07a-107">EXAMPLES</span></span>

### <span data-ttu-id="4d07a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d07a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4d07a-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 RouteFilter01 이라는 경로 필터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4d07a-110">변수</span><span class="sxs-lookup"><span data-stu-id="4d07a-110">PARAMETERS</span></span>

### <span data-ttu-id="4d07a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d07a-111">-DefaultProfile</span></span>
<span data-ttu-id="4d07a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d07a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4d07a-113">-Force</span></span>
<span data-ttu-id="4d07a-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4d07a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4d07a-115">-Name</span></span>
<span data-ttu-id="4d07a-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-116">The resource name.</span></span>

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

### <span data-ttu-id="4d07a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d07a-117">-PassThru</span></span>
<span data-ttu-id="4d07a-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="4d07a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d07a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d07a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-120">The resource group name.</span></span>

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

### <span data-ttu-id="4d07a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="4d07a-121">-Confirm</span></span>
<span data-ttu-id="4d07a-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d07a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d07a-123">-WhatIf</span></span>
<span data-ttu-id="4d07a-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d07a-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d07a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d07a-126">CommonParameters</span></span>
<span data-ttu-id="4d07a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d07a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d07a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d07a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d07a-129">입력</span><span class="sxs-lookup"><span data-stu-id="4d07a-129">INPUTS</span></span>

### <span data-ttu-id="4d07a-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4d07a-130">System.String</span></span>

## <span data-ttu-id="4d07a-131">출력</span><span class="sxs-lookup"><span data-stu-id="4d07a-131">OUTPUTS</span></span>

### <span data-ttu-id="4d07a-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4d07a-132">System.Boolean</span></span>

## <span data-ttu-id="4d07a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4d07a-133">NOTES</span></span>

## <span data-ttu-id="4d07a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d07a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d07a-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4d07a-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4d07a-136">새로운 AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4d07a-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4d07a-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4d07a-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="4d07a-138">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d07a-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4d07a-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d07a-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4d07a-140">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d07a-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4d07a-141">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d07a-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4d07a-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4d07a-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
