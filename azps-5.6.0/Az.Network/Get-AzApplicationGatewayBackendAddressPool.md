---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 458788041ce833cacb30616a7aa8268ed485c65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978320"
---
# <span data-ttu-id="e18df-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e18df-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e18df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e18df-102">SYNOPSIS</span></span>
<span data-ttu-id="e18df-103">애플리케이션 게이트웨이에 대한 백 엔드 주소 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="e18df-104">구문</span><span class="sxs-lookup"><span data-stu-id="e18df-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e18df-105">설명</span><span class="sxs-lookup"><span data-stu-id="e18df-105">DESCRIPTION</span></span>
<span data-ttu-id="e18df-106">**Get-AzApplicationGatewayBackendAddressPool** cmdlet은 애플리케이션 게이트웨이에서 하나 이상의 백END 주소 풀 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="e18df-107">예제</span><span class="sxs-lookup"><span data-stu-id="e18df-107">EXAMPLES</span></span>

### <span data-ttu-id="e18df-108">예제 1: 지정된 백 엔드 서버 풀을 얻다</span><span class="sxs-lookup"><span data-stu-id="e18df-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e18df-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e18df-110">두 번째 명령은 Pool01이라는 이름의 $AppGw 연결된 백 엔드 주소 풀을 $BackendPool 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="e18df-111">예제 2: 백 엔드 서버 풀 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="e18df-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="e18df-112">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e18df-113">두 번째 명령은 와 연결된 백 엔드 주소 풀의 목록을 $AppGw 및 목록은 $BackendPools 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="e18df-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e18df-114">PARAMETERS</span></span>

### <span data-ttu-id="e18df-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e18df-115">-ApplicationGateway</span></span>
<span data-ttu-id="e18df-116">**Get-AzApplicationGatewayBackendAddressPool** cmdlet은 애플리케이션 게이트웨이에 대한 백 엔드 주소 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e18df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18df-117">-DefaultProfile</span></span>
<span data-ttu-id="e18df-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e18df-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e18df-119">-Name</span></span>
<span data-ttu-id="e18df-120">이 cmdlet이 얻을 백 엔드 주소 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18df-121">CommonParameters</span></span>
<span data-ttu-id="e18df-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e18df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18df-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e18df-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18df-124">입력</span><span class="sxs-lookup"><span data-stu-id="e18df-124">INPUTS</span></span>

### <span data-ttu-id="e18df-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e18df-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e18df-126">출력</span><span class="sxs-lookup"><span data-stu-id="e18df-126">OUTPUTS</span></span>

### <span data-ttu-id="e18df-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e18df-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e18df-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e18df-128">NOTES</span></span>

## <span data-ttu-id="e18df-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e18df-129">RELATED LINKS</span></span>

[<span data-ttu-id="e18df-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e18df-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e18df-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e18df-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e18df-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e18df-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e18df-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e18df-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


