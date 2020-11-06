---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 656067c89adbcead5dd24e08d45147eb7f019e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532448"
---
# <span data-ttu-id="25fd1-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="25fd1-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="25fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="25fd1-103">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25fd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25fd1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25fd1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="25fd1-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet은 Azure application gateway에 대 한 프런트 엔드 포트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="25fd1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="25fd1-107">EXAMPLES</span></span>

### <span data-ttu-id="25fd1-108">Example1: 프런트 엔드 포트 만들기</span><span class="sxs-lookup"><span data-stu-id="25fd1-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="25fd1-109">이 명령은 FrontEndPort01 이라는 프런트 엔드 포트를 포트 80에 만들고 그 결과를 $FrontEndPort 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="25fd1-110">변수</span><span class="sxs-lookup"><span data-stu-id="25fd1-110">PARAMETERS</span></span>

### <span data-ttu-id="25fd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fd1-111">-DefaultProfile</span></span>
<span data-ttu-id="25fd1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25fd1-113">-이름</span><span class="sxs-lookup"><span data-stu-id="25fd1-113">-Name</span></span>
<span data-ttu-id="25fd1-114">이 cmdlet이 만드는 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="25fd1-115">-포트</span><span class="sxs-lookup"><span data-stu-id="25fd1-115">-Port</span></span>
<span data-ttu-id="25fd1-116">프런트 엔드 포트의 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="25fd1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fd1-117">CommonParameters</span></span>
<span data-ttu-id="25fd1-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25fd1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fd1-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fd1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fd1-120">입력</span><span class="sxs-lookup"><span data-stu-id="25fd1-120">INPUTS</span></span>

### <span data-ttu-id="25fd1-121">않아야</span><span class="sxs-lookup"><span data-stu-id="25fd1-121">None</span></span>

## <span data-ttu-id="25fd1-122">출력</span><span class="sxs-lookup"><span data-stu-id="25fd1-122">OUTPUTS</span></span>

### <span data-ttu-id="25fd1-123">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="25fd1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="25fd1-124">상속자</span><span class="sxs-lookup"><span data-stu-id="25fd1-124">NOTES</span></span>

## <span data-ttu-id="25fd1-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25fd1-125">RELATED LINKS</span></span>

[<span data-ttu-id="25fd1-126">추가-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="25fd1-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="25fd1-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="25fd1-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="25fd1-128">제거-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="25fd1-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="25fd1-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="25fd1-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


