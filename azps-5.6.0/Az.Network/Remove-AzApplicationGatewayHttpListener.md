---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 46cf3a786642262c1f6d0df0e2c1fd770d61ec6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959488"
---
# <span data-ttu-id="ed76f-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ed76f-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ed76f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed76f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed76f-103">애플리케이션 게이트웨이에서 HTTP 수신기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="ed76f-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed76f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed76f-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed76f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed76f-106">**Remove-AzApplicationGatewayHttpListener** cmdlet은 Azure 애플리케이션 게이트웨이에서 HTTP 수신기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="ed76f-107">예제</span><span class="sxs-lookup"><span data-stu-id="ed76f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed76f-108">예제 1: 애플리케이션 게이트웨이 HTTP 수신기 제거</span><span class="sxs-lookup"><span data-stu-id="ed76f-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="ed76f-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ed76f-110">두 번째 명령은 에 저장된 애플리케이션 게이트웨이에서 Listener02라는 HTTP 수신기를 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ed76f-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ed76f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed76f-111">PARAMETERS</span></span>

### <span data-ttu-id="ed76f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed76f-112">-ApplicationGateway</span></span>
<span data-ttu-id="ed76f-113">HTTP 수신기를 제거할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="ed76f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed76f-114">-DefaultProfile</span></span>
<span data-ttu-id="ed76f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed76f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ed76f-116">-Name</span></span>
<span data-ttu-id="ed76f-117">이 cmdlet이 제거한 HTTP 수신기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ed76f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed76f-118">CommonParameters</span></span>
<span data-ttu-id="ed76f-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed76f-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed76f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed76f-121">입력</span><span class="sxs-lookup"><span data-stu-id="ed76f-121">INPUTS</span></span>

### <span data-ttu-id="ed76f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed76f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed76f-123">출력</span><span class="sxs-lookup"><span data-stu-id="ed76f-123">OUTPUTS</span></span>

### <span data-ttu-id="ed76f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ed76f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ed76f-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed76f-125">NOTES</span></span>

## <span data-ttu-id="ed76f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed76f-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed76f-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ed76f-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ed76f-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ed76f-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ed76f-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ed76f-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ed76f-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ed76f-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


