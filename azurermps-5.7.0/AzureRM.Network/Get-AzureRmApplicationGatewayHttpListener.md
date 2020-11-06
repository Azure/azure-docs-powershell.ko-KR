---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: a28aa5b0f611c8014ae2849e0dee6fe48aedfbe1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532125"
---
# <span data-ttu-id="5a5cb-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5a5cb-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5a5cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5cb-103">응용 프로그램 게이트웨이의 HTTP 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a5cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a5cb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a5cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="5a5cb-106">**Get-AzureRmApplicationGatewayHttpListener** cmdlet은 응용 프로그램 게이트웨이의 HTTP 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="5a5cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5a5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="5a5cb-108">예제 1: 특정 HTTP 수신기 가져오기</span><span class="sxs-lookup"><span data-stu-id="5a5cb-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="5a5cb-109">이 명령은 Listener01 이라는 HTTP 수신기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="5a5cb-110">예제 2: HTTP 수신기 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="5a5cb-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="5a5cb-111">이 명령은 HTTP 수신기 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="5a5cb-112">변수</span><span class="sxs-lookup"><span data-stu-id="5a5cb-112">PARAMETERS</span></span>

### <span data-ttu-id="5a5cb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a5cb-113">-ApplicationGateway</span></span>
<span data-ttu-id="5a5cb-114">HTTP 수신기를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a5cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5cb-115">-DefaultProfile</span></span>
<span data-ttu-id="5a5cb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a5cb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5a5cb-117">-Name</span></span>
<span data-ttu-id="5a5cb-118">이 cmdlet이 가져오는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5cb-119">CommonParameters</span></span>
<span data-ttu-id="5a5cb-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5cb-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a5cb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5cb-122">입력</span><span class="sxs-lookup"><span data-stu-id="5a5cb-122">INPUTS</span></span>

### <span data-ttu-id="5a5cb-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a5cb-123">System.String</span></span>

## <span data-ttu-id="5a5cb-124">출력</span><span class="sxs-lookup"><span data-stu-id="5a5cb-124">OUTPUTS</span></span>

### <span data-ttu-id="5a5cb-125">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5a5cb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5a5cb-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5a5cb-126">NOTES</span></span>

## <span data-ttu-id="5a5cb-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a5cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="5a5cb-128">추가-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5a5cb-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5a5cb-129">새로운 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5a5cb-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5a5cb-130">제거-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5a5cb-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5a5cb-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5a5cb-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


