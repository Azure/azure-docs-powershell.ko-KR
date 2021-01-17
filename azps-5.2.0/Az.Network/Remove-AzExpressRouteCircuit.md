---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356686"
---
# <span data-ttu-id="4df7d-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df7d-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4df7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df7d-102">SYNOPSIS</span></span>
<span data-ttu-id="4df7d-103">ExpressRoute 회로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4df7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4df7d-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df7d-105">설명</span><span class="sxs-lookup"><span data-stu-id="4df7d-105">DESCRIPTION</span></span>
<span data-ttu-id="4df7d-106">**Remove-AzExpressRouteCircuit** cmdlet은 ExpressRoute 회로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4df7d-107">예제</span><span class="sxs-lookup"><span data-stu-id="4df7d-107">EXAMPLES</span></span>

### <span data-ttu-id="4df7d-108">예제 1: ExpressRoute 회로 삭제</span><span class="sxs-lookup"><span data-stu-id="4df7d-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="4df7d-109">예제 2: 파이프라인을 사용하여 ExpressRoute 회로 삭제</span><span class="sxs-lookup"><span data-stu-id="4df7d-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="4df7d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df7d-110">PARAMETERS</span></span>

### <span data-ttu-id="4df7d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4df7d-111">-AsJob</span></span>
<span data-ttu-id="4df7d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4df7d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4df7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df7d-113">-DefaultProfile</span></span>
<span data-ttu-id="4df7d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df7d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4df7d-115">-Force</span></span>
<span data-ttu-id="4df7d-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4df7d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4df7d-117">-Name</span></span>
<span data-ttu-id="4df7d-118">제거할 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="4df7d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df7d-119">-PassThru</span></span>
<span data-ttu-id="4df7d-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="4df7d-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4df7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4df7d-123">이 ExpressRoute 회로가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="4df7d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4df7d-124">-Confirm</span></span>
<span data-ttu-id="4df7d-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df7d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df7d-126">-WhatIf</span></span>
<span data-ttu-id="4df7d-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4df7d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df7d-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df7d-129">CommonParameters</span></span>
<span data-ttu-id="4df7d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4df7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df7d-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4df7d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df7d-132">입력</span><span class="sxs-lookup"><span data-stu-id="4df7d-132">INPUTS</span></span>

### <span data-ttu-id="4df7d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4df7d-133">System.String</span></span>

## <span data-ttu-id="4df7d-134">출력</span><span class="sxs-lookup"><span data-stu-id="4df7d-134">OUTPUTS</span></span>

### <span data-ttu-id="4df7d-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4df7d-135">System.Boolean</span></span>

## <span data-ttu-id="4df7d-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4df7d-136">NOTES</span></span>

## <span data-ttu-id="4df7d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4df7d-137">RELATED LINKS</span></span>

[<span data-ttu-id="4df7d-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df7d-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4df7d-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df7d-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4df7d-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df7d-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="4df7d-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4df7d-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
