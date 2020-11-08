---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034870"
---
# <span data-ttu-id="9ae72-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ae72-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9ae72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ae72-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae72-103">응용 프로그램 게이트웨이에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="9ae72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ae72-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae72-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ae72-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae72-106">**Set-AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="9ae72-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ae72-107">EXAMPLES</span></span>

### <span data-ttu-id="9ae72-108">예제 1: 응용 프로그램 게이트웨이에서 사용자 지정 오류 업데이트</span><span class="sxs-lookup"><span data-stu-id="9ae72-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="9ae72-109">이 명령은 응용 프로그램 게이트웨이에서 $appgw http 상태 코드 502의 사용자 지정 오류를 업데이트 하 고 업데이트 된 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="9ae72-110">변수</span><span class="sxs-lookup"><span data-stu-id="9ae72-110">PARAMETERS</span></span>

### <span data-ttu-id="9ae72-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ae72-111">-ApplicationGateway</span></span>
<span data-ttu-id="9ae72-112">응용 프로그램 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="9ae72-112">The Application Gateway</span></span>

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

### <span data-ttu-id="9ae72-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="9ae72-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="9ae72-114">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9ae72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae72-115">-DefaultProfile</span></span>
<span data-ttu-id="9ae72-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae72-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9ae72-117">-StatusCode</span></span>
<span data-ttu-id="9ae72-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9ae72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae72-119">CommonParameters</span></span>
<span data-ttu-id="9ae72-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ae72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae72-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae72-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae72-122">입력</span><span class="sxs-lookup"><span data-stu-id="9ae72-122">INPUTS</span></span>

### <span data-ttu-id="9ae72-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ae72-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ae72-124">출력</span><span class="sxs-lookup"><span data-stu-id="9ae72-124">OUTPUTS</span></span>

### <span data-ttu-id="9ae72-125">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ae72-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9ae72-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9ae72-126">NOTES</span></span>

## <span data-ttu-id="9ae72-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ae72-127">RELATED LINKS</span></span>

[<span data-ttu-id="9ae72-128">추가-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ae72-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9ae72-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ae72-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9ae72-130">새로운 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ae72-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9ae72-131">제거-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ae72-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
