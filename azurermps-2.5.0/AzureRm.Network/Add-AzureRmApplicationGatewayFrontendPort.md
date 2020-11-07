---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 7c4684dd2461446d2e04b1bca3f835647101c960
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881853"
---
# <span data-ttu-id="2fdde-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fdde-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="2fdde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fdde-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdde-103">응용 프로그램 게이트웨이에 프런트 엔드 포트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fdde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fdde-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fdde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2fdde-105">DESCRIPTION</span></span>
<span data-ttu-id="2fdde-106">**Add-AzureRmApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이에 프런트 엔드 포트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="2fdde-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2fdde-107">EXAMPLES</span></span>

### <span data-ttu-id="2fdde-108">예제 1: 응용 프로그램 게이트웨이에 프런트 엔드 포트 추가</span><span class="sxs-lookup"><span data-stu-id="2fdde-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="2fdde-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2fdde-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이의 프런트 엔드 포트로 포트 80를 추가 하 고 포트 FrontEndPort01를 이름으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="2fdde-111">변수</span><span class="sxs-lookup"><span data-stu-id="2fdde-111">PARAMETERS</span></span>

### <span data-ttu-id="2fdde-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fdde-112">-ApplicationGateway</span></span>
<span data-ttu-id="2fdde-113">이 cmdlet이 프런트 엔드 포트를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="2fdde-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdde-114">-DefaultProfile</span></span>
<span data-ttu-id="2fdde-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fdde-116">-이름</span><span class="sxs-lookup"><span data-stu-id="2fdde-116">-Name</span></span>
<span data-ttu-id="2fdde-117">프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="2fdde-118">-포트</span><span class="sxs-lookup"><span data-stu-id="2fdde-118">-Port</span></span>
<span data-ttu-id="2fdde-119">포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdde-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdde-120">CommonParameters</span></span>
<span data-ttu-id="2fdde-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fdde-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdde-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdde-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdde-123">입력</span><span class="sxs-lookup"><span data-stu-id="2fdde-123">INPUTS</span></span>

### <span data-ttu-id="2fdde-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2fdde-124">System.String</span></span>

## <span data-ttu-id="2fdde-125">출력</span><span class="sxs-lookup"><span data-stu-id="2fdde-125">OUTPUTS</span></span>

### <span data-ttu-id="2fdde-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fdde-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fdde-127">상속자</span><span class="sxs-lookup"><span data-stu-id="2fdde-127">NOTES</span></span>

## <span data-ttu-id="2fdde-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fdde-128">RELATED LINKS</span></span>

[<span data-ttu-id="2fdde-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fdde-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2fdde-130">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fdde-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2fdde-131">제거-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fdde-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2fdde-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2fdde-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


