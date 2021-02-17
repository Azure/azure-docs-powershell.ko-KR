---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191556"
---
# <span data-ttu-id="794c2-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="794c2-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="794c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="794c2-102">SYNOPSIS</span></span>
<span data-ttu-id="794c2-103">가상 네트워크에서 개인 IP 주소의 가용성을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="794c2-104">구문</span><span class="sxs-lookup"><span data-stu-id="794c2-104">SYNTAX</span></span>

### <span data-ttu-id="794c2-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="794c2-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="794c2-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="794c2-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="794c2-107">설명</span><span class="sxs-lookup"><span data-stu-id="794c2-107">DESCRIPTION</span></span>
<span data-ttu-id="794c2-108">**Test-AzPrivateIPAddressAvailability** cmdlet은 지정된 개인 IP 주소를 가상 네트워크에서 사용할 수 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="794c2-109">이 cmdlet은 요청된 개인 IP 주소를 사용할 경우 사용 가능한 개인 IP 주소 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="794c2-110">예제</span><span class="sxs-lookup"><span data-stu-id="794c2-110">EXAMPLES</span></span>

### <span data-ttu-id="794c2-111">예제 1: 파이프라인을 사용하여 IP 주소를 사용할 수 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="794c2-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="794c2-112">이 명령은 가상 네트워크를 다운로드하고 파이프라인 연산자를 사용하여 지정된 개인 IP 주소를 사용할 수 있는지 여부를 테스트하는 **Test-AzPrivateIPAddressAvailability에** 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="794c2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="794c2-113">PARAMETERS</span></span>

### <span data-ttu-id="794c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794c2-114">-DefaultProfile</span></span>
<span data-ttu-id="794c2-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="794c2-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="794c2-116">-IPAddress</span></span>
<span data-ttu-id="794c2-117">테스트할 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="794c2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794c2-118">-ResourceGroupName</span></span>
<span data-ttu-id="794c2-119">가상 네트워크에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="794c2-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="794c2-120">-VirtualNetwork</span></span>
<span data-ttu-id="794c2-121">**PSVirtualNetwork 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="794c2-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="794c2-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="794c2-122">-VirtualNetworkName</span></span>
<span data-ttu-id="794c2-123">가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="794c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794c2-124">CommonParameters</span></span>
<span data-ttu-id="794c2-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="794c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794c2-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="794c2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794c2-127">입력</span><span class="sxs-lookup"><span data-stu-id="794c2-127">INPUTS</span></span>

### <span data-ttu-id="794c2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="794c2-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="794c2-129">출력</span><span class="sxs-lookup"><span data-stu-id="794c2-129">OUTPUTS</span></span>

### <span data-ttu-id="794c2-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="794c2-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="794c2-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="794c2-131">NOTES</span></span>

## <span data-ttu-id="794c2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="794c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="794c2-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="794c2-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


