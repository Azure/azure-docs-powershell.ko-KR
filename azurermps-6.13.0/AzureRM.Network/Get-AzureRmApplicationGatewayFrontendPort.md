---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 388c2d06f7ff62bfe5fc2f6fcf47d5fa9fa16877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537588"
---
# <span data-ttu-id="c5f8f-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c5f8f-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c5f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f8f-103">응용 프로그램 게이트웨이의 프런트 엔드 포트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5f8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5f8f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5f8f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f8f-106">**Get-AzureRmApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이의 프런트 엔드 포트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="c5f8f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c5f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f8f-108">예제 1: 지정 된 프런트 엔드 포트 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5f8f-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c5f8f-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c5f8f-110">두 번째 명령은 $AppGw에서 FrontEndPort01 이라는 프런트 엔드 포트를 가져와 $FrontEndPort 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="c5f8f-111">예제 2: 프런트 엔드 포트 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5f8f-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="c5f8f-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c5f8f-113">두 번째 명령은 $AppGw에서 프런트 엔드 포트 목록을 가져와 $FrontEndPorts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="c5f8f-114">변수</span><span class="sxs-lookup"><span data-stu-id="c5f8f-114">PARAMETERS</span></span>

### <span data-ttu-id="c5f8f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5f8f-115">-ApplicationGateway</span></span>
<span data-ttu-id="c5f8f-116">프런트 엔드 포트를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="c5f8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f8f-117">-DefaultProfile</span></span>
<span data-ttu-id="c5f8f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5f8f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c5f8f-119">-Name</span></span>
<span data-ttu-id="c5f8f-120">가져올 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="c5f8f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f8f-121">CommonParameters</span></span>
<span data-ttu-id="c5f8f-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f8f-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f8f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f8f-124">입력</span><span class="sxs-lookup"><span data-stu-id="c5f8f-124">INPUTS</span></span>

### <span data-ttu-id="c5f8f-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5f8f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="c5f8f-126">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5f8f-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="c5f8f-127">출력</span><span class="sxs-lookup"><span data-stu-id="c5f8f-127">OUTPUTS</span></span>

### <span data-ttu-id="c5f8f-128">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c5f8f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c5f8f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c5f8f-129">NOTES</span></span>

## <span data-ttu-id="c5f8f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5f8f-130">RELATED LINKS</span></span>

[<span data-ttu-id="c5f8f-131">추가-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c5f8f-131">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c5f8f-132">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c5f8f-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c5f8f-133">제거-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c5f8f-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c5f8f-134">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c5f8f-134">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


