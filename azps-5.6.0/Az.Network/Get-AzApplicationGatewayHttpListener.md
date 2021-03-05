---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996534"
---
# <span data-ttu-id="44693-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="44693-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="44693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44693-102">SYNOPSIS</span></span>
<span data-ttu-id="44693-103">애플리케이션 게이트웨이의 HTTP 수신기 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44693-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="44693-104">구문</span><span class="sxs-lookup"><span data-stu-id="44693-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44693-105">설명</span><span class="sxs-lookup"><span data-stu-id="44693-105">DESCRIPTION</span></span>
<span data-ttu-id="44693-106">**Get-AzApplicationGatewayHttpListener** cmdlet은 애플리케이션 게이트웨이의 HTTP 수신기 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44693-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="44693-107">예제</span><span class="sxs-lookup"><span data-stu-id="44693-107">EXAMPLES</span></span>

### <span data-ttu-id="44693-108">예제 1: 특정 HTTP 수신기 사용</span><span class="sxs-lookup"><span data-stu-id="44693-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="44693-109">이 명령은 Listener01이라는 HTTP 수신기 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44693-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="44693-110">예제 2: HTTP 수신기 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="44693-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="44693-111">이 명령은 HTTP 수신기 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44693-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="44693-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="44693-112">PARAMETERS</span></span>

### <span data-ttu-id="44693-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44693-113">-ApplicationGateway</span></span>
<span data-ttu-id="44693-114">HTTP 수신기를 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="44693-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="44693-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44693-115">-DefaultProfile</span></span>
<span data-ttu-id="44693-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44693-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44693-117">-Name</span><span class="sxs-lookup"><span data-stu-id="44693-117">-Name</span></span>
<span data-ttu-id="44693-118">이 cmdlet이 수신하는 HTTP 수신기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="44693-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="44693-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44693-119">CommonParameters</span></span>
<span data-ttu-id="44693-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44693-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44693-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44693-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44693-122">입력</span><span class="sxs-lookup"><span data-stu-id="44693-122">INPUTS</span></span>

### <span data-ttu-id="44693-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44693-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="44693-124">출력</span><span class="sxs-lookup"><span data-stu-id="44693-124">OUTPUTS</span></span>

### <span data-ttu-id="44693-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="44693-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="44693-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44693-126">NOTES</span></span>

## <span data-ttu-id="44693-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44693-127">RELATED LINKS</span></span>

[<span data-ttu-id="44693-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="44693-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="44693-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="44693-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="44693-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="44693-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="44693-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="44693-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


