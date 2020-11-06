---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a33fb510e351a8f1c762801947cf4bbac9a66e28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532094"
---
# <span data-ttu-id="cab8e-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="cab8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab8e-102">SYNOPSIS</span></span>
<span data-ttu-id="cab8e-103">로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cab8e-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cab8e-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cab8e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cab8e-105">DESCRIPTION</span></span>
<span data-ttu-id="cab8e-106">**Set-AzureRmLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cab8e-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="cab8e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cab8e-107">EXAMPLES</span></span>

## <span data-ttu-id="cab8e-108">변수</span><span class="sxs-lookup"><span data-stu-id="cab8e-108">PARAMETERS</span></span>

### <span data-ttu-id="cab8e-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cab8e-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="cab8e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cab8e-110">-AsJob</span></span>
<span data-ttu-id="cab8e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cab8e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cab8e-112">-Asn</span><span class="sxs-lookup"><span data-stu-id="cab8e-112">-Asn</span></span>
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

### <span data-ttu-id="cab8e-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="cab8e-113">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="cab8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab8e-114">-DefaultProfile</span></span>
<span data-ttu-id="cab8e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cab8e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab8e-116">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-116">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="cab8e-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="cab8e-117">-PeerWeight</span></span>
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

### <span data-ttu-id="cab8e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab8e-118">CommonParameters</span></span>
<span data-ttu-id="cab8e-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cab8e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab8e-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab8e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab8e-121">입력</span><span class="sxs-lookup"><span data-stu-id="cab8e-121">INPUTS</span></span>

### <span data-ttu-id="cab8e-122">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-122">PSLocalNetworkGateway</span></span>
<span data-ttu-id="cab8e-123">' LocalNetworkGateway ' 매개 변수는 파이프라인에서 ' PSLocalNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cab8e-123">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="cab8e-124">출력</span><span class="sxs-lookup"><span data-stu-id="cab8e-124">OUTPUTS</span></span>

### <span data-ttu-id="cab8e-125">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-125">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="cab8e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="cab8e-126">NOTES</span></span>

## <span data-ttu-id="cab8e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cab8e-127">RELATED LINKS</span></span>

[<span data-ttu-id="cab8e-128">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-128">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="cab8e-129">새로운 AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-129">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="cab8e-130">제거-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cab8e-130">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


