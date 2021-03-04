---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953947"
---
# <span data-ttu-id="e364f-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e364f-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e364f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e364f-102">SYNOPSIS</span></span>
<span data-ttu-id="e364f-103">애플리케이션 게이트웨이에 대한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e364f-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="e364f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e364f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e364f-105">설명</span><span class="sxs-lookup"><span data-stu-id="e364f-105">DESCRIPTION</span></span>
<span data-ttu-id="e364f-106">**New-AzApplicationGatewayFrontendPort** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e364f-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="e364f-107">예제</span><span class="sxs-lookup"><span data-stu-id="e364f-107">EXAMPLES</span></span>

### <span data-ttu-id="e364f-108">예제 1: 예제1: 프런트 엔드 포트 만들기</span><span class="sxs-lookup"><span data-stu-id="e364f-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="e364f-109">이 명령은 포트 80에서 FrontEndPort01이라는 프런트 엔드 포트를 만들고 결과를 $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="e364f-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="e364f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e364f-110">PARAMETERS</span></span>

### <span data-ttu-id="e364f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e364f-111">-DefaultProfile</span></span>
<span data-ttu-id="e364f-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e364f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e364f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e364f-113">-Name</span></span>
<span data-ttu-id="e364f-114">이 cmdlet이 만드는 프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e364f-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e364f-115">-Port</span><span class="sxs-lookup"><span data-stu-id="e364f-115">-Port</span></span>
<span data-ttu-id="e364f-116">프런트 엔드 포트의 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e364f-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="e364f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e364f-117">CommonParameters</span></span>
<span data-ttu-id="e364f-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e364f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e364f-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e364f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e364f-120">입력</span><span class="sxs-lookup"><span data-stu-id="e364f-120">INPUTS</span></span>

### <span data-ttu-id="e364f-121">없음</span><span class="sxs-lookup"><span data-stu-id="e364f-121">None</span></span>

## <span data-ttu-id="e364f-122">출력</span><span class="sxs-lookup"><span data-stu-id="e364f-122">OUTPUTS</span></span>

### <span data-ttu-id="e364f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e364f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e364f-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e364f-124">NOTES</span></span>

## <span data-ttu-id="e364f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e364f-125">RELATED LINKS</span></span>

[<span data-ttu-id="e364f-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e364f-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e364f-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e364f-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e364f-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e364f-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e364f-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e364f-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


