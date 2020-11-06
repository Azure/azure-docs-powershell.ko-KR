---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527840"
---
# <span data-ttu-id="974a0-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="974a0-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="974a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="974a0-102">SYNOPSIS</span></span>
<span data-ttu-id="974a0-103">응용 프로그램 게이트웨이에서 사용자 지정 오류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="974a0-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="974a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="974a0-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="974a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="974a0-105">DESCRIPTION</span></span>
<span data-ttu-id="974a0-106">**AzureRmApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이에서 사용자 지정 오류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="974a0-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="974a0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="974a0-107">EXAMPLES</span></span>

### <span data-ttu-id="974a0-108">예제 1: 응용 프로그램 게이트웨이에서 사용자 지정 오류 제거</span><span class="sxs-lookup"><span data-stu-id="974a0-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="974a0-109">이 명령은 응용 프로그램 게이트웨이에서 $appgw http 상태 코드 502의 사용자 지정 오류를 제거 하 고 업데이트 된 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="974a0-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="974a0-110">변수</span><span class="sxs-lookup"><span data-stu-id="974a0-110">PARAMETERS</span></span>

### <span data-ttu-id="974a0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="974a0-111">-ApplicationGateway</span></span>
<span data-ttu-id="974a0-112">응용 프로그램 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="974a0-112">The Application Gateway</span></span>

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

### <span data-ttu-id="974a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974a0-113">-DefaultProfile</span></span>
<span data-ttu-id="974a0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="974a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974a0-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="974a0-115">-StatusCode</span></span>
<span data-ttu-id="974a0-116">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="974a0-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="974a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974a0-117">CommonParameters</span></span>
<span data-ttu-id="974a0-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="974a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974a0-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="974a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974a0-120">입력</span><span class="sxs-lookup"><span data-stu-id="974a0-120">INPUTS</span></span>

### <span data-ttu-id="974a0-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="974a0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="974a0-122">출력</span><span class="sxs-lookup"><span data-stu-id="974a0-122">OUTPUTS</span></span>

### <span data-ttu-id="974a0-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="974a0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="974a0-124">상속자</span><span class="sxs-lookup"><span data-stu-id="974a0-124">NOTES</span></span>

## <span data-ttu-id="974a0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="974a0-125">RELATED LINKS</span></span>
