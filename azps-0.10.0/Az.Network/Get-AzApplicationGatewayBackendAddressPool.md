---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875641"
---
# <span data-ttu-id="637f8-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="637f8-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="637f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="637f8-102">SYNOPSIS</span></span>
<span data-ttu-id="637f8-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="637f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="637f8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="637f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="637f8-105">DESCRIPTION</span></span>

## <span data-ttu-id="637f8-106">예제의</span><span class="sxs-lookup"><span data-stu-id="637f8-106">EXAMPLES</span></span>

### <span data-ttu-id="637f8-107">예제 1: 지정 된 백 엔드 서버 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="637f8-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="637f8-108">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="637f8-109">두 번째 명령은 Pool01 이라는 $AppGw와 연결 된 백 엔드 주소 풀을 가져와 $BackendPool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="637f8-110">예제 2: 백 엔드 서버 풀 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="637f8-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="637f8-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="637f8-112">두 번째 명령은 $AppGw와 연결 된 백 엔드 주소 풀 목록을 가져오고 목록을 $BackendPools 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="637f8-113">변수</span><span class="sxs-lookup"><span data-stu-id="637f8-113">PARAMETERS</span></span>

### <span data-ttu-id="637f8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="637f8-114">-ApplicationGateway</span></span>
<span data-ttu-id="637f8-115">**AzApplicationGatewayBackendAddressPool** cmdlet은 응용 프로그램 게이트웨이에 대 한 백 엔드 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="637f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637f8-116">-DefaultProfile</span></span>
<span data-ttu-id="637f8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="637f8-118">-이름</span><span class="sxs-lookup"><span data-stu-id="637f8-118">-Name</span></span>
<span data-ttu-id="637f8-119">이 cmdlet이 가져오는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="637f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637f8-120">CommonParameters</span></span>
<span data-ttu-id="637f8-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="637f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637f8-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="637f8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637f8-123">입력</span><span class="sxs-lookup"><span data-stu-id="637f8-123">INPUTS</span></span>

### <span data-ttu-id="637f8-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="637f8-124">System.String</span></span>

## <span data-ttu-id="637f8-125">출력</span><span class="sxs-lookup"><span data-stu-id="637f8-125">OUTPUTS</span></span>

### <span data-ttu-id="637f8-126">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="637f8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="637f8-127">상속자</span><span class="sxs-lookup"><span data-stu-id="637f8-127">NOTES</span></span>

## <span data-ttu-id="637f8-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="637f8-128">RELATED LINKS</span></span>

[<span data-ttu-id="637f8-129">추가-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="637f8-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="637f8-130">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="637f8-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="637f8-131">제거-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="637f8-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="637f8-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="637f8-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


