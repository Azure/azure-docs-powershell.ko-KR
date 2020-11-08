---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046007"
---
# <span data-ttu-id="30ef4-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30ef4-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="30ef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="30ef4-103">Azure 로컬 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="30ef4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30ef4-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30ef4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="30ef4-106">**새-AzureLocalNetworkGateway** Cmdlet은 Azure 로컬 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="30ef4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30ef4-107">EXAMPLES</span></span>

## <span data-ttu-id="30ef4-108">변수</span><span class="sxs-lookup"><span data-stu-id="30ef4-108">PARAMETERS</span></span>

### <span data-ttu-id="30ef4-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="30ef4-109">-AddressSpace</span></span>
<span data-ttu-id="30ef4-110">주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="30ef4-111">-Asn</span><span class="sxs-lookup"><span data-stu-id="30ef4-111">-Asn</span></span>
<span data-ttu-id="30ef4-112">ASN (익명 시스템 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="30ef4-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="30ef4-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="30ef4-114">BGP (Border Gateway Protocol) 피어 링 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="30ef4-115">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="30ef4-115">-GatewayName</span></span>
<span data-ttu-id="30ef4-116">게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="30ef4-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="30ef4-117">-IpAddress</span></span>
<span data-ttu-id="30ef4-118">IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="30ef4-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="30ef4-119">-PeerWeight</span></span>
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

### <span data-ttu-id="30ef4-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="30ef4-120">-Profile</span></span>
<span data-ttu-id="30ef4-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="30ef4-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30ef4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ef4-123">CommonParameters</span></span>
<span data-ttu-id="30ef4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30ef4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ef4-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ef4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ef4-126">입력</span><span class="sxs-lookup"><span data-stu-id="30ef4-126">INPUTS</span></span>

## <span data-ttu-id="30ef4-127">출력</span><span class="sxs-lookup"><span data-stu-id="30ef4-127">OUTPUTS</span></span>

## <span data-ttu-id="30ef4-128">상속자</span><span class="sxs-lookup"><span data-stu-id="30ef4-128">NOTES</span></span>

## <span data-ttu-id="30ef4-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30ef4-129">RELATED LINKS</span></span>

[<span data-ttu-id="30ef4-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="30ef4-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="30ef4-131">-AzureLocalNetworkGateway 제거</span><span class="sxs-lookup"><span data-stu-id="30ef4-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="30ef4-132">-AzureLocalNetworkGateway 다시 설정</span><span class="sxs-lookup"><span data-stu-id="30ef4-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


