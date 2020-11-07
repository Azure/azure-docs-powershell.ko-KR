---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880993"
---
# <span data-ttu-id="de165-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de165-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="de165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de165-102">SYNOPSIS</span></span>
<span data-ttu-id="de165-103">응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="de165-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de165-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de165-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de165-105">설명은</span><span class="sxs-lookup"><span data-stu-id="de165-105">DESCRIPTION</span></span>
<span data-ttu-id="de165-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 프런트 엔드 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="de165-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="de165-107">예제의</span><span class="sxs-lookup"><span data-stu-id="de165-107">EXAMPLES</span></span>

### <span data-ttu-id="de165-108">예: 응용 프로그램 게이트웨이에서 프런트 엔드 포트 제거</span><span class="sxs-lookup"><span data-stu-id="de165-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="de165-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고 게이트웨이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="de165-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="de165-110">두 번째 명령은 응용 프로그램 게이트웨이에서 FrontEndPort02 이라는 포트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="de165-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="de165-111">변수</span><span class="sxs-lookup"><span data-stu-id="de165-111">PARAMETERS</span></span>

### <span data-ttu-id="de165-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de165-112">-ApplicationGateway</span></span>
<span data-ttu-id="de165-113">프런트 엔드 포트를 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de165-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="de165-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de165-114">-DefaultProfile</span></span>
<span data-ttu-id="de165-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de165-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de165-116">-이름</span><span class="sxs-lookup"><span data-stu-id="de165-116">-Name</span></span>
<span data-ttu-id="de165-117">제거할 프런트 엔드 포트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="de165-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="de165-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de165-118">CommonParameters</span></span>
<span data-ttu-id="de165-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de165-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de165-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de165-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de165-121">입력</span><span class="sxs-lookup"><span data-stu-id="de165-121">INPUTS</span></span>

### <span data-ttu-id="de165-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de165-122">System.String</span></span>

## <span data-ttu-id="de165-123">출력</span><span class="sxs-lookup"><span data-stu-id="de165-123">OUTPUTS</span></span>

### <span data-ttu-id="de165-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de165-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de165-125">상속자</span><span class="sxs-lookup"><span data-stu-id="de165-125">NOTES</span></span>

## <span data-ttu-id="de165-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de165-126">RELATED LINKS</span></span>

[<span data-ttu-id="de165-127">추가-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de165-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="de165-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de165-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="de165-129">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de165-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="de165-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de165-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


