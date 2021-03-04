---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 4d2f3f225e185678dd1e3b0047810a5e68d4273f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952000"
---
# <span data-ttu-id="84ce3-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84ce3-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="84ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="84ce3-103">애플리케이션 게이트웨이를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="84ce3-103">Starts an application gateway.</span></span>

## <span data-ttu-id="84ce3-104">구문</span><span class="sxs-lookup"><span data-stu-id="84ce3-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84ce3-105">설명</span><span class="sxs-lookup"><span data-stu-id="84ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="84ce3-106">**Start-AzApplicationGateway** cmdlet은 Azure 애플리케이션 게이트웨이를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="84ce3-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="84ce3-107">예제</span><span class="sxs-lookup"><span data-stu-id="84ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="84ce3-108">예제1: 애플리케이션 게이트웨이 시작</span><span class="sxs-lookup"><span data-stu-id="84ce3-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="84ce3-109">이 명령은 애플리케이션 게이트웨이가 $AppGw 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="84ce3-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="84ce3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="84ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="84ce3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84ce3-111">-ApplicationGateway</span></span>
<span data-ttu-id="84ce3-112">이 cmdlet이 시작하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="84ce3-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="84ce3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ce3-113">-DefaultProfile</span></span>
<span data-ttu-id="84ce3-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84ce3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84ce3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ce3-115">CommonParameters</span></span>
<span data-ttu-id="84ce3-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84ce3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ce3-117">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="84ce3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ce3-118">입력</span><span class="sxs-lookup"><span data-stu-id="84ce3-118">INPUTS</span></span>

### <span data-ttu-id="84ce3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84ce3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84ce3-120">출력</span><span class="sxs-lookup"><span data-stu-id="84ce3-120">OUTPUTS</span></span>

### <span data-ttu-id="84ce3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84ce3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84ce3-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84ce3-122">NOTES</span></span>

## <span data-ttu-id="84ce3-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84ce3-123">RELATED LINKS</span></span>

[<span data-ttu-id="84ce3-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84ce3-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


