---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 071a6930ce7724c5db9d6bb21689ecb001a84424
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702211"
---
# <span data-ttu-id="219d7-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="219d7-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="219d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219d7-102">SYNOPSIS</span></span>
<span data-ttu-id="219d7-103">응용 프로그램 게이트웨이의 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="219d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="219d7-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="219d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="219d7-105">DESCRIPTION</span></span>
<span data-ttu-id="219d7-106">**Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet은 응용 프로그램 게이트웨이의 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="219d7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="219d7-107">EXAMPLES</span></span>

### <span data-ttu-id="219d7-108">예제 1: 지정 된 프런트 엔드 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="219d7-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="219d7-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에서 FrontEndIP01 이라는 프런트 엔드 IP 구성을 가져와 $FrontEndIP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="219d7-110">예제 2: 프런트 엔드 IP 구성 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="219d7-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="219d7-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에서 프런트 엔드 IP 구성 목록을 가져와 $FrontEndIPs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="219d7-112">변수</span><span class="sxs-lookup"><span data-stu-id="219d7-112">PARAMETERS</span></span>

### <span data-ttu-id="219d7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="219d7-113">-ApplicationGateway</span></span>
<span data-ttu-id="219d7-114">프런트 엔드 IP 구성을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="219d7-115">-이름</span><span class="sxs-lookup"><span data-stu-id="219d7-115">-Name</span></span>
<span data-ttu-id="219d7-116">이 cmdlet이 가져오는 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-116">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219d7-117">-DefaultProfile</span></span>
<span data-ttu-id="219d7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="219d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219d7-119">CommonParameters</span></span>
<span data-ttu-id="219d7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="219d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219d7-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219d7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219d7-122">입력</span><span class="sxs-lookup"><span data-stu-id="219d7-122">INPUTS</span></span>

### <span data-ttu-id="219d7-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="219d7-123">System.String</span></span>

## <span data-ttu-id="219d7-124">출력</span><span class="sxs-lookup"><span data-stu-id="219d7-124">OUTPUTS</span></span>

### <span data-ttu-id="219d7-125">PSApplicationGatewayFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="219d7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="219d7-126">상속자</span><span class="sxs-lookup"><span data-stu-id="219d7-126">NOTES</span></span>

## <span data-ttu-id="219d7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="219d7-127">RELATED LINKS</span></span>

[<span data-ttu-id="219d7-128">추가-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="219d7-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="219d7-129">새로운 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="219d7-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="219d7-130">제거-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="219d7-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="219d7-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="219d7-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


