---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529306"
---
# <span data-ttu-id="817d1-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="817d1-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="817d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="817d1-102">SYNOPSIS</span></span>
<span data-ttu-id="817d1-103">Azure에서 Azure Express 경로 회로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="817d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="817d1-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="817d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="817d1-105">DESCRIPTION</span></span>
<span data-ttu-id="817d1-106">**AzureRmExpressRouteCircuit** cmdlet은 구독에서 express 경로 회로 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="817d1-107">반환 되는 회로 개체는 Express 경로 회로에서 작동 하는 다른 cmdlet에 대 한 입력으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="817d1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="817d1-108">EXAMPLES</span></span>

### <span data-ttu-id="817d1-109">예제 1: 삭제 될 Express 경로 회로 가져오기</span><span class="sxs-lookup"><span data-stu-id="817d1-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="817d1-110">변수</span><span class="sxs-lookup"><span data-stu-id="817d1-110">PARAMETERS</span></span>

### <span data-ttu-id="817d1-111">-이름</span><span class="sxs-lookup"><span data-stu-id="817d1-111">-Name</span></span>
<span data-ttu-id="817d1-112">Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817d1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817d1-113">-ResourceGroupName</span></span>
<span data-ttu-id="817d1-114">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817d1-115">-DefaultProfile</span></span>
<span data-ttu-id="817d1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="817d1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817d1-117">CommonParameters</span></span>
<span data-ttu-id="817d1-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="817d1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817d1-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817d1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817d1-120">입력</span><span class="sxs-lookup"><span data-stu-id="817d1-120">INPUTS</span></span>

## <span data-ttu-id="817d1-121">출력</span><span class="sxs-lookup"><span data-stu-id="817d1-121">OUTPUTS</span></span>

### <span data-ttu-id="817d1-122">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="817d1-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="817d1-123">상속자</span><span class="sxs-lookup"><span data-stu-id="817d1-123">NOTES</span></span>

## <span data-ttu-id="817d1-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="817d1-124">RELATED LINKS</span></span>

[<span data-ttu-id="817d1-125">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="817d1-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="817d1-126">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="817d1-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="817d1-127">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="817d1-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="817d1-128">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="817d1-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
