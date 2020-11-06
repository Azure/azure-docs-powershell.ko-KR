---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535719"
---
# <span data-ttu-id="2d9fa-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="2d9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9fa-103">가상 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d9fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d9fa-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d9fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9fa-106">가상 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="2d9fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2d9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="2d9fa-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="2d9fa-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="2d9fa-109">변수</span><span class="sxs-lookup"><span data-stu-id="2d9fa-109">PARAMETERS</span></span>

### <span data-ttu-id="2d9fa-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d9fa-110">-AsJob</span></span>
<span data-ttu-id="2d9fa-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2d9fa-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9fa-112">-DefaultProfile</span></span>
<span data-ttu-id="2d9fa-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d9fa-114">-게이트웨이 Vip</span><span class="sxs-lookup"><span data-stu-id="2d9fa-114">-GatewayVip</span></span>
<span data-ttu-id="2d9fa-115">특정 게이트웨이 인스턴스를 다시 설정 하기 위한 게이트웨이 vip (예: Active-Active 기능을 사용할 수 있는 게이트웨이를 사용 하는 경우) 값이 전달 되지 않으면 기본적으로 게이트웨이 기본 인스턴스가 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9fa-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9fa-117">CommonParameters</span></span>
<span data-ttu-id="2d9fa-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9fa-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9fa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9fa-120">입력</span><span class="sxs-lookup"><span data-stu-id="2d9fa-120">INPUTS</span></span>

### <span data-ttu-id="2d9fa-121">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="2d9fa-122">매개 변수: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d9fa-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="2d9fa-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d9fa-123">System.String</span></span>
<span data-ttu-id="2d9fa-124">매개 변수: 게이트웨이 Vip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d9fa-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="2d9fa-125">출력</span><span class="sxs-lookup"><span data-stu-id="2d9fa-125">OUTPUTS</span></span>

### <span data-ttu-id="2d9fa-126">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2d9fa-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2d9fa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="2d9fa-127">NOTES</span></span>

## <span data-ttu-id="2d9fa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d9fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="2d9fa-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2d9fa-130">새로운 AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2d9fa-131">제거-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2d9fa-132">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2d9fa-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d9fa-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


