---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 6813d1e1abf8e1f1b978c3cbcdf5a52fed92f96f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700026"
---
# <span data-ttu-id="804ef-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="804ef-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="804ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="804ef-102">SYNOPSIS</span></span>
<span data-ttu-id="804ef-103">Express 경로 회로를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="804ef-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="804ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="804ef-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="804ef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="804ef-105">DESCRIPTION</span></span>
<span data-ttu-id="804ef-106">**AzExpressRouteCircuit** cmdlet은 수정 된 express 경로 기반 회로를 Azure에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="804ef-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="804ef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="804ef-107">EXAMPLES</span></span>

### <span data-ttu-id="804ef-108">예제 1: Express 경로 회로의 ServiceKey 변경</span><span class="sxs-lookup"><span data-stu-id="804ef-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="804ef-109">변수</span><span class="sxs-lookup"><span data-stu-id="804ef-109">PARAMETERS</span></span>

### <span data-ttu-id="804ef-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="804ef-110">-AsJob</span></span>
<span data-ttu-id="804ef-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="804ef-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="804ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804ef-112">-DefaultProfile</span></span>
<span data-ttu-id="804ef-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="804ef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804ef-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="804ef-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="804ef-115">이 cmdlet이 수정 하는 **ExpressRouteCircuit** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="804ef-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="804ef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804ef-116">CommonParameters</span></span>
<span data-ttu-id="804ef-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="804ef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804ef-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804ef-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804ef-119">입력</span><span class="sxs-lookup"><span data-stu-id="804ef-119">INPUTS</span></span>

### <span data-ttu-id="804ef-120">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="804ef-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="804ef-121">출력</span><span class="sxs-lookup"><span data-stu-id="804ef-121">OUTPUTS</span></span>

### <span data-ttu-id="804ef-122">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="804ef-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="804ef-123">상속자</span><span class="sxs-lookup"><span data-stu-id="804ef-123">NOTES</span></span>

## <span data-ttu-id="804ef-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="804ef-124">RELATED LINKS</span></span>

[<span data-ttu-id="804ef-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="804ef-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="804ef-126">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="804ef-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="804ef-127">새로운 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="804ef-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="804ef-128">제거-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="804ef-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)