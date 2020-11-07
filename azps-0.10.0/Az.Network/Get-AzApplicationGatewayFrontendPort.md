---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875628"
---
# <span data-ttu-id="84214-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="84214-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="84214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84214-102">SYNOPSIS</span></span>
<span data-ttu-id="84214-103">응용 프로그램 게이트웨이의 프런트 엔드 포트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84214-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="84214-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84214-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84214-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84214-105">DESCRIPTION</span></span>
<span data-ttu-id="84214-106">**Get-AzApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이의 프런트 엔드 포트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84214-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="84214-107">예제의</span><span class="sxs-lookup"><span data-stu-id="84214-107">EXAMPLES</span></span>

### <span data-ttu-id="84214-108">예제 1: 지정 된 프런트 엔드 포트 가져오기</span><span class="sxs-lookup"><span data-stu-id="84214-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="84214-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="84214-110">두 번째 명령은 $AppGw에서 FrontEndPort01 이라는 프런트 엔드 포트를 가져와 $FrontEndPort 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="84214-111">예제 2: 프런트 엔드 포트 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="84214-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="84214-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="84214-113">두 번째 명령은 $AppGw에서 프런트 엔드 포트 목록을 가져와 $FrontEndPorts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="84214-114">변수</span><span class="sxs-lookup"><span data-stu-id="84214-114">PARAMETERS</span></span>

### <span data-ttu-id="84214-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84214-115">-ApplicationGateway</span></span>
<span data-ttu-id="84214-116">프런트 엔드 포트를 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="84214-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84214-117">-DefaultProfile</span></span>
<span data-ttu-id="84214-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84214-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84214-119">-이름</span><span class="sxs-lookup"><span data-stu-id="84214-119">-Name</span></span>
<span data-ttu-id="84214-120">가져올 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="84214-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84214-121">CommonParameters</span></span>
<span data-ttu-id="84214-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84214-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84214-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84214-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84214-124">입력</span><span class="sxs-lookup"><span data-stu-id="84214-124">INPUTS</span></span>

### <span data-ttu-id="84214-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84214-125">System.String</span></span>

## <span data-ttu-id="84214-126">출력</span><span class="sxs-lookup"><span data-stu-id="84214-126">OUTPUTS</span></span>

### <span data-ttu-id="84214-127">PSApplicationGatewayFrontendPort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="84214-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="84214-128">상속자</span><span class="sxs-lookup"><span data-stu-id="84214-128">NOTES</span></span>

## <span data-ttu-id="84214-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84214-129">RELATED LINKS</span></span>

[<span data-ttu-id="84214-130">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="84214-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="84214-131">새로운 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="84214-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="84214-132">제거-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="84214-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="84214-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="84214-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


