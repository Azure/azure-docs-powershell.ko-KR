---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881358"
---
# <span data-ttu-id="af6f8-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="af6f8-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="af6f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af6f8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af6f8-103">구문과</span><span class="sxs-lookup"><span data-stu-id="af6f8-103">SYNTAX</span></span>

### <span data-ttu-id="af6f8-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af6f8-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af6f8-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="af6f8-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af6f8-106">설명은</span><span class="sxs-lookup"><span data-stu-id="af6f8-106">DESCRIPTION</span></span>

## <span data-ttu-id="af6f8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="af6f8-107">EXAMPLES</span></span>

### <span data-ttu-id="af6f8-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="af6f8-108">1:</span></span>
```

```

## <span data-ttu-id="af6f8-109">변수</span><span class="sxs-lookup"><span data-stu-id="af6f8-109">PARAMETERS</span></span>

### <span data-ttu-id="af6f8-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="af6f8-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6f8-111">-DefaultProfile</span></span>
<span data-ttu-id="af6f8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af6f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af6f8-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="af6f8-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af6f8-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="af6f8-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="af6f8-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="af6f8-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-118">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="af6f8-118">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6f8-119">CommonParameters</span></span>
<span data-ttu-id="af6f8-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af6f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6f8-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af6f8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6f8-122">입력</span><span class="sxs-lookup"><span data-stu-id="af6f8-122">INPUTS</span></span>

## <span data-ttu-id="af6f8-123">출력</span><span class="sxs-lookup"><span data-stu-id="af6f8-123">OUTPUTS</span></span>

### <span data-ttu-id="af6f8-124">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="af6f8-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="af6f8-125">상속자</span><span class="sxs-lookup"><span data-stu-id="af6f8-125">NOTES</span></span>

## <span data-ttu-id="af6f8-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af6f8-126">RELATED LINKS</span></span>

