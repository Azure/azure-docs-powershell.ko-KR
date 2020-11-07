---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710985"
---
# <span data-ttu-id="cfbed-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="cfbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfbed-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfbed-103">구문과</span><span class="sxs-lookup"><span data-stu-id="cfbed-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfbed-104">설명은</span><span class="sxs-lookup"><span data-stu-id="cfbed-104">DESCRIPTION</span></span>

## <span data-ttu-id="cfbed-105">예제의</span><span class="sxs-lookup"><span data-stu-id="cfbed-105">EXAMPLES</span></span>

## <span data-ttu-id="cfbed-106">변수</span><span class="sxs-lookup"><span data-stu-id="cfbed-106">PARAMETERS</span></span>

### <span data-ttu-id="cfbed-107">-게이트웨이 Vip</span><span class="sxs-lookup"><span data-stu-id="cfbed-107">-GatewayVip</span></span>
<span data-ttu-id="cfbed-108">특정 게이트웨이 인스턴스를 다시 설정 하기 위한 게이트웨이 vip (예: Active-Active 기능을 사용할 수 있는 게이트웨이를 사용 하는 경우) 값이 전달 되지 않으면 기본적으로 게이트웨이 기본 인스턴스가 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfbed-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="cfbed-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-109">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="cfbed-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbed-110">-DefaultProfile</span></span>
<span data-ttu-id="cfbed-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfbed-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfbed-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbed-112">CommonParameters</span></span>
<span data-ttu-id="cfbed-113">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbed-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbed-114">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfbed-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbed-115">입력</span><span class="sxs-lookup"><span data-stu-id="cfbed-115">INPUTS</span></span>

### <span data-ttu-id="cfbed-116">이름</span><span class="sxs-lookup"><span data-stu-id="cfbed-116">String</span></span>
<span data-ttu-id="cfbed-117">'. H i m ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="cfbed-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="cfbed-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="cfbed-119">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfbed-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="cfbed-120">출력</span><span class="sxs-lookup"><span data-stu-id="cfbed-120">OUTPUTS</span></span>

### <span data-ttu-id="cfbed-121">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cfbed-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cfbed-122">상속자</span><span class="sxs-lookup"><span data-stu-id="cfbed-122">NOTES</span></span>

## <span data-ttu-id="cfbed-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfbed-123">RELATED LINKS</span></span>

[<span data-ttu-id="cfbed-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cfbed-125">새로운 AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cfbed-126">제거-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cfbed-127">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cfbed-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfbed-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


