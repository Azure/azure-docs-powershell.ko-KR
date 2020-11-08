---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213027"
---
# <span data-ttu-id="5f9d9-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5f9d9-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5f9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9d9-103">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="5f9d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f9d9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f9d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="5f9d9-106">**AzApplicationGatewayFrontendPort** Cmdlet은 Azure application gateway에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="5f9d9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5f9d9-107">EXAMPLES</span></span>

### <span data-ttu-id="5f9d9-108">예제 1: Example1: 프런트 엔드 포트 만들기</span><span class="sxs-lookup"><span data-stu-id="5f9d9-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5f9d9-109">이 명령은 FrontEndPort01 이라는 프런트 엔드 포트를 포트 80에 만들고 그 결과를 $FrontEndPort 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="5f9d9-110">변수</span><span class="sxs-lookup"><span data-stu-id="5f9d9-110">PARAMETERS</span></span>

### <span data-ttu-id="5f9d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9d9-111">-DefaultProfile</span></span>
<span data-ttu-id="5f9d9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f9d9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5f9d9-113">-Name</span></span>
<span data-ttu-id="5f9d9-114">이 cmdlet이 만드는 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5f9d9-115">-포트</span><span class="sxs-lookup"><span data-stu-id="5f9d9-115">-Port</span></span>
<span data-ttu-id="5f9d9-116">프런트 엔드 포트의 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="5f9d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9d9-117">CommonParameters</span></span>
<span data-ttu-id="5f9d9-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9d9-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f9d9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9d9-120">입력</span><span class="sxs-lookup"><span data-stu-id="5f9d9-120">INPUTS</span></span>

### <span data-ttu-id="5f9d9-121">않아야</span><span class="sxs-lookup"><span data-stu-id="5f9d9-121">None</span></span>

## <span data-ttu-id="5f9d9-122">출력</span><span class="sxs-lookup"><span data-stu-id="5f9d9-122">OUTPUTS</span></span>

### <span data-ttu-id="5f9d9-123">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5f9d9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5f9d9-124">상속자</span><span class="sxs-lookup"><span data-stu-id="5f9d9-124">NOTES</span></span>

## <span data-ttu-id="5f9d9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f9d9-125">RELATED LINKS</span></span>

[<span data-ttu-id="5f9d9-126">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5f9d9-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5f9d9-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5f9d9-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5f9d9-128">제거-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5f9d9-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5f9d9-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5f9d9-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


