---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342626"
---
# <span data-ttu-id="83365-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="83365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83365-102">SYNOPSIS</span></span>
<span data-ttu-id="83365-103">ExpressRoute 회로를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="83365-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="83365-104">구문</span><span class="sxs-lookup"><span data-stu-id="83365-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83365-105">설명</span><span class="sxs-lookup"><span data-stu-id="83365-105">DESCRIPTION</span></span>
<span data-ttu-id="83365-106">**Set-AzExpressRouteCircuit** cmdlet은 수정된 ExpressRoute 회로를 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="83365-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="83365-107">예제</span><span class="sxs-lookup"><span data-stu-id="83365-107">EXAMPLES</span></span>

### <span data-ttu-id="83365-108">예제 1: ExpressRoute 회로의 ServiceKey 변경</span><span class="sxs-lookup"><span data-stu-id="83365-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="83365-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83365-109">PARAMETERS</span></span>

### <span data-ttu-id="83365-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83365-110">-AsJob</span></span>
<span data-ttu-id="83365-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="83365-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83365-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83365-112">-DefaultProfile</span></span>
<span data-ttu-id="83365-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83365-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83365-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="83365-115">이 cmdlet이 수정하는 **ExpressRouteCircuit** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83365-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="83365-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83365-116">CommonParameters</span></span>
<span data-ttu-id="83365-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83365-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83365-118">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="83365-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83365-119">입력</span><span class="sxs-lookup"><span data-stu-id="83365-119">INPUTS</span></span>

### <span data-ttu-id="83365-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="83365-121">출력</span><span class="sxs-lookup"><span data-stu-id="83365-121">OUTPUTS</span></span>

### <span data-ttu-id="83365-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="83365-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83365-123">NOTES</span></span>

## <span data-ttu-id="83365-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83365-124">RELATED LINKS</span></span>

[<span data-ttu-id="83365-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="83365-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="83365-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="83365-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="83365-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
