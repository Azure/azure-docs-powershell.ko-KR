---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044835"
---
# <span data-ttu-id="50762-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="50762-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="50762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50762-102">SYNOPSIS</span></span>
<span data-ttu-id="50762-103">Http 상태 코드와 사용자 지정 오류 페이지 url을 사용 하 여 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50762-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="50762-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50762-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50762-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50762-105">DESCRIPTION</span></span>
<span data-ttu-id="50762-106">**AzApplicationGatewayCustomError** cmdlet은 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50762-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="50762-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50762-107">EXAMPLES</span></span>

### <span data-ttu-id="50762-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="50762-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="50762-109">이 명령은 http 상태 코드 403의 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50762-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="50762-110">변수</span><span class="sxs-lookup"><span data-stu-id="50762-110">PARAMETERS</span></span>

### <span data-ttu-id="50762-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="50762-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="50762-112">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="50762-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="50762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50762-113">-DefaultProfile</span></span>
<span data-ttu-id="50762-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50762-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50762-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="50762-115">-StatusCode</span></span>
<span data-ttu-id="50762-116">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="50762-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="50762-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50762-117">CommonParameters</span></span>
<span data-ttu-id="50762-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50762-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50762-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50762-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50762-120">입력</span><span class="sxs-lookup"><span data-stu-id="50762-120">INPUTS</span></span>

### <span data-ttu-id="50762-121">않아야</span><span class="sxs-lookup"><span data-stu-id="50762-121">None</span></span>

## <span data-ttu-id="50762-122">출력</span><span class="sxs-lookup"><span data-stu-id="50762-122">OUTPUTS</span></span>

### <span data-ttu-id="50762-123">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="50762-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="50762-124">상속자</span><span class="sxs-lookup"><span data-stu-id="50762-124">NOTES</span></span>

## <span data-ttu-id="50762-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50762-125">RELATED LINKS</span></span>

[<span data-ttu-id="50762-126">추가-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="50762-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="50762-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="50762-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="50762-128">제거-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="50762-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="50762-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="50762-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
