---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2004fe6a10fe2700d256ae4cae8419ab631a2f64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875627"
---
# <span data-ttu-id="b043c-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b043c-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b043c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b043c-102">SYNOPSIS</span></span>
<span data-ttu-id="b043c-103">응용 프로그램 게이트웨이의 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="b043c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b043c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b043c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b043c-105">DESCRIPTION</span></span>
<span data-ttu-id="b043c-106">**Get-AzApplicationGatewayFrontendIPConfig** cmdlet은 응용 프로그램 게이트웨이의 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="b043c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b043c-107">EXAMPLES</span></span>

### <span data-ttu-id="b043c-108">예제 1: 지정 된 프런트 엔드 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b043c-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b043c-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에서 FrontEndIP01 이라는 프런트 엔드 IP 구성을 가져와 $FrontEndIP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="b043c-110">예제 2: 프런트 엔드 IP 구성 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="b043c-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="b043c-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에서 프런트 엔드 IP 구성 목록을 가져와 $FrontEndIPs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="b043c-112">변수</span><span class="sxs-lookup"><span data-stu-id="b043c-112">PARAMETERS</span></span>

### <span data-ttu-id="b043c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b043c-113">-ApplicationGateway</span></span>
<span data-ttu-id="b043c-114">프런트 엔드 IP 구성을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="b043c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b043c-115">-DefaultProfile</span></span>
<span data-ttu-id="b043c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b043c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b043c-117">-Name</span></span>
<span data-ttu-id="b043c-118">이 cmdlet이 가져오는 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b043c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b043c-119">CommonParameters</span></span>
<span data-ttu-id="b043c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b043c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b043c-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b043c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b043c-122">입력</span><span class="sxs-lookup"><span data-stu-id="b043c-122">INPUTS</span></span>

### <span data-ttu-id="b043c-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b043c-123">System.String</span></span>

## <span data-ttu-id="b043c-124">출력</span><span class="sxs-lookup"><span data-stu-id="b043c-124">OUTPUTS</span></span>

### <span data-ttu-id="b043c-125">PSApplicationGatewayFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b043c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="b043c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b043c-126">NOTES</span></span>

## <span data-ttu-id="b043c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b043c-127">RELATED LINKS</span></span>

[<span data-ttu-id="b043c-128">추가-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b043c-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b043c-129">새로운 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b043c-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b043c-130">제거-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b043c-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b043c-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b043c-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


