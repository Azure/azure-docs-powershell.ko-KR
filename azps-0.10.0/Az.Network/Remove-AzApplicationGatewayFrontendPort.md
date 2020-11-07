---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 39a2bd8ad1951cba41ff8fffb124c7486680b352
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875365"
---
# <span data-ttu-id="589ad-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="589ad-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="589ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="589ad-102">SYNOPSIS</span></span>
<span data-ttu-id="589ad-103">응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="589ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="589ad-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="589ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="589ad-105">DESCRIPTION</span></span>
<span data-ttu-id="589ad-106">**AzApplicationGatewayFrontendPort** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="589ad-107">예제의</span><span class="sxs-lookup"><span data-stu-id="589ad-107">EXAMPLES</span></span>

### <span data-ttu-id="589ad-108">예: 응용 프로그램 게이트웨이에서 프런트 엔드 포트 제거</span><span class="sxs-lookup"><span data-stu-id="589ad-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="589ad-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고 게이트웨이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="589ad-110">두 번째 명령은 응용 프로그램 게이트웨이에서 FrontEndPort02 이라는 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="589ad-111">변수</span><span class="sxs-lookup"><span data-stu-id="589ad-111">PARAMETERS</span></span>

### <span data-ttu-id="589ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="589ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="589ad-113">프런트 엔드 포트를 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="589ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589ad-114">-DefaultProfile</span></span>
<span data-ttu-id="589ad-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="589ad-116">-이름</span><span class="sxs-lookup"><span data-stu-id="589ad-116">-Name</span></span>
<span data-ttu-id="589ad-117">제거할 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="589ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589ad-118">CommonParameters</span></span>
<span data-ttu-id="589ad-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="589ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589ad-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589ad-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589ad-121">입력</span><span class="sxs-lookup"><span data-stu-id="589ad-121">INPUTS</span></span>

### <span data-ttu-id="589ad-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="589ad-122">System.String</span></span>

## <span data-ttu-id="589ad-123">출력</span><span class="sxs-lookup"><span data-stu-id="589ad-123">OUTPUTS</span></span>

### <span data-ttu-id="589ad-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="589ad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="589ad-125">상속자</span><span class="sxs-lookup"><span data-stu-id="589ad-125">NOTES</span></span>

## <span data-ttu-id="589ad-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="589ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="589ad-127">추가-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="589ad-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="589ad-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="589ad-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="589ad-129">새로운 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="589ad-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="589ad-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="589ad-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


