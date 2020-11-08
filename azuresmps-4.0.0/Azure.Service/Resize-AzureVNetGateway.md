---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046087"
---
# <span data-ttu-id="12bd2-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="12bd2-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="12bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="12bd2-103">VPN 게이트웨이의 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="12bd2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12bd2-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="12bd2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="12bd2-106">**크기 조정-AzureVNetGateway** cmdlet은 가상 네트워크 VPN (가상 사설망) 게이트웨이를 다른 SKU로 크기 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="12bd2-107">가상 네트워크 게이트웨이의 유효한 Sku는 기본값, 표준 및 HighPerformance입니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="12bd2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="12bd2-108">EXAMPLES</span></span>

### <span data-ttu-id="12bd2-109">예제 1: 가상 네트워크 게이트웨이의 SKU 변경</span><span class="sxs-lookup"><span data-stu-id="12bd2-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="12bd2-110">이 명령은 ContosoVN07 이라는 가상 네트워크에 대 한 가상 네트워크 게이트웨이의 SKU를 HighPerformance로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="12bd2-111">변수</span><span class="sxs-lookup"><span data-stu-id="12bd2-111">PARAMETERS</span></span>

### <span data-ttu-id="12bd2-112">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="12bd2-112">-GatewaySKU</span></span>
<span data-ttu-id="12bd2-113">이 cmdlet이 가상 네트워크 게이트웨이의 크기를 조정 하는 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="12bd2-114">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-114">Valid values are:</span></span> 

- <span data-ttu-id="12bd2-115">기본값</span><span class="sxs-lookup"><span data-stu-id="12bd2-115">Default</span></span> 
- <span data-ttu-id="12bd2-116">표준이</span><span class="sxs-lookup"><span data-stu-id="12bd2-116">Standard</span></span> 
- <span data-ttu-id="12bd2-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="12bd2-117">HighPerformance</span></span>

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

### <span data-ttu-id="12bd2-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="12bd2-118">-Profile</span></span>
<span data-ttu-id="12bd2-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="12bd2-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12bd2-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="12bd2-121">-VNetName</span></span>
<span data-ttu-id="12bd2-122">이 cmdlet이 가상 네트워크 게이트웨이의 크기를 조정 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="12bd2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bd2-123">CommonParameters</span></span>
<span data-ttu-id="12bd2-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12bd2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bd2-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12bd2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bd2-126">입력</span><span class="sxs-lookup"><span data-stu-id="12bd2-126">INPUTS</span></span>

## <span data-ttu-id="12bd2-127">출력</span><span class="sxs-lookup"><span data-stu-id="12bd2-127">OUTPUTS</span></span>

## <span data-ttu-id="12bd2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="12bd2-128">NOTES</span></span>

## <span data-ttu-id="12bd2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12bd2-129">RELATED LINKS</span></span>

[<span data-ttu-id="12bd2-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="12bd2-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="12bd2-131">새-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="12bd2-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="12bd2-132">-AzureVNetGateway 제거</span><span class="sxs-lookup"><span data-stu-id="12bd2-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="12bd2-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="12bd2-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="12bd2-134">Set-Azurevnet2| Key</span><span class="sxs-lookup"><span data-stu-id="12bd2-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


