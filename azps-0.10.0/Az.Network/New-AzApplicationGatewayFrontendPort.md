---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: ddfe8b1736ef6c037522815dc81019fadc5b6c1f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875470"
---
# <span data-ttu-id="5d640-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d640-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5d640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d640-102">SYNOPSIS</span></span>
<span data-ttu-id="5d640-103">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="5d640-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d640-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d640-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d640-105">DESCRIPTION</span></span>
<span data-ttu-id="5d640-106">**AzApplicationGatewayFrontendPort** Cmdlet은 Azure application gateway에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="5d640-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5d640-107">EXAMPLES</span></span>

### <span data-ttu-id="5d640-108">Example1: 프런트 엔드 포트 만들기</span><span class="sxs-lookup"><span data-stu-id="5d640-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5d640-109">이 명령은 FrontEndPort01 이라는 프런트 엔드 포트를 포트 80에 만들고 그 결과를 $FrontEndPort 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="5d640-110">변수</span><span class="sxs-lookup"><span data-stu-id="5d640-110">PARAMETERS</span></span>

### <span data-ttu-id="5d640-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d640-111">-DefaultProfile</span></span>
<span data-ttu-id="5d640-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d640-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5d640-113">-Name</span></span>
<span data-ttu-id="5d640-114">이 cmdlet이 만드는 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d640-115">-포트</span><span class="sxs-lookup"><span data-stu-id="5d640-115">-Port</span></span>
<span data-ttu-id="5d640-116">프런트 엔드 포트의 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d640-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d640-117">CommonParameters</span></span>
<span data-ttu-id="5d640-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d640-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d640-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d640-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d640-120">입력</span><span class="sxs-lookup"><span data-stu-id="5d640-120">INPUTS</span></span>

### <span data-ttu-id="5d640-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d640-121">System.String</span></span>

## <span data-ttu-id="5d640-122">출력</span><span class="sxs-lookup"><span data-stu-id="5d640-122">OUTPUTS</span></span>

### <span data-ttu-id="5d640-123">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5d640-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5d640-124">상속자</span><span class="sxs-lookup"><span data-stu-id="5d640-124">NOTES</span></span>

## <span data-ttu-id="5d640-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d640-125">RELATED LINKS</span></span>

[<span data-ttu-id="5d640-126">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d640-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5d640-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d640-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5d640-128">제거-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d640-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5d640-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d640-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


