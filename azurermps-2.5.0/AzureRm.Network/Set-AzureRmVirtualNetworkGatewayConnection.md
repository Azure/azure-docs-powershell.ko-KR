---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882162"
---
# <span data-ttu-id="a565e-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a565e-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a565e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a565e-102">SYNOPSIS</span></span>
<span data-ttu-id="a565e-103">가상 네트워크 게이트웨이 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a565e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a565e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a565e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a565e-105">DESCRIPTION</span></span>
<span data-ttu-id="a565e-106">**AzureRmVirtualNetworkGatewayConnection** cmdlet은 가상 네트워크 게이트웨이 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="a565e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a565e-107">EXAMPLES</span></span>

### <span data-ttu-id="a565e-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="a565e-108">1:</span></span>
```

```

## <span data-ttu-id="a565e-109">변수</span><span class="sxs-lookup"><span data-stu-id="a565e-109">PARAMETERS</span></span>

### <span data-ttu-id="a565e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a565e-110">-AsJob</span></span>
<span data-ttu-id="a565e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a565e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a565e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a565e-112">-DefaultProfile</span></span>
<span data-ttu-id="a565e-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a565e-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a565e-114">-EnableBgp</span></span>
<span data-ttu-id="a565e-115">S2S VPN 터널을 통해 BGP 세션을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="a565e-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a565e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a565e-116">-Force</span></span>
<span data-ttu-id="a565e-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a565e-118">-계층 정책</span><span class="sxs-lookup"><span data-stu-id="a565e-118">-IpsecPolicies</span></span>
<span data-ttu-id="a565e-119">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a565e-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="a565e-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="a565e-121">S2S 연결에 대해 정책 기반 트래픽 선택기를 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="a565e-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a565e-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a565e-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="a565e-123">이 cmdlet이 가상 네트워크 게이트웨이 연결을 수정 하는 데 사용 하는 PSVirtualNetworkGatewayConnection 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a565e-124">-확인</span><span class="sxs-lookup"><span data-stu-id="a565e-124">-Confirm</span></span>
<span data-ttu-id="a565e-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a565e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a565e-126">-WhatIf</span></span>
<span data-ttu-id="a565e-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a565e-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a565e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a565e-129">CommonParameters</span></span>
<span data-ttu-id="a565e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a565e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a565e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a565e-132">입력</span><span class="sxs-lookup"><span data-stu-id="a565e-132">INPUTS</span></span>

### <span data-ttu-id="a565e-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a565e-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="a565e-134">' VirtualNetworkGatewayConnection ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGatewayConnection ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a565e-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="a565e-135">출력</span><span class="sxs-lookup"><span data-stu-id="a565e-135">OUTPUTS</span></span>

### <span data-ttu-id="a565e-136">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a565e-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="a565e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="a565e-137">NOTES</span></span>

## <span data-ttu-id="a565e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a565e-138">RELATED LINKS</span></span>

[<span data-ttu-id="a565e-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a565e-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a565e-140">새로운 AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a565e-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="a565e-141">제거-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a565e-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


