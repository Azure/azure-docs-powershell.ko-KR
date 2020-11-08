---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217257"
---
# <span data-ttu-id="c8bde-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c8bde-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c8bde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8bde-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bde-103">백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c8bde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8bde-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8bde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8bde-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bde-106">**AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c8bde-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c8bde-107">EXAMPLES</span></span>

### <span data-ttu-id="c8bde-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8bde-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="c8bde-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c8bde-110">두 번째 명령은 $AppGw에 대 한 Settings01 라는 백 엔드 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c8bde-111">마지막 명령은 $Settings에 저장 된 백 엔드 HTTP 설정의 연결 드레이닝 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="c8bde-112">변수</span><span class="sxs-lookup"><span data-stu-id="c8bde-112">PARAMETERS</span></span>

### <span data-ttu-id="c8bde-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c8bde-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c8bde-114">백 엔드 http 설정</span><span class="sxs-lookup"><span data-stu-id="c8bde-114">The backend http settings</span></span>

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

### <span data-ttu-id="c8bde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bde-115">-DefaultProfile</span></span>
<span data-ttu-id="c8bde-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8bde-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bde-117">CommonParameters</span></span>
<span data-ttu-id="c8bde-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8bde-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bde-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8bde-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bde-120">입력</span><span class="sxs-lookup"><span data-stu-id="c8bde-120">INPUTS</span></span>

### <span data-ttu-id="c8bde-121">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c8bde-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c8bde-122">출력</span><span class="sxs-lookup"><span data-stu-id="c8bde-122">OUTPUTS</span></span>

### <span data-ttu-id="c8bde-123">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c8bde-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c8bde-124">상속자</span><span class="sxs-lookup"><span data-stu-id="c8bde-124">NOTES</span></span>

## <span data-ttu-id="c8bde-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8bde-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8bde-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8bde-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c8bde-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c8bde-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c8bde-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c8bde-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c8bde-129">새로운 AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c8bde-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c8bde-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c8bde-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

