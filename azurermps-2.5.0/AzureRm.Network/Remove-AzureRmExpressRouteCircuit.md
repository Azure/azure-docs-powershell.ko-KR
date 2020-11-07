---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880361"
---
# <span data-ttu-id="08eb2-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08eb2-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="08eb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="08eb2-103">Express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08eb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08eb2-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08eb2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08eb2-105">DESCRIPTION</span></span>
<span data-ttu-id="08eb2-106">**AzureRmExpressRouteCircuit** Cmdlet은 express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="08eb2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="08eb2-107">EXAMPLES</span></span>

### <span data-ttu-id="08eb2-108">예제 1: Express 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="08eb2-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="08eb2-109">예제 2: 파이프라인을 사용 하 여 Express 회로 삭제</span><span class="sxs-lookup"><span data-stu-id="08eb2-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="08eb2-110">변수</span><span class="sxs-lookup"><span data-stu-id="08eb2-110">PARAMETERS</span></span>

### <span data-ttu-id="08eb2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08eb2-111">-AsJob</span></span>
<span data-ttu-id="08eb2-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="08eb2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08eb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08eb2-113">-DefaultProfile</span></span>
<span data-ttu-id="08eb2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08eb2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="08eb2-115">-Force</span></span>
<span data-ttu-id="08eb2-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08eb2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="08eb2-117">-Name</span></span>
<span data-ttu-id="08eb2-118">제거할 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="08eb2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08eb2-119">-PassThru</span></span>
<span data-ttu-id="08eb2-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="08eb2-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08eb2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08eb2-122">-ResourceGroupName</span></span>
<span data-ttu-id="08eb2-123">이 Express 경로 회로가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="08eb2-124">-확인</span><span class="sxs-lookup"><span data-stu-id="08eb2-124">-Confirm</span></span>
<span data-ttu-id="08eb2-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08eb2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08eb2-126">-WhatIf</span></span>
<span data-ttu-id="08eb2-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08eb2-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08eb2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08eb2-129">CommonParameters</span></span>
<span data-ttu-id="08eb2-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08eb2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08eb2-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08eb2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08eb2-132">입력</span><span class="sxs-lookup"><span data-stu-id="08eb2-132">INPUTS</span></span>

## <span data-ttu-id="08eb2-133">출력</span><span class="sxs-lookup"><span data-stu-id="08eb2-133">OUTPUTS</span></span>

## <span data-ttu-id="08eb2-134">상속자</span><span class="sxs-lookup"><span data-stu-id="08eb2-134">NOTES</span></span>

## <span data-ttu-id="08eb2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08eb2-135">RELATED LINKS</span></span>

[<span data-ttu-id="08eb2-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08eb2-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="08eb2-137">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08eb2-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="08eb2-138">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08eb2-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="08eb2-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="08eb2-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
