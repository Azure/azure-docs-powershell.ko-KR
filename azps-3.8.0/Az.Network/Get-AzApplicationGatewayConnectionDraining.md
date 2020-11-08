---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: c9ebdbf6feec64cc4545b1a77b39d91d4bf98d79
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043568"
---
# <span data-ttu-id="9ac07-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac07-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9ac07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac07-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac07-103">백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9ac07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ac07-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ac07-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac07-106">**AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9ac07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ac07-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac07-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ac07-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="9ac07-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9ac07-110">두 번째 명령은 $AppGw에 대 한 Settings01 라는 백 엔드 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="9ac07-111">마지막 명령은 백 엔드 HTTP 설정 $Settings의 연결 드레이닝 구성을 가져와 $ConnectionDraining 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="9ac07-112">변수</span><span class="sxs-lookup"><span data-stu-id="9ac07-112">PARAMETERS</span></span>

### <span data-ttu-id="9ac07-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9ac07-113">-BackendHttpSettings</span></span>
<span data-ttu-id="9ac07-114">백 엔드 http 설정</span><span class="sxs-lookup"><span data-stu-id="9ac07-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac07-115">-DefaultProfile</span></span>
<span data-ttu-id="9ac07-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac07-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac07-117">CommonParameters</span></span>
<span data-ttu-id="9ac07-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac07-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac07-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ac07-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac07-120">입력</span><span class="sxs-lookup"><span data-stu-id="9ac07-120">INPUTS</span></span>

### <span data-ttu-id="9ac07-121">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ac07-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9ac07-122">출력</span><span class="sxs-lookup"><span data-stu-id="9ac07-122">OUTPUTS</span></span>

### <span data-ttu-id="9ac07-123">Microsoft. 네트워크 모델. Psapplication게이트웨이 Connection드레이닝</span><span class="sxs-lookup"><span data-stu-id="9ac07-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9ac07-124">상속자</span><span class="sxs-lookup"><span data-stu-id="9ac07-124">NOTES</span></span>

## <span data-ttu-id="9ac07-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ac07-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ac07-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ac07-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9ac07-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9ac07-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="9ac07-128">새로운 AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac07-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9ac07-129">제거-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac07-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9ac07-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac07-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
