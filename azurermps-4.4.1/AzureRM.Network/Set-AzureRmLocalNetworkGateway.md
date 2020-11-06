---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 8d2b3c6c15a48407b138fa26778bdf906b5a7a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529272"
---
# <span data-ttu-id="b4641-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="b4641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4641-102">SYNOPSIS</span></span>
<span data-ttu-id="b4641-103">로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4641-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4641-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4641-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4641-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4641-105">DESCRIPTION</span></span>
<span data-ttu-id="b4641-106">**Set-AzureRmLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4641-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="b4641-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b4641-107">EXAMPLES</span></span>

## <span data-ttu-id="b4641-108">변수</span><span class="sxs-lookup"><span data-stu-id="b4641-108">PARAMETERS</span></span>

### <span data-ttu-id="b4641-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4641-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="b4641-110">-Asn</span><span class="sxs-lookup"><span data-stu-id="b4641-110">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4641-111">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b4641-111">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4641-112">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-112">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4641-113">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="b4641-113">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4641-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4641-114">-DefaultProfile</span></span>
<span data-ttu-id="b4641-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4641-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4641-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4641-116">CommonParameters</span></span>
<span data-ttu-id="b4641-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4641-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4641-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4641-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4641-119">입력</span><span class="sxs-lookup"><span data-stu-id="b4641-119">INPUTS</span></span>

### <span data-ttu-id="b4641-120">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-120">PSLocalNetworkGateway</span></span>
<span data-ttu-id="b4641-121">' LocalNetworkGateway ' 매개 변수는 파이프라인에서 ' PSLocalNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4641-121">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="b4641-122">출력</span><span class="sxs-lookup"><span data-stu-id="b4641-122">OUTPUTS</span></span>

### <span data-ttu-id="b4641-123">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b4641-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b4641-124">NOTES</span></span>

## <span data-ttu-id="b4641-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4641-125">RELATED LINKS</span></span>

[<span data-ttu-id="b4641-126">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-126">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b4641-127">새로운 AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-127">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="b4641-128">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4641-128">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


