---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878138"
---
# <span data-ttu-id="07ae3-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="07ae3-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="07ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="07ae3-103">가상 네트워크에서 개인 IP 주소의 사용 가능성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="07ae3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07ae3-104">SYNTAX</span></span>

### <span data-ttu-id="07ae3-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="07ae3-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ae3-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="07ae3-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ae3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="07ae3-107">DESCRIPTION</span></span>
<span data-ttu-id="07ae3-108">**테스트 AzPrivateIPAddressAvailability** cmdlet은 가상 네트워크에서 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="07ae3-109">이 cmdlet은 요청 된 개인 IP 주소를 가져온 경우 사용 가능한 개인 IP 주소 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="07ae3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="07ae3-110">EXAMPLES</span></span>

### <span data-ttu-id="07ae3-111">예제 1: 파이프라인을 사용 하 여 IP 주소를 사용할 수 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="07ae3-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="07ae3-112">이 명령은 가상 네트워크를 가져오고 파이프라인 연산자를 사용 하 여 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 하는 **테스트-AzPrivateIPAddressAvailability** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="07ae3-113">변수</span><span class="sxs-lookup"><span data-stu-id="07ae3-113">PARAMETERS</span></span>

### <span data-ttu-id="07ae3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ae3-114">-DefaultProfile</span></span>
<span data-ttu-id="07ae3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ae3-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="07ae3-116">-IPAddress</span></span>
<span data-ttu-id="07ae3-117">테스트할 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-117">Specifies the IP address to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ae3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ae3-118">-ResourceGroupName</span></span>
<span data-ttu-id="07ae3-119">가상 네트워크에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ae3-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="07ae3-120">-VirtualNetwork</span></span>
<span data-ttu-id="07ae3-121">**PSVirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ae3-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="07ae3-122">-VirtualNetworkName</span></span>
<span data-ttu-id="07ae3-123">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ae3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ae3-124">CommonParameters</span></span>
<span data-ttu-id="07ae3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ae3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ae3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ae3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ae3-127">입력</span><span class="sxs-lookup"><span data-stu-id="07ae3-127">INPUTS</span></span>

### <span data-ttu-id="07ae3-128">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="07ae3-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="07ae3-129">출력</span><span class="sxs-lookup"><span data-stu-id="07ae3-129">OUTPUTS</span></span>

### <span data-ttu-id="07ae3-130">PSIPAddressAvailabilityResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="07ae3-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="07ae3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="07ae3-131">NOTES</span></span>

## <span data-ttu-id="07ae3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07ae3-132">RELATED LINKS</span></span>

[<span data-ttu-id="07ae3-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="07ae3-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


