---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 71a6ec46cea6cc9d2ba6e6537797657b2124fe01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528924"
---
# <span data-ttu-id="34d98-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="34d98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d98-102">SYNOPSIS</span></span>
<span data-ttu-id="34d98-103">Express 경로 회로를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d98-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34d98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34d98-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34d98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34d98-105">DESCRIPTION</span></span>
<span data-ttu-id="34d98-106">**AzureRmExpressRouteCircuit** cmdlet은 수정 된 express 경로 기반 회로를 Azure에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d98-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="34d98-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34d98-107">EXAMPLES</span></span>

### <span data-ttu-id="34d98-108">예제 1: Express 경로 회로의 ServiceKey 변경</span><span class="sxs-lookup"><span data-stu-id="34d98-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="34d98-109">변수</span><span class="sxs-lookup"><span data-stu-id="34d98-109">PARAMETERS</span></span>

### <span data-ttu-id="34d98-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34d98-110">-AsJob</span></span>
<span data-ttu-id="34d98-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="34d98-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34d98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d98-112">-DefaultProfile</span></span>
<span data-ttu-id="34d98-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34d98-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34d98-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="34d98-115">이 cmdlet이 수정 하는 **ExpressRouteCircuit** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d98-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34d98-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d98-116">CommonParameters</span></span>
<span data-ttu-id="34d98-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d98-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d98-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d98-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d98-119">입력</span><span class="sxs-lookup"><span data-stu-id="34d98-119">INPUTS</span></span>

### <span data-ttu-id="34d98-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="34d98-121">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34d98-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="34d98-122">출력</span><span class="sxs-lookup"><span data-stu-id="34d98-122">OUTPUTS</span></span>

### <span data-ttu-id="34d98-123">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="34d98-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="34d98-124">상속자</span><span class="sxs-lookup"><span data-stu-id="34d98-124">NOTES</span></span>

## <span data-ttu-id="34d98-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34d98-125">RELATED LINKS</span></span>

[<span data-ttu-id="34d98-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="34d98-127">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="34d98-128">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="34d98-129">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34d98-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)