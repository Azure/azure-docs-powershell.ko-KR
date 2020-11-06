---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 58c7e2770380d309125b3e242c854fcdb86a8f08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530776"
---
# <span data-ttu-id="5b6a3-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5b6a3-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5b6a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6a3-103">응용 프로그램 게이트웨이에서 HTTP 수신기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b6a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b6a3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b6a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b6a3-105">DESCRIPTION</span></span>
<span data-ttu-id="5b6a3-106">**AzureRmApplicationGatewayHttpListener** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 HTTP 수신기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="5b6a3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b6a3-107">EXAMPLES</span></span>

### <span data-ttu-id="5b6a3-108">예제 1: 응용 프로그램 게이트웨이 HTTP 수신기 제거</span><span class="sxs-lookup"><span data-stu-id="5b6a3-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="5b6a3-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5b6a3-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Listener02 이라는 HTTP 수신기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5b6a3-111">변수</span><span class="sxs-lookup"><span data-stu-id="5b6a3-111">PARAMETERS</span></span>

### <span data-ttu-id="5b6a3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b6a3-112">-ApplicationGateway</span></span>
<span data-ttu-id="5b6a3-113">HTTP 수신기를 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="5b6a3-114">-이름</span><span class="sxs-lookup"><span data-stu-id="5b6a3-114">-Name</span></span>
<span data-ttu-id="5b6a3-115">이 cmdlet이 제거 하는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-115">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b6a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6a3-116">-DefaultProfile</span></span>
<span data-ttu-id="5b6a3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b6a3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6a3-118">CommonParameters</span></span>
<span data-ttu-id="5b6a3-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6a3-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b6a3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6a3-121">입력</span><span class="sxs-lookup"><span data-stu-id="5b6a3-121">INPUTS</span></span>

### <span data-ttu-id="5b6a3-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b6a3-122">System.String</span></span>

## <span data-ttu-id="5b6a3-123">출력</span><span class="sxs-lookup"><span data-stu-id="5b6a3-123">OUTPUTS</span></span>

### <span data-ttu-id="5b6a3-124">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5b6a3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5b6a3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="5b6a3-125">NOTES</span></span>

## <span data-ttu-id="5b6a3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b6a3-126">RELATED LINKS</span></span>

[<span data-ttu-id="5b6a3-127">추가-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5b6a3-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5b6a3-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5b6a3-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5b6a3-129">새로운 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5b6a3-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5b6a3-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5b6a3-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


