---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 61e2fd8a4f6c073bbb900586b0d73dec97c3b662
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876573"
---
# <span data-ttu-id="634b6-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="634b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="634b6-102">SYNOPSIS</span></span>
<span data-ttu-id="634b6-103">로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634b6-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="634b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="634b6-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="634b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="634b6-105">DESCRIPTION</span></span>
<span data-ttu-id="634b6-106">**Set-AzLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634b6-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="634b6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="634b6-107">EXAMPLES</span></span>

### <span data-ttu-id="634b6-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="634b6-108">1:</span></span>
```

```

## <span data-ttu-id="634b6-109">변수</span><span class="sxs-lookup"><span data-stu-id="634b6-109">PARAMETERS</span></span>

### <span data-ttu-id="634b6-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="634b6-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="634b6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="634b6-111">-AsJob</span></span>
<span data-ttu-id="634b6-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="634b6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="634b6-113">-Asn</span><span class="sxs-lookup"><span data-stu-id="634b6-113">-Asn</span></span>
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

### <span data-ttu-id="634b6-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="634b6-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="634b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634b6-115">-DefaultProfile</span></span>
<span data-ttu-id="634b6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="634b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="634b6-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-117">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="634b6-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="634b6-118">-PeerWeight</span></span>
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

### <span data-ttu-id="634b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634b6-119">CommonParameters</span></span>
<span data-ttu-id="634b6-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="634b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634b6-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="634b6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634b6-122">입력</span><span class="sxs-lookup"><span data-stu-id="634b6-122">INPUTS</span></span>

### <span data-ttu-id="634b6-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="634b6-124">' LocalNetworkGateway ' 매개 변수는 파이프라인에서 ' PSLocalNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="634b6-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="634b6-125">출력</span><span class="sxs-lookup"><span data-stu-id="634b6-125">OUTPUTS</span></span>

### <span data-ttu-id="634b6-126">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="634b6-127">상속자</span><span class="sxs-lookup"><span data-stu-id="634b6-127">NOTES</span></span>

## <span data-ttu-id="634b6-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="634b6-128">RELATED LINKS</span></span>

[<span data-ttu-id="634b6-129">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-129">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="634b6-130">새로운 AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-130">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="634b6-131">제거-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="634b6-131">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)


