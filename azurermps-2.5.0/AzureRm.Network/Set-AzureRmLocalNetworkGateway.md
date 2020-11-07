---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882549"
---
# <span data-ttu-id="3cd24-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="3cd24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd24-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd24-103">로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd24-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cd24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3cd24-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cd24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3cd24-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd24-106">**Set-AzureRmLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd24-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="3cd24-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3cd24-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd24-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="3cd24-108">1:</span></span>
```

```

## <span data-ttu-id="3cd24-109">변수</span><span class="sxs-lookup"><span data-stu-id="3cd24-109">PARAMETERS</span></span>

### <span data-ttu-id="3cd24-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3cd24-110">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd24-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cd24-111">-AsJob</span></span>
<span data-ttu-id="3cd24-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3cd24-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cd24-113">-Asn</span><span class="sxs-lookup"><span data-stu-id="3cd24-113">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd24-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3cd24-114">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd24-115">-DefaultProfile</span></span>
<span data-ttu-id="3cd24-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd24-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cd24-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd24-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3cd24-118">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd24-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd24-119">CommonParameters</span></span>
<span data-ttu-id="3cd24-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd24-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd24-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd24-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd24-122">입력</span><span class="sxs-lookup"><span data-stu-id="3cd24-122">INPUTS</span></span>

### <span data-ttu-id="3cd24-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="3cd24-124">' LocalNetworkGateway ' 매개 변수는 파이프라인에서 ' PSLocalNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd24-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3cd24-125">출력</span><span class="sxs-lookup"><span data-stu-id="3cd24-125">OUTPUTS</span></span>

### <span data-ttu-id="3cd24-126">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3cd24-127">상속자</span><span class="sxs-lookup"><span data-stu-id="3cd24-127">NOTES</span></span>

## <span data-ttu-id="3cd24-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cd24-128">RELATED LINKS</span></span>

[<span data-ttu-id="3cd24-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3cd24-130">새로운 AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3cd24-131">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3cd24-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


