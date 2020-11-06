---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530168"
---
# <span data-ttu-id="a3cfb-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a3cfb-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a3cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a3cfb-103">응용 프로그램 게이트웨이에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3cfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3cfb-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3cfb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="a3cfb-106">**Set-AzureRmApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이에서 사용자 지정 오류를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="a3cfb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a3cfb-107">EXAMPLES</span></span>

### <span data-ttu-id="a3cfb-108">예제 1: 응용 프로그램 게이트웨이에서 사용자 지정 오류 업데이트</span><span class="sxs-lookup"><span data-stu-id="a3cfb-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="a3cfb-109">이 명령은 응용 프로그램 게이트웨이에서 $appgw http 상태 코드 502의 사용자 지정 오류를 업데이트 하 고 업데이트 된 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="a3cfb-110">변수</span><span class="sxs-lookup"><span data-stu-id="a3cfb-110">PARAMETERS</span></span>

### <span data-ttu-id="a3cfb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3cfb-111">-ApplicationGateway</span></span>
<span data-ttu-id="a3cfb-112">응용 프로그램 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="a3cfb-112">The Application Gateway</span></span>

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

### <span data-ttu-id="a3cfb-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="a3cfb-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="a3cfb-114">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a3cfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3cfb-115">-DefaultProfile</span></span>
<span data-ttu-id="a3cfb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3cfb-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a3cfb-117">-StatusCode</span></span>
<span data-ttu-id="a3cfb-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a3cfb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3cfb-119">CommonParameters</span></span>
<span data-ttu-id="a3cfb-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3cfb-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3cfb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3cfb-122">입력</span><span class="sxs-lookup"><span data-stu-id="a3cfb-122">INPUTS</span></span>

### <span data-ttu-id="a3cfb-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3cfb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3cfb-124">출력</span><span class="sxs-lookup"><span data-stu-id="a3cfb-124">OUTPUTS</span></span>

### <span data-ttu-id="a3cfb-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3cfb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3cfb-126">상속자</span><span class="sxs-lookup"><span data-stu-id="a3cfb-126">NOTES</span></span>

## <span data-ttu-id="a3cfb-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3cfb-127">RELATED LINKS</span></span>
