---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046086"
---
# <span data-ttu-id="5e7c6-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e7c6-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="5e7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7c6-103">가상 네트워크 게이트웨이의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c6-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="5e7c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e7c6-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e7c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e7c6-105">DESCRIPTION</span></span>
<span data-ttu-id="5e7c6-106">Resize-AzureVirtualNetworkGateway cmdlet은 가상 네트워크 게이트웨이의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c6-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="5e7c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e7c6-107">EXAMPLES</span></span>

## <span data-ttu-id="5e7c6-108">변수</span><span class="sxs-lookup"><span data-stu-id="5e7c6-108">PARAMETERS</span></span>

### <span data-ttu-id="5e7c6-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5e7c6-109">-GatewayId</span></span>
<span data-ttu-id="5e7c6-110">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c6-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="5e7c6-111">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="5e7c6-111">-GatewaySKU</span></span>
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

### <span data-ttu-id="5e7c6-112">-프로필</span><span class="sxs-lookup"><span data-stu-id="5e7c6-112">-Profile</span></span>
<span data-ttu-id="5e7c6-113">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c6-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5e7c6-114">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c6-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e7c6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7c6-115">CommonParameters</span></span>
<span data-ttu-id="5e7c6-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7c6-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7c6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7c6-118">입력</span><span class="sxs-lookup"><span data-stu-id="5e7c6-118">INPUTS</span></span>

## <span data-ttu-id="5e7c6-119">출력</span><span class="sxs-lookup"><span data-stu-id="5e7c6-119">OUTPUTS</span></span>

## <span data-ttu-id="5e7c6-120">상속자</span><span class="sxs-lookup"><span data-stu-id="5e7c6-120">NOTES</span></span>

## <span data-ttu-id="5e7c6-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e7c6-121">RELATED LINKS</span></span>

[<span data-ttu-id="5e7c6-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e7c6-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="5e7c6-123">새로운 AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e7c6-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="5e7c6-124">제거-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e7c6-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="5e7c6-125">다시 설정-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5e7c6-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


