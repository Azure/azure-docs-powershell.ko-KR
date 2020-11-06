---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 05e71fc334ae45f8a74a4afbeaa33be5816b6532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534263"
---
# <span data-ttu-id="be0d9-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be0d9-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="be0d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="be0d9-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be0d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be0d9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be0d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be0d9-105">DESCRIPTION</span></span>

## <span data-ttu-id="be0d9-106">예제의</span><span class="sxs-lookup"><span data-stu-id="be0d9-106">EXAMPLES</span></span>

### <span data-ttu-id="be0d9-107">예제 1: 지정 된 백 엔드 서버 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="be0d9-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="be0d9-108">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="be0d9-109">두 번째 명령은 Pool01 이라는 $AppGw와 연결 된 백 엔드 주소 풀을 가져와 $BackendPool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="be0d9-110">예제 2: 백 엔드 서버 풀 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="be0d9-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="be0d9-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="be0d9-112">두 번째 명령은 $AppGw와 연결 된 백 엔드 주소 풀 목록을 가져오고 목록을 $BackendPools 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="be0d9-113">변수</span><span class="sxs-lookup"><span data-stu-id="be0d9-113">PARAMETERS</span></span>

### <span data-ttu-id="be0d9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be0d9-114">-ApplicationGateway</span></span>
<span data-ttu-id="be0d9-115">**AzureRmApplicationGatewayBackendAddressPool** cmdlet은 응용 프로그램 게이트웨이에 대 한 백 엔드 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="be0d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0d9-116">-DefaultProfile</span></span>
<span data-ttu-id="be0d9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be0d9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="be0d9-118">-Name</span></span>
<span data-ttu-id="be0d9-119">이 cmdlet이 가져오는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="be0d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0d9-120">CommonParameters</span></span>
<span data-ttu-id="be0d9-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0d9-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be0d9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0d9-123">입력</span><span class="sxs-lookup"><span data-stu-id="be0d9-123">INPUTS</span></span>

### <span data-ttu-id="be0d9-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be0d9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="be0d9-125">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be0d9-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="be0d9-126">출력</span><span class="sxs-lookup"><span data-stu-id="be0d9-126">OUTPUTS</span></span>

### <span data-ttu-id="be0d9-127">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="be0d9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="be0d9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="be0d9-128">NOTES</span></span>

## <span data-ttu-id="be0d9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be0d9-129">RELATED LINKS</span></span>

[<span data-ttu-id="be0d9-130">추가-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be0d9-130">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="be0d9-131">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be0d9-131">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="be0d9-132">제거-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be0d9-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="be0d9-133">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be0d9-133">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


