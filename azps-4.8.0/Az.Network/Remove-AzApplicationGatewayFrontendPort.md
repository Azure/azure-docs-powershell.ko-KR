---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056171"
---
# <span data-ttu-id="4a8be-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a8be-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4a8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a8be-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8be-103">응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="4a8be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a8be-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a8be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4a8be-105">DESCRIPTION</span></span>
<span data-ttu-id="4a8be-106">**AzApplicationGatewayFrontendPort** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="4a8be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4a8be-107">EXAMPLES</span></span>

### <span data-ttu-id="4a8be-108">예: 응용 프로그램 게이트웨이에서 프런트 엔드 포트 제거</span><span class="sxs-lookup"><span data-stu-id="4a8be-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="4a8be-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고 게이트웨이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="4a8be-110">두 번째 명령은 응용 프로그램 게이트웨이에서 FrontEndPort02 이라는 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="4a8be-111">변수</span><span class="sxs-lookup"><span data-stu-id="4a8be-111">PARAMETERS</span></span>

### <span data-ttu-id="4a8be-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a8be-112">-ApplicationGateway</span></span>
<span data-ttu-id="4a8be-113">프런트 엔드 포트를 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="4a8be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8be-114">-DefaultProfile</span></span>
<span data-ttu-id="4a8be-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a8be-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4a8be-116">-Name</span></span>
<span data-ttu-id="4a8be-117">제거할 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="4a8be-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8be-118">CommonParameters</span></span>
<span data-ttu-id="4a8be-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a8be-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8be-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a8be-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8be-121">입력</span><span class="sxs-lookup"><span data-stu-id="4a8be-121">INPUTS</span></span>

### <span data-ttu-id="4a8be-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a8be-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a8be-123">출력</span><span class="sxs-lookup"><span data-stu-id="4a8be-123">OUTPUTS</span></span>

### <span data-ttu-id="4a8be-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a8be-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a8be-125">상속자</span><span class="sxs-lookup"><span data-stu-id="4a8be-125">NOTES</span></span>

## <span data-ttu-id="4a8be-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a8be-126">RELATED LINKS</span></span>

[<span data-ttu-id="4a8be-127">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a8be-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4a8be-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a8be-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4a8be-129">새로운 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a8be-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4a8be-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4a8be-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


