---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046186"
---
# <span data-ttu-id="2771b-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2771b-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="2771b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2771b-102">SYNOPSIS</span></span>
<span data-ttu-id="2771b-103">Azure 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="2771b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2771b-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2771b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2771b-105">DESCRIPTION</span></span>
<span data-ttu-id="2771b-106">**새 AzureVirtualNetworkGateway** Cmdlet은 Azure 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="2771b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2771b-107">EXAMPLES</span></span>

## <span data-ttu-id="2771b-108">변수</span><span class="sxs-lookup"><span data-stu-id="2771b-108">PARAMETERS</span></span>

### <span data-ttu-id="2771b-109">-Asn</span><span class="sxs-lookup"><span data-stu-id="2771b-109">-Asn</span></span>
<span data-ttu-id="2771b-110">ASN (익명 시스템 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-110">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="2771b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2771b-111">-Force</span></span>
<span data-ttu-id="2771b-112">Azure 가상 네트워크 게이트웨이 만들기 확인 안 함</span><span class="sxs-lookup"><span data-stu-id="2771b-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

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

### <span data-ttu-id="2771b-113">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="2771b-113">-GatewayName</span></span>
<span data-ttu-id="2771b-114">게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="2771b-115">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="2771b-115">-GatewaySKU</span></span>
<span data-ttu-id="2771b-116">이 cmdlet이 만드는 가상 네트워크 게이트웨이의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="2771b-117">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-117">Valid values are:</span></span>

- <span data-ttu-id="2771b-118">기본값</span><span class="sxs-lookup"><span data-stu-id="2771b-118">Default</span></span>
- <span data-ttu-id="2771b-119">표준이</span><span class="sxs-lookup"><span data-stu-id="2771b-119">Standard</span></span>
- <span data-ttu-id="2771b-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="2771b-120">HighPerformance</span></span>

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

### <span data-ttu-id="2771b-121">-게이트웨이 종류</span><span class="sxs-lookup"><span data-stu-id="2771b-121">-GatewayType</span></span>
<span data-ttu-id="2771b-122">게이트웨이의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="2771b-123">-위치</span><span class="sxs-lookup"><span data-stu-id="2771b-123">-Location</span></span>
<span data-ttu-id="2771b-124">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-124">Specifies the location.</span></span>

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

### <span data-ttu-id="2771b-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2771b-125">-PeerWeight</span></span>
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

### <span data-ttu-id="2771b-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="2771b-126">-Profile</span></span>
<span data-ttu-id="2771b-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2771b-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2771b-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="2771b-129">-VnetId</span></span>
<span data-ttu-id="2771b-130">가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="2771b-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="2771b-131">-VNetName</span></span>
<span data-ttu-id="2771b-132">가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="2771b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2771b-133">CommonParameters</span></span>
<span data-ttu-id="2771b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2771b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2771b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2771b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2771b-136">입력</span><span class="sxs-lookup"><span data-stu-id="2771b-136">INPUTS</span></span>

## <span data-ttu-id="2771b-137">출력</span><span class="sxs-lookup"><span data-stu-id="2771b-137">OUTPUTS</span></span>

## <span data-ttu-id="2771b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2771b-138">NOTES</span></span>

## <span data-ttu-id="2771b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2771b-139">RELATED LINKS</span></span>

[<span data-ttu-id="2771b-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2771b-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2771b-141">제거-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2771b-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2771b-142">크기 조정-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2771b-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
