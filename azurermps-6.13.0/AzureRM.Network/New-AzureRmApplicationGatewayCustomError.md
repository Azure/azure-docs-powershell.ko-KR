---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534243"
---
# <span data-ttu-id="0e7a1-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0e7a1-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0e7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7a1-103">Http 상태 코드와 사용자 지정 오류 페이지 url을 사용 하 여 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e7a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e7a1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e7a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e7a1-105">DESCRIPTION</span></span>
<span data-ttu-id="0e7a1-106">**AzureRmApplicationGatewayCustomError** cmdlet은 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="0e7a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e7a1-107">EXAMPLES</span></span>

### <span data-ttu-id="0e7a1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e7a1-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="0e7a1-109">이 명령은 http 상태 코드 403의 사용자 지정 오류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="0e7a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="0e7a1-110">PARAMETERS</span></span>

### <span data-ttu-id="0e7a1-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="0e7a1-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="0e7a1-112">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0e7a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7a1-113">-DefaultProfile</span></span>
<span data-ttu-id="0e7a1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7a1-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0e7a1-115">-StatusCode</span></span>
<span data-ttu-id="0e7a1-116">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0e7a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7a1-117">CommonParameters</span></span>
<span data-ttu-id="0e7a1-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e7a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0e7a1-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e7a1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7a1-120">입력</span><span class="sxs-lookup"><span data-stu-id="0e7a1-120">INPUTS</span></span>

### <span data-ttu-id="0e7a1-121">않아야</span><span class="sxs-lookup"><span data-stu-id="0e7a1-121">None</span></span>

## <span data-ttu-id="0e7a1-122">출력</span><span class="sxs-lookup"><span data-stu-id="0e7a1-122">OUTPUTS</span></span>

### <span data-ttu-id="0e7a1-123">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0e7a1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0e7a1-124">상속자</span><span class="sxs-lookup"><span data-stu-id="0e7a1-124">NOTES</span></span>

## <span data-ttu-id="0e7a1-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e7a1-125">RELATED LINKS</span></span>
