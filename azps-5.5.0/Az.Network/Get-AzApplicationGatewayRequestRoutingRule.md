---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184756"
---
# <span data-ttu-id="532ec-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="532ec-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="532ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="532ec-102">SYNOPSIS</span></span>
<span data-ttu-id="532ec-103">애플리케이션 게이트웨이의 요청 라우팅 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="532ec-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="532ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="532ec-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="532ec-105">설명</span><span class="sxs-lookup"><span data-stu-id="532ec-105">DESCRIPTION</span></span>
<span data-ttu-id="532ec-106">**Get-AzApplicationGatewayRequestRoutingRule** cmdlet은 애플리케이션 게이트웨이의 요청 라우팅 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="532ec-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="532ec-107">예제</span><span class="sxs-lookup"><span data-stu-id="532ec-107">EXAMPLES</span></span>

### <span data-ttu-id="532ec-108">예제 1: 특정 요청 라우팅 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="532ec-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="532ec-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 사용하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="532ec-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="532ec-110">두 번째 명령은 규칙이라는 변수에 저장된 Application Gateway에서 Rule01이라는 요청 라우팅 규칙을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="532ec-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="532ec-111">예제 2: 요청 라우팅 규칙 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="532ec-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="532ec-112">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 해당 애플리케이션이라는 변수에 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="532ec-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="532ec-113">두 번째 명령은 애플리케이션 게이트웨이의 요청 라우팅 규칙 목록을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="532ec-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="532ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="532ec-114">PARAMETERS</span></span>

### <span data-ttu-id="532ec-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="532ec-115">-ApplicationGateway</span></span>
<span data-ttu-id="532ec-116">요청 라우팅 규칙을 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="532ec-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="532ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532ec-117">-DefaultProfile</span></span>
<span data-ttu-id="532ec-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="532ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="532ec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="532ec-119">-Name</span></span>
<span data-ttu-id="532ec-120">이 cmdlet이 얻을 요청 라우팅 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="532ec-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="532ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532ec-121">CommonParameters</span></span>
<span data-ttu-id="532ec-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="532ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532ec-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="532ec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532ec-124">입력</span><span class="sxs-lookup"><span data-stu-id="532ec-124">INPUTS</span></span>

### <span data-ttu-id="532ec-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="532ec-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="532ec-126">출력</span><span class="sxs-lookup"><span data-stu-id="532ec-126">OUTPUTS</span></span>

### <span data-ttu-id="532ec-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="532ec-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="532ec-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="532ec-128">NOTES</span></span>

## <span data-ttu-id="532ec-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="532ec-129">RELATED LINKS</span></span>

[<span data-ttu-id="532ec-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="532ec-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="532ec-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="532ec-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="532ec-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="532ec-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="532ec-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="532ec-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


