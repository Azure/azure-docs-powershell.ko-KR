---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496723"
---
# <span data-ttu-id="d1f07-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1f07-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d1f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f07-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f07-103">애플리케이션 게이트웨이의 프런트 엔드 포트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="d1f07-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1f07-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1f07-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1f07-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f07-106">**Get-AzApplicationGatewayFrontendPort** cmdlet은 애플리케이션 게이트웨이의 프런트 엔드 포트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="d1f07-107">예제</span><span class="sxs-lookup"><span data-stu-id="d1f07-107">EXAMPLES</span></span>

### <span data-ttu-id="d1f07-108">예제 1: 지정된 프런트 엔드 포트를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d1f07-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1f07-110">두 번째 명령은 FrontEndPort01이라는 프런트 엔드 포트를 $AppGw 변수에 $FrontEndPort 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="d1f07-111">예제 2: 프런트 엔드 포트 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="d1f07-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="d1f07-112">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1f07-113">두 번째 명령은 프런트 엔드 포트의 목록을 $AppGw 변수에 $FrontEndPorts 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="d1f07-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f07-114">PARAMETERS</span></span>

### <span data-ttu-id="d1f07-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1f07-115">-ApplicationGateway</span></span>
<span data-ttu-id="d1f07-116">프런트 엔드 포트를 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="d1f07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f07-117">-DefaultProfile</span></span>
<span data-ttu-id="d1f07-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1f07-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f07-119">-Name</span></span>
<span data-ttu-id="d1f07-120">얻을 프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="d1f07-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f07-121">CommonParameters</span></span>
<span data-ttu-id="d1f07-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f07-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f07-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1f07-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f07-124">입력</span><span class="sxs-lookup"><span data-stu-id="d1f07-124">INPUTS</span></span>

### <span data-ttu-id="d1f07-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1f07-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1f07-126">출력</span><span class="sxs-lookup"><span data-stu-id="d1f07-126">OUTPUTS</span></span>

### <span data-ttu-id="d1f07-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1f07-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d1f07-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1f07-128">NOTES</span></span>

## <span data-ttu-id="d1f07-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1f07-129">RELATED LINKS</span></span>

[<span data-ttu-id="d1f07-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1f07-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d1f07-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1f07-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d1f07-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1f07-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d1f07-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1f07-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


