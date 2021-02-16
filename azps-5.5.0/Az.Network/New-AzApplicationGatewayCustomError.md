---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202966"
---
# <span data-ttu-id="dbf10-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbf10-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="dbf10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf10-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf10-103">http 상태 코드 및 사용자 지정 오류 페이지 URL을 사용하여 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="dbf10-104">구문</span><span class="sxs-lookup"><span data-stu-id="dbf10-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbf10-105">설명</span><span class="sxs-lookup"><span data-stu-id="dbf10-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf10-106">**New-AzApplicationGatewayCustomError** cmdlet은 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="dbf10-107">예제</span><span class="sxs-lookup"><span data-stu-id="dbf10-107">EXAMPLES</span></span>

### <span data-ttu-id="dbf10-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbf10-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="dbf10-109">이 명령은 http 상태 코드 403의 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="dbf10-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbf10-110">PARAMETERS</span></span>

### <span data-ttu-id="dbf10-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="dbf10-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="dbf10-112">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="dbf10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf10-113">-DefaultProfile</span></span>
<span data-ttu-id="dbf10-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf10-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="dbf10-115">-StatusCode</span></span>
<span data-ttu-id="dbf10-116">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="dbf10-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf10-117">CommonParameters</span></span>
<span data-ttu-id="dbf10-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf10-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf10-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dbf10-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf10-120">입력</span><span class="sxs-lookup"><span data-stu-id="dbf10-120">INPUTS</span></span>

### <span data-ttu-id="dbf10-121">없음</span><span class="sxs-lookup"><span data-stu-id="dbf10-121">None</span></span>

## <span data-ttu-id="dbf10-122">출력</span><span class="sxs-lookup"><span data-stu-id="dbf10-122">OUTPUTS</span></span>

### <span data-ttu-id="dbf10-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbf10-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="dbf10-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dbf10-124">NOTES</span></span>

## <span data-ttu-id="dbf10-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbf10-125">RELATED LINKS</span></span>

[<span data-ttu-id="dbf10-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbf10-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="dbf10-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbf10-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="dbf10-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbf10-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="dbf10-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbf10-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
