---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047726"
---
# <span data-ttu-id="34840-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="34840-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="34840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34840-102">SYNOPSIS</span></span>
<span data-ttu-id="34840-103">응용 프로그램 게이트웨이에 프런트 엔드 포트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="34840-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34840-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34840-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34840-105">DESCRIPTION</span></span>
<span data-ttu-id="34840-106">**Add-AzApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이에 프런트 엔드 포트를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="34840-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34840-107">EXAMPLES</span></span>

### <span data-ttu-id="34840-108">예제 1: 응용 프로그램 게이트웨이에 프런트 엔드 포트 추가</span><span class="sxs-lookup"><span data-stu-id="34840-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="34840-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="34840-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이의 프런트 엔드 포트로 포트 80를 추가 하 고 포트 FrontEndPort01를 이름으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34840-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="34840-111">변수</span><span class="sxs-lookup"><span data-stu-id="34840-111">PARAMETERS</span></span>

### <span data-ttu-id="34840-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34840-112">-ApplicationGateway</span></span>
<span data-ttu-id="34840-113">이 cmdlet이 프런트 엔드 포트를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="34840-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34840-114">-DefaultProfile</span></span>
<span data-ttu-id="34840-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34840-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34840-116">-이름</span><span class="sxs-lookup"><span data-stu-id="34840-116">-Name</span></span>
<span data-ttu-id="34840-117">프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="34840-118">-포트</span><span class="sxs-lookup"><span data-stu-id="34840-118">-Port</span></span>
<span data-ttu-id="34840-119">포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34840-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34840-120">CommonParameters</span></span>
<span data-ttu-id="34840-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34840-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34840-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34840-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34840-123">입력</span><span class="sxs-lookup"><span data-stu-id="34840-123">INPUTS</span></span>

### <span data-ttu-id="34840-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34840-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34840-125">출력</span><span class="sxs-lookup"><span data-stu-id="34840-125">OUTPUTS</span></span>

### <span data-ttu-id="34840-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34840-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34840-127">상속자</span><span class="sxs-lookup"><span data-stu-id="34840-127">NOTES</span></span>

## <span data-ttu-id="34840-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34840-128">RELATED LINKS</span></span>

[<span data-ttu-id="34840-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="34840-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="34840-130">새로운 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="34840-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="34840-131">제거-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="34840-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="34840-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="34840-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


