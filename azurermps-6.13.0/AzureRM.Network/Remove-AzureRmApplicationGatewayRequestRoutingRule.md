---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: a4c1710ebbdfad1afb428bb09cccf27865c5e56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529493"
---
# <span data-ttu-id="d4274-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4274-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d4274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4274-102">SYNOPSIS</span></span>
<span data-ttu-id="d4274-103">응용 프로그램 게이트웨이에서 요청 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4274-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4274-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4274-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d4274-105">DESCRIPTION</span></span>
<span data-ttu-id="d4274-106">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet은 Azure application gateway에서 요청 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="d4274-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d4274-107">EXAMPLES</span></span>

### <span data-ttu-id="d4274-108">예제 1: 응용 프로그램 게이트웨이에서 요청 라우팅 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="d4274-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="d4274-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d4274-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Rule02 라는 요청 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d4274-111">변수</span><span class="sxs-lookup"><span data-stu-id="d4274-111">PARAMETERS</span></span>

### <span data-ttu-id="d4274-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4274-112">-ApplicationGateway</span></span>
<span data-ttu-id="d4274-113">요청 라우팅 규칙을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="d4274-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4274-114">-DefaultProfile</span></span>
<span data-ttu-id="d4274-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4274-116">-이름</span><span class="sxs-lookup"><span data-stu-id="d4274-116">-Name</span></span>
<span data-ttu-id="d4274-117">이 cmdlet이 제거할 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="d4274-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4274-118">CommonParameters</span></span>
<span data-ttu-id="d4274-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4274-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4274-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4274-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4274-121">입력</span><span class="sxs-lookup"><span data-stu-id="d4274-121">INPUTS</span></span>

### <span data-ttu-id="d4274-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4274-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d4274-123">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4274-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d4274-124">출력</span><span class="sxs-lookup"><span data-stu-id="d4274-124">OUTPUTS</span></span>

### <span data-ttu-id="d4274-125">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d4274-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d4274-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d4274-126">NOTES</span></span>

## <span data-ttu-id="d4274-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4274-127">RELATED LINKS</span></span>

[<span data-ttu-id="d4274-128">추가-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4274-128">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d4274-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4274-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d4274-130">새로운 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4274-130">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d4274-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4274-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


