---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
ms.openlocfilehash: 73924c1d1308a4cf457033e27e49ad7f9e19392e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880890"
---
# <span data-ttu-id="a8fc7-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="a8fc7-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="a8fc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fc7-103">가상 네트워크에서 개인 IP 주소의 사용 가능성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8fc7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8fc7-104">SYNTAX</span></span>

### <span data-ttu-id="a8fc7-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="a8fc7-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8fc7-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8fc7-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8fc7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a8fc7-107">DESCRIPTION</span></span>
<span data-ttu-id="a8fc7-108">**테스트 AzureRmPrivateIPAddressAvailability** cmdlet은 가상 네트워크에서 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="a8fc7-109">이 cmdlet은 요청 된 개인 IP 주소를 가져온 경우 사용 가능한 개인 IP 주소 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="a8fc7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a8fc7-110">EXAMPLES</span></span>

### <span data-ttu-id="a8fc7-111">예제 1: 파이프라인을 사용 하 여 IP 주소를 사용할 수 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="a8fc7-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="a8fc7-112">이 명령은 가상 네트워크를 가져오고 파이프라인 연산자를 사용 하 여 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 하는 **테스트-AzureRmPrivateIPAddressAvailability** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="a8fc7-113">변수</span><span class="sxs-lookup"><span data-stu-id="a8fc7-113">PARAMETERS</span></span>

### <span data-ttu-id="a8fc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fc7-114">-DefaultProfile</span></span>
<span data-ttu-id="a8fc7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8fc7-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a8fc7-116">-IPAddress</span></span>
<span data-ttu-id="a8fc7-117">테스트할 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="a8fc7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fc7-118">-ResourceGroupName</span></span>
<span data-ttu-id="a8fc7-119">가상 네트워크에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fc7-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8fc7-120">-VirtualNetwork</span></span>
<span data-ttu-id="a8fc7-121">**PSVirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fc7-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a8fc7-122">-VirtualNetworkName</span></span>
<span data-ttu-id="a8fc7-123">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fc7-124">CommonParameters</span></span>
<span data-ttu-id="a8fc7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fc7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8fc7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fc7-127">입력</span><span class="sxs-lookup"><span data-stu-id="a8fc7-127">INPUTS</span></span>

### <span data-ttu-id="a8fc7-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8fc7-128">PSVirtualNetwork</span></span>
<span data-ttu-id="a8fc7-129">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a8fc7-130">출력</span><span class="sxs-lookup"><span data-stu-id="a8fc7-130">OUTPUTS</span></span>

### <span data-ttu-id="a8fc7-131">PSIPAddressAvailabilityResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a8fc7-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="a8fc7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a8fc7-132">NOTES</span></span>

## <span data-ttu-id="a8fc7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8fc7-133">RELATED LINKS</span></span>

[<span data-ttu-id="a8fc7-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8fc7-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

