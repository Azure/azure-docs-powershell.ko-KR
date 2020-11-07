---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882838"
---
# <span data-ttu-id="1ed28-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="1ed28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed28-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed28-103">구문과</span><span class="sxs-lookup"><span data-stu-id="1ed28-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ed28-104">설명은</span><span class="sxs-lookup"><span data-stu-id="1ed28-104">DESCRIPTION</span></span>

## <span data-ttu-id="1ed28-105">예제의</span><span class="sxs-lookup"><span data-stu-id="1ed28-105">EXAMPLES</span></span>

### <span data-ttu-id="1ed28-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="1ed28-106">1:</span></span>
```

```

## <span data-ttu-id="1ed28-107">변수</span><span class="sxs-lookup"><span data-stu-id="1ed28-107">PARAMETERS</span></span>

### <span data-ttu-id="1ed28-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ed28-108">-AsJob</span></span>
<span data-ttu-id="1ed28-109">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1ed28-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ed28-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed28-110">-DefaultProfile</span></span>
<span data-ttu-id="1ed28-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ed28-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed28-112">-게이트웨이 Vip</span><span class="sxs-lookup"><span data-stu-id="1ed28-112">-GatewayVip</span></span>
<span data-ttu-id="1ed28-113">특정 게이트웨이 인스턴스를 다시 설정 하기 위한 게이트웨이 vip (예: Active-Active 기능을 사용할 수 있는 게이트웨이를 사용 하는 경우) 값이 전달 되지 않으면 기본적으로 게이트웨이 기본 인스턴스가 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ed28-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed28-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed28-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed28-115">CommonParameters</span></span>
<span data-ttu-id="1ed28-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed28-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed28-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed28-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed28-118">입력</span><span class="sxs-lookup"><span data-stu-id="1ed28-118">INPUTS</span></span>

### <span data-ttu-id="1ed28-119">이름</span><span class="sxs-lookup"><span data-stu-id="1ed28-119">String</span></span>
<span data-ttu-id="1ed28-120">'. H i m ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed28-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="1ed28-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1ed28-122">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed28-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="1ed28-123">출력</span><span class="sxs-lookup"><span data-stu-id="1ed28-123">OUTPUTS</span></span>

### <span data-ttu-id="1ed28-124">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1ed28-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1ed28-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1ed28-125">NOTES</span></span>

## <span data-ttu-id="1ed28-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ed28-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ed28-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ed28-128">새로운 AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ed28-129">제거-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ed28-130">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1ed28-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ed28-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


