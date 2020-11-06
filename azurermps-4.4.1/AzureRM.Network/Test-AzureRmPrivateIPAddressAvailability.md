---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 880e079d5facec2edc20f38d7d1e1d4c9ba41e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530756"
---
# <span data-ttu-id="5bbe1-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="5bbe1-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="5bbe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bbe1-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbe1-103">가상 네트워크에서 개인 IP 주소의 사용 가능성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bbe1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5bbe1-104">SYNTAX</span></span>

### <span data-ttu-id="5bbe1-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="5bbe1-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bbe1-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="5bbe1-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bbe1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5bbe1-107">DESCRIPTION</span></span>
<span data-ttu-id="5bbe1-108">**테스트 AzureRmPrivateIPAddressAvailability** cmdlet은 가상 네트워크에서 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="5bbe1-109">이 cmdlet은 요청 된 개인 IP 주소를 가져온 경우 사용 가능한 개인 IP 주소 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="5bbe1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5bbe1-110">EXAMPLES</span></span>

### <span data-ttu-id="5bbe1-111">예제 1: 파이프라인을 사용 하 여 IP 주소를 사용할 수 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="5bbe1-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="5bbe1-112">이 명령은 가상 네트워크를 가져오고 파이프라인 연산자를 사용 하 여 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 하는 **테스트-AzureRmPrivateIPAddressAvailability** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="5bbe1-113">변수</span><span class="sxs-lookup"><span data-stu-id="5bbe1-113">PARAMETERS</span></span>

### <span data-ttu-id="5bbe1-114">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="5bbe1-114">-IPAddress</span></span>
<span data-ttu-id="5bbe1-115">테스트할 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-115">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="5bbe1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bbe1-116">-ResourceGroupName</span></span>
<span data-ttu-id="5bbe1-117">가상 네트워크에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-117">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="5bbe1-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bbe1-118">-VirtualNetwork</span></span>
<span data-ttu-id="5bbe1-119">**PSVirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-119">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="5bbe1-120">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5bbe1-120">-VirtualNetworkName</span></span>
<span data-ttu-id="5bbe1-121">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-121">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="5bbe1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbe1-122">-DefaultProfile</span></span>
<span data-ttu-id="5bbe1-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bbe1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbe1-124">CommonParameters</span></span>
<span data-ttu-id="5bbe1-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbe1-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbe1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbe1-127">입력</span><span class="sxs-lookup"><span data-stu-id="5bbe1-127">INPUTS</span></span>

### <span data-ttu-id="5bbe1-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bbe1-128">PSVirtualNetwork</span></span>
<span data-ttu-id="5bbe1-129">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5bbe1-130">출력</span><span class="sxs-lookup"><span data-stu-id="5bbe1-130">OUTPUTS</span></span>

### <span data-ttu-id="5bbe1-131">PSIPAddressAvailabilityResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="5bbe1-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5bbe1-132">NOTES</span></span>

## <span data-ttu-id="5bbe1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bbe1-133">RELATED LINKS</span></span>

[<span data-ttu-id="5bbe1-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5bbe1-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


