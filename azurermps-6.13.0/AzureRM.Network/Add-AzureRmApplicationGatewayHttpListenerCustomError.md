---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711073"
---
# <span data-ttu-id="49aea-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="49aea-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="49aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49aea-102">SYNOPSIS</span></span>
<span data-ttu-id="49aea-103">사용자 지정 오류를 응용 프로그램 게이트웨이의 http 수신기에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49aea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49aea-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49aea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49aea-105">DESCRIPTION</span></span>
<span data-ttu-id="49aea-106">**Add-AzureRmApplicationGatewayCustomError** cmdlet은 사용자 지정 오류를 응용 프로그램 게이트웨이의 http 수신기에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="49aea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="49aea-107">EXAMPLES</span></span>

### <span data-ttu-id="49aea-108">예제 1: http 수신기 수준에 사용자 지정 오류 추가</span><span class="sxs-lookup"><span data-stu-id="49aea-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="49aea-109">이 명령은 http 상태 코드 502의 사용자 지정 오류를 http 수신기 $listener 01에 추가 하 고 업데이트 된 수신기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="49aea-110">변수</span><span class="sxs-lookup"><span data-stu-id="49aea-110">PARAMETERS</span></span>

### <span data-ttu-id="49aea-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="49aea-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="49aea-112">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="49aea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49aea-113">-DefaultProfile</span></span>
<span data-ttu-id="49aea-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49aea-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="49aea-115">-HttpListener</span></span>
<span data-ttu-id="49aea-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="49aea-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49aea-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="49aea-117">-StatusCode</span></span>
<span data-ttu-id="49aea-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="49aea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49aea-119">CommonParameters</span></span>
<span data-ttu-id="49aea-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49aea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49aea-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49aea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49aea-122">입력</span><span class="sxs-lookup"><span data-stu-id="49aea-122">INPUTS</span></span>

### <span data-ttu-id="49aea-123">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="49aea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="49aea-124">출력</span><span class="sxs-lookup"><span data-stu-id="49aea-124">OUTPUTS</span></span>

### <span data-ttu-id="49aea-125">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="49aea-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="49aea-126">상속자</span><span class="sxs-lookup"><span data-stu-id="49aea-126">NOTES</span></span>

## <span data-ttu-id="49aea-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49aea-127">RELATED LINKS</span></span>
