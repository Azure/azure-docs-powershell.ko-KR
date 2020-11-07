---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 20837f96bc17d2cfd71abc359ff4114b44e6c062
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881026"
---
# <span data-ttu-id="28d3b-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="28d3b-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="28d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d3b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28d3b-103">구문과</span><span class="sxs-lookup"><span data-stu-id="28d3b-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28d3b-104">설명은</span><span class="sxs-lookup"><span data-stu-id="28d3b-104">DESCRIPTION</span></span>

## <span data-ttu-id="28d3b-105">예제의</span><span class="sxs-lookup"><span data-stu-id="28d3b-105">EXAMPLES</span></span>

### <span data-ttu-id="28d3b-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="28d3b-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="28d3b-107">변수</span><span class="sxs-lookup"><span data-stu-id="28d3b-107">PARAMETERS</span></span>

### <span data-ttu-id="28d3b-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d3b-108">-DefaultProfile</span></span>
<span data-ttu-id="28d3b-109">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28d3b-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28d3b-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="28d3b-110">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28d3b-111">-이름</span><span class="sxs-lookup"><span data-stu-id="28d3b-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d3b-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d3b-112">CommonParameters</span></span>
<span data-ttu-id="28d3b-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d3b-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d3b-114">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d3b-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d3b-115">입력</span><span class="sxs-lookup"><span data-stu-id="28d3b-115">INPUTS</span></span>

### <span data-ttu-id="28d3b-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="28d3b-116">PSLoadBalancer</span></span>
<span data-ttu-id="28d3b-117">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d3b-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="28d3b-118">출력</span><span class="sxs-lookup"><span data-stu-id="28d3b-118">OUTPUTS</span></span>

### <span data-ttu-id="28d3b-119">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="28d3b-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="28d3b-120">상속자</span><span class="sxs-lookup"><span data-stu-id="28d3b-120">NOTES</span></span>

## <span data-ttu-id="28d3b-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28d3b-121">RELATED LINKS</span></span>

