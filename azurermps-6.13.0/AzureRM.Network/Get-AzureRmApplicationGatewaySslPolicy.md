---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 97851183233993400205993f091c8c57f376fcaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703453"
---
# <span data-ttu-id="10684-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="10684-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="10684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10684-102">SYNOPSIS</span></span>
<span data-ttu-id="10684-103">응용 프로그램 게이트웨이의 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10684-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10684-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10684-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10684-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10684-105">DESCRIPTION</span></span>
<span data-ttu-id="10684-106">**Get-AzureRmApplicationGatewaySslPolicy** cmdlet은 응용 프로그램 게이트웨이의 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10684-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="10684-107">예제의</span><span class="sxs-lookup"><span data-stu-id="10684-107">EXAMPLES</span></span>

### <span data-ttu-id="10684-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="10684-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="10684-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="10684-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="10684-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 ssl 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10684-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="10684-111">변수</span><span class="sxs-lookup"><span data-stu-id="10684-111">PARAMETERS</span></span>

### <span data-ttu-id="10684-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10684-112">-ApplicationGateway</span></span>
<span data-ttu-id="10684-113">이 cmdlet이 가져오는 SSL 정책의 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10684-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10684-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10684-114">-DefaultProfile</span></span>
<span data-ttu-id="10684-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10684-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10684-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10684-116">CommonParameters</span></span>
<span data-ttu-id="10684-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10684-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10684-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10684-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10684-119">입력</span><span class="sxs-lookup"><span data-stu-id="10684-119">INPUTS</span></span>

### <span data-ttu-id="10684-120">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10684-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="10684-121">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10684-121">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="10684-122">출력</span><span class="sxs-lookup"><span data-stu-id="10684-122">OUTPUTS</span></span>

### <span data-ttu-id="10684-123">PSApplicationGatewaySslPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="10684-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="10684-124">상속자</span><span class="sxs-lookup"><span data-stu-id="10684-124">NOTES</span></span>
* <span data-ttu-id="10684-125">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="10684-125">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="10684-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10684-126">RELATED LINKS</span></span>

[<span data-ttu-id="10684-127">새로운 AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="10684-127">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="10684-128">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="10684-128">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


