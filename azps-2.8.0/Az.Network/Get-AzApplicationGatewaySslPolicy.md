---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870766"
---
# <span data-ttu-id="fe02b-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="fe02b-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="fe02b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe02b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe02b-103">응용 프로그램 게이트웨이의 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="fe02b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe02b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe02b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe02b-105">DESCRIPTION</span></span>
<span data-ttu-id="fe02b-106">**Get-AzApplicationGatewaySslPolicy** cmdlet은 응용 프로그램 게이트웨이의 SSL 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="fe02b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe02b-107">EXAMPLES</span></span>

### <span data-ttu-id="fe02b-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="fe02b-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="fe02b-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="fe02b-110">두 번째 명령은 $AppGW 이라는 변수에 저장 된 응용 프로그램 게이트웨이에서 ssl 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="fe02b-111">변수</span><span class="sxs-lookup"><span data-stu-id="fe02b-111">PARAMETERS</span></span>

### <span data-ttu-id="fe02b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe02b-112">-ApplicationGateway</span></span>
<span data-ttu-id="fe02b-113">이 cmdlet이 가져오는 SSL 정책의 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fe02b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe02b-114">-DefaultProfile</span></span>
<span data-ttu-id="fe02b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe02b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe02b-116">CommonParameters</span></span>
<span data-ttu-id="fe02b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe02b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe02b-118">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fe02b-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe02b-119">입력</span><span class="sxs-lookup"><span data-stu-id="fe02b-119">INPUTS</span></span>

### <span data-ttu-id="fe02b-120">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe02b-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe02b-121">출력</span><span class="sxs-lookup"><span data-stu-id="fe02b-121">OUTPUTS</span></span>

### <span data-ttu-id="fe02b-122">PSApplicationGatewaySslPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fe02b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="fe02b-123">상속자</span><span class="sxs-lookup"><span data-stu-id="fe02b-123">NOTES</span></span>
* <span data-ttu-id="fe02b-124">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="fe02b-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fe02b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe02b-125">RELATED LINKS</span></span>

[<span data-ttu-id="fe02b-126">새로운 AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="fe02b-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="fe02b-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="fe02b-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


