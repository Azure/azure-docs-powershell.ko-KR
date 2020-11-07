---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 3c034f3bbbd5edc77fb6f43c291b8bf7ca27cd38
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875359"
---
# <span data-ttu-id="2a2f5-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a2f5-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2a2f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2f5-103">응용 프로그램 게이트웨이에서 요청 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="2a2f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a2f5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a2f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a2f5-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2f5-106">**AzApplicationGatewayRequestRoutingRule** Cmdlet은 Azure application gateway에서 요청 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="2a2f5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2a2f5-107">EXAMPLES</span></span>

### <span data-ttu-id="2a2f5-108">예제 1: 응용 프로그램 게이트웨이에서 요청 라우팅 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="2a2f5-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="2a2f5-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2a2f5-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Rule02 라는 요청 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2a2f5-111">변수</span><span class="sxs-lookup"><span data-stu-id="2a2f5-111">PARAMETERS</span></span>

### <span data-ttu-id="2a2f5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a2f5-112">-ApplicationGateway</span></span>
<span data-ttu-id="2a2f5-113">요청 라우팅 규칙을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="2a2f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2f5-114">-DefaultProfile</span></span>
<span data-ttu-id="2a2f5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a2f5-116">-이름</span><span class="sxs-lookup"><span data-stu-id="2a2f5-116">-Name</span></span>
<span data-ttu-id="2a2f5-117">이 cmdlet이 제거할 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a2f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2f5-118">CommonParameters</span></span>
<span data-ttu-id="2a2f5-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2f5-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2f5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2f5-121">입력</span><span class="sxs-lookup"><span data-stu-id="2a2f5-121">INPUTS</span></span>

### <span data-ttu-id="2a2f5-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a2f5-122">System.String</span></span>

## <span data-ttu-id="2a2f5-123">출력</span><span class="sxs-lookup"><span data-stu-id="2a2f5-123">OUTPUTS</span></span>

### <span data-ttu-id="2a2f5-124">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2a2f5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2a2f5-125">상속자</span><span class="sxs-lookup"><span data-stu-id="2a2f5-125">NOTES</span></span>

## <span data-ttu-id="2a2f5-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a2f5-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a2f5-127">추가-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a2f5-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a2f5-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a2f5-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a2f5-129">새로운 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a2f5-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2a2f5-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2a2f5-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


