---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 7a6d8bef710ddf41f805c6ced558e12781a23276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533380"
---
# <span data-ttu-id="90175-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90175-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90175-102">SYNOPSIS</span></span>
<span data-ttu-id="90175-103">응용 프로그램 게이트웨이의 요청 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90175-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90175-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90175-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90175-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90175-105">DESCRIPTION</span></span>
<span data-ttu-id="90175-106">**Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet은 응용 프로그램 게이트웨이의 요청 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90175-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="90175-107">예제의</span><span class="sxs-lookup"><span data-stu-id="90175-107">EXAMPLES</span></span>

### <span data-ttu-id="90175-108">예제 1: 특정 요청 라우팅 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="90175-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="90175-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90175-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="90175-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 Rule01 라는 요청 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90175-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="90175-111">예제 2: 요청 라우팅 규칙 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="90175-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="90175-112">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90175-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="90175-113">두 번째 명령은 $AppGW 라는 변수에 저장 된 응용 프로그램 게이트웨이에서 요청 라우팅 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90175-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="90175-114">변수</span><span class="sxs-lookup"><span data-stu-id="90175-114">PARAMETERS</span></span>

### <span data-ttu-id="90175-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90175-115">-ApplicationGateway</span></span>
<span data-ttu-id="90175-116">요청 라우팅 규칙을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90175-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="90175-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90175-117">-DefaultProfile</span></span>
<span data-ttu-id="90175-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90175-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90175-119">-이름</span><span class="sxs-lookup"><span data-stu-id="90175-119">-Name</span></span>
<span data-ttu-id="90175-120">이 cmdlet이 가져오는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90175-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90175-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90175-121">CommonParameters</span></span>
<span data-ttu-id="90175-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90175-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90175-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90175-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90175-124">입력</span><span class="sxs-lookup"><span data-stu-id="90175-124">INPUTS</span></span>

### <span data-ttu-id="90175-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90175-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="90175-126">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90175-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="90175-127">출력</span><span class="sxs-lookup"><span data-stu-id="90175-127">OUTPUTS</span></span>

### <span data-ttu-id="90175-128">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="90175-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90175-129">상속자</span><span class="sxs-lookup"><span data-stu-id="90175-129">NOTES</span></span>

## <span data-ttu-id="90175-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90175-130">RELATED LINKS</span></span>

[<span data-ttu-id="90175-131">추가-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90175-131">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90175-132">새로운 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90175-132">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90175-133">제거-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90175-133">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90175-134">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90175-134">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


