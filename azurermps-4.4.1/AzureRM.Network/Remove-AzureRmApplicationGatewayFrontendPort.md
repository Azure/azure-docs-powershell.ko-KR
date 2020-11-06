---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9e3a9a515f7b33e23cb7444baa281e083c3c10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530778"
---
# <span data-ttu-id="42660-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42660-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="42660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42660-102">SYNOPSIS</span></span>
<span data-ttu-id="42660-103">응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42660-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42660-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42660-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42660-105">설명은</span><span class="sxs-lookup"><span data-stu-id="42660-105">DESCRIPTION</span></span>
<span data-ttu-id="42660-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42660-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="42660-107">예제의</span><span class="sxs-lookup"><span data-stu-id="42660-107">EXAMPLES</span></span>

### <span data-ttu-id="42660-108">예: 응용 프로그램 게이트웨이에서 프런트 엔드 포트 제거</span><span class="sxs-lookup"><span data-stu-id="42660-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="42660-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고 게이트웨이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42660-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="42660-110">두 번째 명령은 응용 프로그램 게이트웨이에서 FrontEndPort02 이라는 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42660-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="42660-111">변수</span><span class="sxs-lookup"><span data-stu-id="42660-111">PARAMETERS</span></span>

### <span data-ttu-id="42660-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42660-112">-ApplicationGateway</span></span>
<span data-ttu-id="42660-113">프런트 엔드 포트를 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42660-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="42660-114">-이름</span><span class="sxs-lookup"><span data-stu-id="42660-114">-Name</span></span>
<span data-ttu-id="42660-115">제거할 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42660-115">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="42660-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42660-116">-DefaultProfile</span></span>
<span data-ttu-id="42660-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42660-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42660-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42660-118">CommonParameters</span></span>
<span data-ttu-id="42660-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42660-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42660-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42660-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42660-121">입력</span><span class="sxs-lookup"><span data-stu-id="42660-121">INPUTS</span></span>

### <span data-ttu-id="42660-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42660-122">System.String</span></span>

## <span data-ttu-id="42660-123">출력</span><span class="sxs-lookup"><span data-stu-id="42660-123">OUTPUTS</span></span>

### <span data-ttu-id="42660-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42660-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42660-125">상속자</span><span class="sxs-lookup"><span data-stu-id="42660-125">NOTES</span></span>

## <span data-ttu-id="42660-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42660-126">RELATED LINKS</span></span>

[<span data-ttu-id="42660-127">추가-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42660-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42660-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42660-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42660-129">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42660-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42660-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42660-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)

