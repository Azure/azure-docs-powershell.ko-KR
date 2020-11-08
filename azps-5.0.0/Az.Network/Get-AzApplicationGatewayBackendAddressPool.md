---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218360"
---
# <span data-ttu-id="e60e1-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e60e1-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e60e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e60e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e60e1-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="e60e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e60e1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e60e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e60e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e60e1-106">**AzApplicationGatewayBackendAddressPool** cmdlet은 응용 프로그램 게이트웨이에서 하나 이상의 백 엔드 주소 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="e60e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e60e1-107">EXAMPLES</span></span>

### <span data-ttu-id="e60e1-108">예제 1: 지정 된 백 엔드 서버 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="e60e1-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e60e1-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e60e1-110">두 번째 명령은 Pool01 이라는 $AppGw와 연결 된 백 엔드 주소 풀을 가져와 $BackendPool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="e60e1-111">예제 2: 백 엔드 서버 풀 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="e60e1-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="e60e1-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e60e1-113">두 번째 명령은 $AppGw와 연결 된 백 엔드 주소 풀 목록을 가져오고 목록을 $BackendPools 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="e60e1-114">변수</span><span class="sxs-lookup"><span data-stu-id="e60e1-114">PARAMETERS</span></span>

### <span data-ttu-id="e60e1-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e60e1-115">-ApplicationGateway</span></span>
<span data-ttu-id="e60e1-116">**AzApplicationGatewayBackendAddressPool** cmdlet은 응용 프로그램 게이트웨이에 대 한 백 엔드 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="e60e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60e1-117">-DefaultProfile</span></span>
<span data-ttu-id="e60e1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e60e1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e60e1-119">-Name</span></span>
<span data-ttu-id="e60e1-120">이 cmdlet이 가져오는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e60e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60e1-121">CommonParameters</span></span>
<span data-ttu-id="e60e1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e60e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60e1-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e60e1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60e1-124">입력</span><span class="sxs-lookup"><span data-stu-id="e60e1-124">INPUTS</span></span>

### <span data-ttu-id="e60e1-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e60e1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e60e1-126">출력</span><span class="sxs-lookup"><span data-stu-id="e60e1-126">OUTPUTS</span></span>

### <span data-ttu-id="e60e1-127">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e60e1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e60e1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e60e1-128">NOTES</span></span>

## <span data-ttu-id="e60e1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e60e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="e60e1-130">추가-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e60e1-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e60e1-131">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e60e1-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e60e1-132">제거-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e60e1-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e60e1-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e60e1-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


