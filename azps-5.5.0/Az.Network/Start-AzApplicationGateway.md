---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184137"
---
# <span data-ttu-id="7a316-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a316-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="7a316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a316-102">SYNOPSIS</span></span>
<span data-ttu-id="7a316-103">애플리케이션 게이트웨이를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7a316-103">Starts an application gateway.</span></span>

## <span data-ttu-id="7a316-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a316-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a316-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a316-105">DESCRIPTION</span></span>
<span data-ttu-id="7a316-106">**Start-AzApplicationGateway** cmdlet이 Azure 애플리케이션 게이트웨이를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7a316-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="7a316-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a316-107">EXAMPLES</span></span>

### <span data-ttu-id="7a316-108">예제1: 애플리케이션 게이트웨이 시작</span><span class="sxs-lookup"><span data-stu-id="7a316-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="7a316-109">이 명령은 $AppGw 변수에 저장된 애플리케이션 게이트웨이를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7a316-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="7a316-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a316-110">PARAMETERS</span></span>

### <span data-ttu-id="7a316-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a316-111">-ApplicationGateway</span></span>
<span data-ttu-id="7a316-112">이 cmdlet이 시작되는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a316-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="7a316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a316-113">-DefaultProfile</span></span>
<span data-ttu-id="7a316-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a316-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a316-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a316-115">CommonParameters</span></span>
<span data-ttu-id="7a316-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a316-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a316-117">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a316-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a316-118">입력</span><span class="sxs-lookup"><span data-stu-id="7a316-118">INPUTS</span></span>

### <span data-ttu-id="7a316-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a316-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a316-120">출력</span><span class="sxs-lookup"><span data-stu-id="7a316-120">OUTPUTS</span></span>

### <span data-ttu-id="7a316-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a316-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a316-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a316-122">NOTES</span></span>

## <span data-ttu-id="7a316-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a316-123">RELATED LINKS</span></span>

[<span data-ttu-id="7a316-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a316-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


