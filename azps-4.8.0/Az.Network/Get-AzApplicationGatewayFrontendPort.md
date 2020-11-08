---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056211"
---
# <span data-ttu-id="c2ddb-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2ddb-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c2ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ddb-103">응용 프로그램 게이트웨이의 프런트 엔드 포트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="c2ddb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2ddb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2ddb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ddb-106">**Get-AzApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이의 프런트 엔드 포트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="c2ddb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c2ddb-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ddb-108">예제 1: 지정 된 프런트 엔드 포트 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2ddb-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c2ddb-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c2ddb-110">두 번째 명령은 $AppGw에서 FrontEndPort01 이라는 프런트 엔드 포트를 가져와 $FrontEndPort 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="c2ddb-111">예제 2: 프런트 엔드 포트 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2ddb-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="c2ddb-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c2ddb-113">두 번째 명령은 $AppGw에서 프런트 엔드 포트 목록을 가져와 $FrontEndPorts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="c2ddb-114">변수</span><span class="sxs-lookup"><span data-stu-id="c2ddb-114">PARAMETERS</span></span>

### <span data-ttu-id="c2ddb-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2ddb-115">-ApplicationGateway</span></span>
<span data-ttu-id="c2ddb-116">프런트 엔드 포트를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="c2ddb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ddb-117">-DefaultProfile</span></span>
<span data-ttu-id="c2ddb-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2ddb-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c2ddb-119">-Name</span></span>
<span data-ttu-id="c2ddb-120">가져올 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="c2ddb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ddb-121">CommonParameters</span></span>
<span data-ttu-id="c2ddb-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ddb-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ddb-124">입력</span><span class="sxs-lookup"><span data-stu-id="c2ddb-124">INPUTS</span></span>

### <span data-ttu-id="c2ddb-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2ddb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2ddb-126">출력</span><span class="sxs-lookup"><span data-stu-id="c2ddb-126">OUTPUTS</span></span>

### <span data-ttu-id="c2ddb-127">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c2ddb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c2ddb-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c2ddb-128">NOTES</span></span>

## <span data-ttu-id="c2ddb-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2ddb-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2ddb-130">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2ddb-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c2ddb-131">새로운 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2ddb-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c2ddb-132">제거-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2ddb-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c2ddb-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2ddb-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


