---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbd49a948108d23c0f824adaea2e06105152a36b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531405"
---
# <span data-ttu-id="049df-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="049df-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="049df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="049df-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="049df-103">구문과</span><span class="sxs-lookup"><span data-stu-id="049df-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="049df-104">설명은</span><span class="sxs-lookup"><span data-stu-id="049df-104">DESCRIPTION</span></span>

## <span data-ttu-id="049df-105">예제의</span><span class="sxs-lookup"><span data-stu-id="049df-105">EXAMPLES</span></span>

### <span data-ttu-id="049df-106">1: Get</span><span class="sxs-lookup"><span data-stu-id="049df-106">1: Get</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzureRmLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="049df-107">변수</span><span class="sxs-lookup"><span data-stu-id="049df-107">PARAMETERS</span></span>

### <span data-ttu-id="049df-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049df-108">-DefaultProfile</span></span>
<span data-ttu-id="049df-109">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="049df-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="049df-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="049df-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="049df-111">-이름</span><span class="sxs-lookup"><span data-stu-id="049df-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049df-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049df-112">CommonParameters</span></span>
<span data-ttu-id="049df-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="049df-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049df-114">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="049df-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049df-115">입력</span><span class="sxs-lookup"><span data-stu-id="049df-115">INPUTS</span></span>

### <span data-ttu-id="049df-116">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="049df-116">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="049df-117">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="049df-117">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="049df-118">출력</span><span class="sxs-lookup"><span data-stu-id="049df-118">OUTPUTS</span></span>

### <span data-ttu-id="049df-119">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="049df-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="049df-120">상속자</span><span class="sxs-lookup"><span data-stu-id="049df-120">NOTES</span></span>

## <span data-ttu-id="049df-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="049df-121">RELATED LINKS</span></span>
