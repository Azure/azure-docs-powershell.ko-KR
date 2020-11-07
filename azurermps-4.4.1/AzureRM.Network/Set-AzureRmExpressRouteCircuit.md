---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: b223cf62b536479b4c39d5852974698f2f38becf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710978"
---
# <span data-ttu-id="4ea19-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="4ea19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea19-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea19-103">Express 경로 회로를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea19-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ea19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ea19-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea19-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ea19-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea19-106">**AzureRmExpressRouteCircuit** cmdlet은 수정 된 express 경로 기반 회로를 Azure에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea19-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="4ea19-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ea19-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea19-108">예제 1: Express 경로 회로의 ServiceKey 변경</span><span class="sxs-lookup"><span data-stu-id="4ea19-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="4ea19-109">변수</span><span class="sxs-lookup"><span data-stu-id="4ea19-109">PARAMETERS</span></span>

### <span data-ttu-id="4ea19-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4ea19-111">이 cmdlet이 수정 하는 **ExpressRouteCircuit** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea19-111">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4ea19-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea19-112">-DefaultProfile</span></span>
<span data-ttu-id="4ea19-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ea19-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea19-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea19-114">CommonParameters</span></span>
<span data-ttu-id="4ea19-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea19-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea19-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea19-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea19-117">입력</span><span class="sxs-lookup"><span data-stu-id="4ea19-117">INPUTS</span></span>

### <span data-ttu-id="4ea19-118">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-118">PSExpressRouteCircuit</span></span>
<span data-ttu-id="4ea19-119">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ea19-119">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="4ea19-120">출력</span><span class="sxs-lookup"><span data-stu-id="4ea19-120">OUTPUTS</span></span>

### <span data-ttu-id="4ea19-121">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4ea19-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4ea19-122">상속자</span><span class="sxs-lookup"><span data-stu-id="4ea19-122">NOTES</span></span>

## <span data-ttu-id="4ea19-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ea19-123">RELATED LINKS</span></span>

[<span data-ttu-id="4ea19-124">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-124">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4ea19-125">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-125">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4ea19-126">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-126">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4ea19-127">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4ea19-127">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
