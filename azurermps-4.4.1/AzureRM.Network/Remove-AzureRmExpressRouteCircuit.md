---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530768"
---
# <span data-ttu-id="2706e-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2706e-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="2706e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2706e-102">SYNOPSIS</span></span>
<span data-ttu-id="2706e-103">Express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2706e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2706e-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2706e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2706e-105">DESCRIPTION</span></span>
<span data-ttu-id="2706e-106">**AzureRmExpressRouteCircuit** Cmdlet은 express 경로 회로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2706e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2706e-107">EXAMPLES</span></span>

### <span data-ttu-id="2706e-108">예제 1: Express 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="2706e-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="2706e-109">예제 2: 파이프라인을 사용 하 여 Express 회로 삭제</span><span class="sxs-lookup"><span data-stu-id="2706e-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="2706e-110">변수</span><span class="sxs-lookup"><span data-stu-id="2706e-110">PARAMETERS</span></span>

### <span data-ttu-id="2706e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2706e-111">-Force</span></span>
<span data-ttu-id="2706e-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2706e-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2706e-113">-Name</span></span>
<span data-ttu-id="2706e-114">제거할 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="2706e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2706e-115">-PassThru</span></span>
<span data-ttu-id="2706e-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2706e-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2706e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2706e-118">-ResourceGroupName</span></span>
<span data-ttu-id="2706e-119">이 Express 경로 회로가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="2706e-120">-확인</span><span class="sxs-lookup"><span data-stu-id="2706e-120">-Confirm</span></span>
<span data-ttu-id="2706e-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2706e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2706e-122">-WhatIf</span></span>
<span data-ttu-id="2706e-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2706e-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2706e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2706e-125">-DefaultProfile</span></span>
<span data-ttu-id="2706e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2706e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2706e-127">CommonParameters</span></span>
<span data-ttu-id="2706e-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2706e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2706e-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2706e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2706e-130">입력</span><span class="sxs-lookup"><span data-stu-id="2706e-130">INPUTS</span></span>

## <span data-ttu-id="2706e-131">출력</span><span class="sxs-lookup"><span data-stu-id="2706e-131">OUTPUTS</span></span>

## <span data-ttu-id="2706e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2706e-132">NOTES</span></span>

## <span data-ttu-id="2706e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2706e-133">RELATED LINKS</span></span>

[<span data-ttu-id="2706e-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2706e-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2706e-135">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2706e-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2706e-136">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2706e-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="2706e-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2706e-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
