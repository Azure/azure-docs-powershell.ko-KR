---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226362"
---
# <span data-ttu-id="ca360-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca360-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="ca360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca360-102">SYNOPSIS</span></span>
<span data-ttu-id="ca360-103">Express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ca360-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca360-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca360-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca360-105">DESCRIPTION</span></span>
<span data-ttu-id="ca360-106">**AzExpressRouteCircuit** Cmdlet은 express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ca360-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ca360-107">EXAMPLES</span></span>

### <span data-ttu-id="ca360-108">예제 1: Express 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="ca360-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="ca360-109">예제 2: 파이프라인을 사용 하 여 Express 회로 삭제</span><span class="sxs-lookup"><span data-stu-id="ca360-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="ca360-110">변수</span><span class="sxs-lookup"><span data-stu-id="ca360-110">PARAMETERS</span></span>

### <span data-ttu-id="ca360-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca360-111">-AsJob</span></span>
<span data-ttu-id="ca360-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ca360-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca360-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca360-113">-DefaultProfile</span></span>
<span data-ttu-id="ca360-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca360-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca360-115">-Force</span></span>
<span data-ttu-id="ca360-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca360-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ca360-117">-Name</span></span>
<span data-ttu-id="ca360-118">제거할 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="ca360-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca360-119">-PassThru</span></span>
<span data-ttu-id="ca360-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ca360-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca360-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca360-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca360-123">이 Express 경로 회로가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="ca360-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ca360-124">-Confirm</span></span>
<span data-ttu-id="ca360-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca360-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca360-126">-WhatIf</span></span>
<span data-ttu-id="ca360-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca360-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca360-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca360-129">CommonParameters</span></span>
<span data-ttu-id="ca360-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca360-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca360-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca360-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca360-132">입력</span><span class="sxs-lookup"><span data-stu-id="ca360-132">INPUTS</span></span>

### <span data-ttu-id="ca360-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ca360-133">System.String</span></span>

## <span data-ttu-id="ca360-134">출력</span><span class="sxs-lookup"><span data-stu-id="ca360-134">OUTPUTS</span></span>

### <span data-ttu-id="ca360-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ca360-135">System.Boolean</span></span>

## <span data-ttu-id="ca360-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ca360-136">NOTES</span></span>

## <span data-ttu-id="ca360-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca360-137">RELATED LINKS</span></span>

[<span data-ttu-id="ca360-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca360-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ca360-139">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca360-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="ca360-140">새로운 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca360-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="ca360-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca360-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
