---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 377145933832c587691ed30db08754ef1e6f1f64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971920"
---
# <span data-ttu-id="851f3-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="851f3-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="851f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="851f3-102">SYNOPSIS</span></span>
<span data-ttu-id="851f3-103">http 상태 코드 및 사용자 지정 오류 페이지 URL을 사용하여 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="851f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="851f3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="851f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="851f3-105">DESCRIPTION</span></span>
<span data-ttu-id="851f3-106">**New-AzApplicationGatewayCustomError** cmdlet은 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="851f3-107">예제</span><span class="sxs-lookup"><span data-stu-id="851f3-107">EXAMPLES</span></span>

### <span data-ttu-id="851f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="851f3-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="851f3-109">이 명령은 http 상태 코드 403의 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="851f3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="851f3-110">PARAMETERS</span></span>

### <span data-ttu-id="851f3-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="851f3-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="851f3-112">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="851f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851f3-113">-DefaultProfile</span></span>
<span data-ttu-id="851f3-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="851f3-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="851f3-115">-StatusCode</span></span>
<span data-ttu-id="851f3-116">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="851f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851f3-117">CommonParameters</span></span>
<span data-ttu-id="851f3-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="851f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851f3-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="851f3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851f3-120">입력</span><span class="sxs-lookup"><span data-stu-id="851f3-120">INPUTS</span></span>

### <span data-ttu-id="851f3-121">없음</span><span class="sxs-lookup"><span data-stu-id="851f3-121">None</span></span>

## <span data-ttu-id="851f3-122">출력</span><span class="sxs-lookup"><span data-stu-id="851f3-122">OUTPUTS</span></span>

### <span data-ttu-id="851f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="851f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="851f3-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="851f3-124">NOTES</span></span>

## <span data-ttu-id="851f3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="851f3-125">RELATED LINKS</span></span>

[<span data-ttu-id="851f3-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="851f3-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="851f3-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="851f3-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="851f3-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="851f3-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="851f3-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="851f3-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
