---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: f72d398eaea1d127ba600130fae3bbc690052332
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875601"
---
# <span data-ttu-id="662df-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="662df-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="662df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="662df-102">SYNOPSIS</span></span>
<span data-ttu-id="662df-103">Azure에서 Azure Express 경로 회로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="662df-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="662df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="662df-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="662df-105">설명은</span><span class="sxs-lookup"><span data-stu-id="662df-105">DESCRIPTION</span></span>
<span data-ttu-id="662df-106">**AzExpressRouteCircuit** cmdlet은 구독에서 express 경로 회로 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="662df-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="662df-107">반환 되는 회로 개체는 Express 경로 회로에서 작동 하는 다른 cmdlet에 대 한 입력으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="662df-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="662df-108">예제의</span><span class="sxs-lookup"><span data-stu-id="662df-108">EXAMPLES</span></span>

### <span data-ttu-id="662df-109">예제 1: 삭제 될 Express 경로 회로 가져오기</span><span class="sxs-lookup"><span data-stu-id="662df-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="662df-110">변수</span><span class="sxs-lookup"><span data-stu-id="662df-110">PARAMETERS</span></span>

### <span data-ttu-id="662df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662df-111">-DefaultProfile</span></span>
<span data-ttu-id="662df-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="662df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="662df-113">-이름</span><span class="sxs-lookup"><span data-stu-id="662df-113">-Name</span></span>
<span data-ttu-id="662df-114">Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="662df-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662df-115">-ResourceGroupName</span></span>
<span data-ttu-id="662df-116">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="662df-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="662df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662df-117">CommonParameters</span></span>
<span data-ttu-id="662df-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="662df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662df-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="662df-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662df-120">입력</span><span class="sxs-lookup"><span data-stu-id="662df-120">INPUTS</span></span>

## <span data-ttu-id="662df-121">출력</span><span class="sxs-lookup"><span data-stu-id="662df-121">OUTPUTS</span></span>

### <span data-ttu-id="662df-122">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="662df-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="662df-123">상속자</span><span class="sxs-lookup"><span data-stu-id="662df-123">NOTES</span></span>

## <span data-ttu-id="662df-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="662df-124">RELATED LINKS</span></span>

[<span data-ttu-id="662df-125">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="662df-125">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="662df-126">새로운 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="662df-126">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="662df-127">제거-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="662df-127">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="662df-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="662df-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
