---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872058"
---
# <span data-ttu-id="92760-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="92760-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="92760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92760-102">SYNOPSIS</span></span>
<span data-ttu-id="92760-103">가상 네트워크에서 개인 IP 주소의 사용 가능성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="92760-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92760-104">SYNTAX</span></span>

### <span data-ttu-id="92760-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="92760-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92760-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="92760-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92760-107">설명은</span><span class="sxs-lookup"><span data-stu-id="92760-107">DESCRIPTION</span></span>
<span data-ttu-id="92760-108">**테스트 AzPrivateIPAddressAvailability** cmdlet은 가상 네트워크에서 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="92760-109">이 cmdlet은 요청 된 개인 IP 주소를 가져온 경우 사용 가능한 개인 IP 주소 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="92760-110">예제의</span><span class="sxs-lookup"><span data-stu-id="92760-110">EXAMPLES</span></span>

### <span data-ttu-id="92760-111">예제 1: 파이프라인을 사용 하 여 IP 주소를 사용할 수 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="92760-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="92760-112">이 명령은 가상 네트워크를 가져오고 파이프라인 연산자를 사용 하 여 지정 된 개인 IP 주소를 사용할 수 있는지 여부를 테스트 하는 **테스트-AzPrivateIPAddressAvailability** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="92760-113">변수</span><span class="sxs-lookup"><span data-stu-id="92760-113">PARAMETERS</span></span>

### <span data-ttu-id="92760-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92760-114">-DefaultProfile</span></span>
<span data-ttu-id="92760-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92760-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92760-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="92760-116">-IPAddress</span></span>
<span data-ttu-id="92760-117">테스트할 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="92760-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92760-118">-ResourceGroupName</span></span>
<span data-ttu-id="92760-119">가상 네트워크에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="92760-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="92760-120">-VirtualNetwork</span></span>
<span data-ttu-id="92760-121">**PSVirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="92760-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="92760-122">-VirtualNetworkName</span></span>
<span data-ttu-id="92760-123">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="92760-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92760-124">CommonParameters</span></span>
<span data-ttu-id="92760-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92760-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92760-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92760-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92760-127">입력</span><span class="sxs-lookup"><span data-stu-id="92760-127">INPUTS</span></span>

### <span data-ttu-id="92760-128">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="92760-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="92760-129">출력</span><span class="sxs-lookup"><span data-stu-id="92760-129">OUTPUTS</span></span>

### <span data-ttu-id="92760-130">PSIPAddressAvailabilityResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="92760-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="92760-131">상속자</span><span class="sxs-lookup"><span data-stu-id="92760-131">NOTES</span></span>

## <span data-ttu-id="92760-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92760-132">RELATED LINKS</span></span>

[<span data-ttu-id="92760-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="92760-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


