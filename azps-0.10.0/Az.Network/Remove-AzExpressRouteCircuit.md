---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 4dbddf7e78297acc3f12f69dd2a44f9698f7b891
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875346"
---
# <span data-ttu-id="a70ee-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a70ee-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a70ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a70ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a70ee-103">Express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a70ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a70ee-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a70ee-105">DESCRIPTION</span></span>
<span data-ttu-id="a70ee-106">**AzExpressRouteCircuit** Cmdlet은 express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a70ee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a70ee-107">EXAMPLES</span></span>

### <span data-ttu-id="a70ee-108">예제 1: Express 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="a70ee-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="a70ee-109">예제 2: 파이프라인을 사용 하 여 Express 회로 삭제</span><span class="sxs-lookup"><span data-stu-id="a70ee-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="a70ee-110">변수</span><span class="sxs-lookup"><span data-stu-id="a70ee-110">PARAMETERS</span></span>

### <span data-ttu-id="a70ee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a70ee-111">-AsJob</span></span>
<span data-ttu-id="a70ee-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a70ee-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a70ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70ee-113">-DefaultProfile</span></span>
<span data-ttu-id="a70ee-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a70ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a70ee-115">-Force</span></span>
<span data-ttu-id="a70ee-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a70ee-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a70ee-117">-Name</span></span>
<span data-ttu-id="a70ee-118">제거할 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70ee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a70ee-119">-PassThru</span></span>
<span data-ttu-id="a70ee-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a70ee-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a70ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="a70ee-123">이 Express 경로 회로가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70ee-124">-확인</span><span class="sxs-lookup"><span data-stu-id="a70ee-124">-Confirm</span></span>
<span data-ttu-id="a70ee-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70ee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70ee-126">-WhatIf</span></span>
<span data-ttu-id="a70ee-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70ee-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70ee-129">CommonParameters</span></span>
<span data-ttu-id="a70ee-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70ee-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a70ee-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70ee-132">입력</span><span class="sxs-lookup"><span data-stu-id="a70ee-132">INPUTS</span></span>

## <span data-ttu-id="a70ee-133">출력</span><span class="sxs-lookup"><span data-stu-id="a70ee-133">OUTPUTS</span></span>

## <span data-ttu-id="a70ee-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a70ee-134">NOTES</span></span>

## <span data-ttu-id="a70ee-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a70ee-135">RELATED LINKS</span></span>

[<span data-ttu-id="a70ee-136">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a70ee-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a70ee-137">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a70ee-137">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a70ee-138">새로운 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a70ee-138">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a70ee-139">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a70ee-139">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
