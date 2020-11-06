---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 8ef7121e057759a6fbdb341d9d6bc137692a36cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537523"
---
# <span data-ttu-id="af1fa-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af1fa-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="af1fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="af1fa-103">Express 경로 회로를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1fa-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af1fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af1fa-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af1fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="af1fa-105">DESCRIPTION</span></span>
<span data-ttu-id="af1fa-106">**AzureRmExpressRouteCircuit** cmdlet은 수정 된 express 경로 기반 회로를 Azure에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1fa-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="af1fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="af1fa-107">EXAMPLES</span></span>

### <span data-ttu-id="af1fa-108">예제 1: Express 경로 회로의 ServiceKey 변경</span><span class="sxs-lookup"><span data-stu-id="af1fa-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="af1fa-109">변수</span><span class="sxs-lookup"><span data-stu-id="af1fa-109">PARAMETERS</span></span>

### <span data-ttu-id="af1fa-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af1fa-110">-AsJob</span></span>
<span data-ttu-id="af1fa-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="af1fa-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af1fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1fa-112">-DefaultProfile</span></span>
<span data-ttu-id="af1fa-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af1fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af1fa-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af1fa-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="af1fa-115">이 cmdlet이 수정 하는 **ExpressRouteCircuit** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1fa-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="af1fa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1fa-116">CommonParameters</span></span>
<span data-ttu-id="af1fa-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af1fa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1fa-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af1fa-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1fa-119">입력</span><span class="sxs-lookup"><span data-stu-id="af1fa-119">INPUTS</span></span>

### <span data-ttu-id="af1fa-120">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="af1fa-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="af1fa-121">매개 변수: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af1fa-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="af1fa-122">출력</span><span class="sxs-lookup"><span data-stu-id="af1fa-122">OUTPUTS</span></span>

### <span data-ttu-id="af1fa-123">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="af1fa-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="af1fa-124">상속자</span><span class="sxs-lookup"><span data-stu-id="af1fa-124">NOTES</span></span>

## <span data-ttu-id="af1fa-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af1fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="af1fa-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af1fa-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="af1fa-127">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af1fa-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="af1fa-128">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af1fa-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="af1fa-129">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af1fa-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
