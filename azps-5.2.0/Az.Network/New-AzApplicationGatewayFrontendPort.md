---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340814"
---
# <span data-ttu-id="ca446-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca446-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ca446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca446-102">SYNOPSIS</span></span>
<span data-ttu-id="ca446-103">애플리케이션 게이트웨이에 대한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca446-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="ca446-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca446-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca446-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca446-105">DESCRIPTION</span></span>
<span data-ttu-id="ca446-106">**New-AzApplicationGatewayFrontendPort** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca446-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="ca446-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca446-107">EXAMPLES</span></span>

### <span data-ttu-id="ca446-108">예제 1: Example1: 프런트 엔드 포트 만들기</span><span class="sxs-lookup"><span data-stu-id="ca446-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="ca446-109">이 명령은 포트 80에 FrontEndPort01이라는 프런트 엔드 포트를 만들고, 그 결과를 $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="ca446-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="ca446-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca446-110">PARAMETERS</span></span>

### <span data-ttu-id="ca446-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca446-111">-DefaultProfile</span></span>
<span data-ttu-id="ca446-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca446-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca446-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ca446-113">-Name</span></span>
<span data-ttu-id="ca446-114">이 cmdlet에서 만드는 프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca446-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ca446-115">-Port</span><span class="sxs-lookup"><span data-stu-id="ca446-115">-Port</span></span>
<span data-ttu-id="ca446-116">프런트 엔드 포트의 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca446-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca446-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca446-117">CommonParameters</span></span>
<span data-ttu-id="ca446-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca446-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca446-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca446-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca446-120">입력</span><span class="sxs-lookup"><span data-stu-id="ca446-120">INPUTS</span></span>

### <span data-ttu-id="ca446-121">없음</span><span class="sxs-lookup"><span data-stu-id="ca446-121">None</span></span>

## <span data-ttu-id="ca446-122">출력</span><span class="sxs-lookup"><span data-stu-id="ca446-122">OUTPUTS</span></span>

### <span data-ttu-id="ca446-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca446-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ca446-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca446-124">NOTES</span></span>

## <span data-ttu-id="ca446-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca446-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca446-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca446-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ca446-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca446-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ca446-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca446-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ca446-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca446-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


