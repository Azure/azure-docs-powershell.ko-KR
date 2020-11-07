---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 6f4981469bf9468de7fd05ec79b1d3d2b28daa93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882561"
---
# <span data-ttu-id="360b5-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="360b5-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="360b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="360b5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="360b5-103">구문과</span><span class="sxs-lookup"><span data-stu-id="360b5-103">SYNTAX</span></span>

### <span data-ttu-id="360b5-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="360b5-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="360b5-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="360b5-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="360b5-106">설명은</span><span class="sxs-lookup"><span data-stu-id="360b5-106">DESCRIPTION</span></span>

## <span data-ttu-id="360b5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="360b5-107">EXAMPLES</span></span>

### <span data-ttu-id="360b5-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="360b5-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="360b5-109">변수</span><span class="sxs-lookup"><span data-stu-id="360b5-109">PARAMETERS</span></span>

### <span data-ttu-id="360b5-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="360b5-110">-BackendPort</span></span>
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

### <span data-ttu-id="360b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360b5-111">-DefaultProfile</span></span>
<span data-ttu-id="360b5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="360b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="360b5-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="360b5-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="360b5-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="360b5-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="360b5-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="360b5-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="360b5-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="360b5-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="360b5-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="360b5-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="360b5-118">-이름</span><span class="sxs-lookup"><span data-stu-id="360b5-118">-Name</span></span>
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

### <span data-ttu-id="360b5-119">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="360b5-119">-Protocol</span></span>
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

### <span data-ttu-id="360b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360b5-120">CommonParameters</span></span>
<span data-ttu-id="360b5-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="360b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360b5-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360b5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360b5-123">입력</span><span class="sxs-lookup"><span data-stu-id="360b5-123">INPUTS</span></span>

### <span data-ttu-id="360b5-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="360b5-124">PSLoadBalancer</span></span>
<span data-ttu-id="360b5-125">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="360b5-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="360b5-126">출력</span><span class="sxs-lookup"><span data-stu-id="360b5-126">OUTPUTS</span></span>

### <span data-ttu-id="360b5-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="360b5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="360b5-128">상속자</span><span class="sxs-lookup"><span data-stu-id="360b5-128">NOTES</span></span>

## <span data-ttu-id="360b5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="360b5-129">RELATED LINKS</span></span>

[<span data-ttu-id="360b5-130">추가-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="360b5-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="360b5-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="360b5-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="360b5-132">새로운 AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="360b5-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="360b5-133">제거-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="360b5-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


