---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045472"
---
# <span data-ttu-id="054cb-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="054cb-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="054cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="054cb-102">SYNOPSIS</span></span>
<span data-ttu-id="054cb-103">로컬 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="054cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="054cb-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="054cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="054cb-105">DESCRIPTION</span></span>
<span data-ttu-id="054cb-106">**Reset-AzureLocalNetworkGateway** cmdlet은 로컬 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="054cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="054cb-107">EXAMPLES</span></span>

## <span data-ttu-id="054cb-108">변수</span><span class="sxs-lookup"><span data-stu-id="054cb-108">PARAMETERS</span></span>

### <span data-ttu-id="054cb-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="054cb-109">-AddressSpace</span></span>
<span data-ttu-id="054cb-110">주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-111">-Asn</span><span class="sxs-lookup"><span data-stu-id="054cb-111">-Asn</span></span>
<span data-ttu-id="054cb-112">ASN (익명 시스템 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="054cb-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="054cb-114">BGP (Border Gateway Protocol) 피어 링 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="054cb-115">-GatewayId</span></span>
<span data-ttu-id="054cb-116">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="054cb-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="054cb-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054cb-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="054cb-118">-Profile</span></span>
<span data-ttu-id="054cb-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="054cb-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="054cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054cb-121">CommonParameters</span></span>
<span data-ttu-id="054cb-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="054cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054cb-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="054cb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054cb-124">입력</span><span class="sxs-lookup"><span data-stu-id="054cb-124">INPUTS</span></span>

## <span data-ttu-id="054cb-125">출력</span><span class="sxs-lookup"><span data-stu-id="054cb-125">OUTPUTS</span></span>

## <span data-ttu-id="054cb-126">상속자</span><span class="sxs-lookup"><span data-stu-id="054cb-126">NOTES</span></span>

## <span data-ttu-id="054cb-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="054cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="054cb-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="054cb-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="054cb-129">새 AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="054cb-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="054cb-130">-AzureLocalNetworkGateway 제거</span><span class="sxs-lookup"><span data-stu-id="054cb-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


