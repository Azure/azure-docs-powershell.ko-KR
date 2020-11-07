---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 402084acc332102c8a2f003e31e140b175b6f22f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875623"
---
# <span data-ttu-id="8a43c-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8a43c-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8a43c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a43c-102">SYNOPSIS</span></span>
<span data-ttu-id="8a43c-103">응용 프로그램 게이트웨이의 요청 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="8a43c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a43c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a43c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a43c-105">DESCRIPTION</span></span>
<span data-ttu-id="8a43c-106">**Get-AzApplicationGatewayRequestRoutingRule** cmdlet은 응용 프로그램 게이트웨이의 요청 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="8a43c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a43c-107">EXAMPLES</span></span>

### <span data-ttu-id="8a43c-108">예제 1: 특정 요청 라우팅 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a43c-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="8a43c-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8a43c-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 Rule01 라는 요청 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="8a43c-111">예제 2: 요청 라우팅 규칙 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a43c-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="8a43c-112">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8a43c-113">두 번째 명령은 $AppGW 라는 변수에 저장 된 응용 프로그램 게이트웨이에서 요청 라우팅 규칙 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="8a43c-114">변수</span><span class="sxs-lookup"><span data-stu-id="8a43c-114">PARAMETERS</span></span>

### <span data-ttu-id="8a43c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a43c-115">-ApplicationGateway</span></span>
<span data-ttu-id="8a43c-116">요청 라우팅 규칙을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-116">Specifies the application gateway object that contains request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a43c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a43c-117">-DefaultProfile</span></span>
<span data-ttu-id="8a43c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a43c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8a43c-119">-Name</span></span>
<span data-ttu-id="8a43c-120">이 cmdlet이 가져오는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a43c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a43c-121">CommonParameters</span></span>
<span data-ttu-id="8a43c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a43c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a43c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a43c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a43c-124">입력</span><span class="sxs-lookup"><span data-stu-id="8a43c-124">INPUTS</span></span>

### <span data-ttu-id="8a43c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a43c-125">System.String</span></span>

## <span data-ttu-id="8a43c-126">출력</span><span class="sxs-lookup"><span data-stu-id="8a43c-126">OUTPUTS</span></span>

### <span data-ttu-id="8a43c-127">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8a43c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8a43c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8a43c-128">NOTES</span></span>

## <span data-ttu-id="8a43c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a43c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8a43c-130">추가-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8a43c-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8a43c-131">새로운 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8a43c-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8a43c-132">제거-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8a43c-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8a43c-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8a43c-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


