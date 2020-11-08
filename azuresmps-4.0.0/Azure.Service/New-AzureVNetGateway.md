---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046187"
---
# <span data-ttu-id="56635-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56635-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="56635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56635-102">SYNOPSIS</span></span>
<span data-ttu-id="56635-103">가상 네트워크에서 VPN 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56635-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="56635-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56635-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56635-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56635-105">DESCRIPTION</span></span>
<span data-ttu-id="56635-106">**새-AzureVNetGateway** cmdlet은 가상 네트워크에 가상 개인 네트워크 (VPN) 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56635-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="56635-107">게이트웨이의 SKU (기본값, 표준 또는 HighPerformance)를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56635-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="56635-108">형식을 StaticRouting 또는 DynamicRouting 중에서 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56635-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="56635-109">예제의</span><span class="sxs-lookup"><span data-stu-id="56635-109">EXAMPLES</span></span>

### <span data-ttu-id="56635-110">예제 1: 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="56635-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="56635-111">이 명령은 ContosoVN07 이라는 가상 네트워크에 대 한 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56635-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="56635-112">게이트웨이는 기본 SKU이 고 동적 라우팅을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56635-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="56635-113">변수</span><span class="sxs-lookup"><span data-stu-id="56635-113">PARAMETERS</span></span>

### <span data-ttu-id="56635-114">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="56635-114">-GatewaySKU</span></span>
<span data-ttu-id="56635-115">이 cmdlet이 만드는 가상 네트워크 게이트웨이의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56635-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="56635-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56635-116">Valid values are:</span></span> 

- <span data-ttu-id="56635-117">기본값</span><span class="sxs-lookup"><span data-stu-id="56635-117">Default</span></span> 
- <span data-ttu-id="56635-118">표준이</span><span class="sxs-lookup"><span data-stu-id="56635-118">Standard</span></span> 
- <span data-ttu-id="56635-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="56635-119">HighPerformance</span></span>

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

### <span data-ttu-id="56635-120">-게이트웨이 종류</span><span class="sxs-lookup"><span data-stu-id="56635-120">-GatewayType</span></span>
<span data-ttu-id="56635-121">이 cmdlet이 만드는 게이트웨이의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56635-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="56635-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56635-122">Valid values are:</span></span> 

- <span data-ttu-id="56635-123">정적 라우팅</span><span class="sxs-lookup"><span data-stu-id="56635-123">StaticRouting</span></span> 
- <span data-ttu-id="56635-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="56635-124">DynamicRouting</span></span>

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

### <span data-ttu-id="56635-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="56635-125">-Profile</span></span>
<span data-ttu-id="56635-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56635-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="56635-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="56635-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56635-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="56635-128">-VNetName</span></span>
<span data-ttu-id="56635-129">이 cmdlet이 가상 네트워크 게이트웨이를 추가 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56635-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="56635-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56635-130">CommonParameters</span></span>
<span data-ttu-id="56635-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56635-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56635-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56635-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56635-133">입력</span><span class="sxs-lookup"><span data-stu-id="56635-133">INPUTS</span></span>

## <span data-ttu-id="56635-134">출력</span><span class="sxs-lookup"><span data-stu-id="56635-134">OUTPUTS</span></span>

## <span data-ttu-id="56635-135">상속자</span><span class="sxs-lookup"><span data-stu-id="56635-135">NOTES</span></span>

## <span data-ttu-id="56635-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56635-136">RELATED LINKS</span></span>

[<span data-ttu-id="56635-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56635-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="56635-138">-AzureVNetGateway 제거</span><span class="sxs-lookup"><span data-stu-id="56635-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="56635-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56635-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="56635-140">크기 조정-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56635-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="56635-141">Set-Azurevnet2| Key</span><span class="sxs-lookup"><span data-stu-id="56635-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


