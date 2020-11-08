---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033822"
---
# <span data-ttu-id="12255-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="12255-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="12255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12255-102">SYNOPSIS</span></span>
<span data-ttu-id="12255-103">응용 프로그램 게이트웨이에서 HTTP 수신기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="12255-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12255-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12255-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12255-105">DESCRIPTION</span></span>
<span data-ttu-id="12255-106">**AzApplicationGatewayHttpListener** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 HTTP 수신기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="12255-107">예제의</span><span class="sxs-lookup"><span data-stu-id="12255-107">EXAMPLES</span></span>

### <span data-ttu-id="12255-108">예제 1: 응용 프로그램 게이트웨이 HTTP 수신기 제거</span><span class="sxs-lookup"><span data-stu-id="12255-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="12255-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="12255-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Listener02 이라는 HTTP 수신기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="12255-111">변수</span><span class="sxs-lookup"><span data-stu-id="12255-111">PARAMETERS</span></span>

### <span data-ttu-id="12255-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12255-112">-ApplicationGateway</span></span>
<span data-ttu-id="12255-113">HTTP 수신기를 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="12255-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12255-114">-DefaultProfile</span></span>
<span data-ttu-id="12255-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12255-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12255-116">-이름</span><span class="sxs-lookup"><span data-stu-id="12255-116">-Name</span></span>
<span data-ttu-id="12255-117">이 cmdlet이 제거 하는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12255-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12255-118">CommonParameters</span></span>
<span data-ttu-id="12255-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12255-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12255-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12255-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12255-121">입력</span><span class="sxs-lookup"><span data-stu-id="12255-121">INPUTS</span></span>

### <span data-ttu-id="12255-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12255-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12255-123">출력</span><span class="sxs-lookup"><span data-stu-id="12255-123">OUTPUTS</span></span>

### <span data-ttu-id="12255-124">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="12255-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="12255-125">상속자</span><span class="sxs-lookup"><span data-stu-id="12255-125">NOTES</span></span>

## <span data-ttu-id="12255-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12255-126">RELATED LINKS</span></span>

[<span data-ttu-id="12255-127">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="12255-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="12255-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="12255-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="12255-129">새로운 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="12255-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="12255-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="12255-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


