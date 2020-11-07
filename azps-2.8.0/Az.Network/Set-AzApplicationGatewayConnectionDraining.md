---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: d04dc0c3d9d446941870f30578f50d5ecd795009
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869614"
---
# <span data-ttu-id="10df4-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10df4-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="10df4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10df4-102">SYNOPSIS</span></span>
<span data-ttu-id="10df4-103">백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="10df4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10df4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10df4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10df4-105">DESCRIPTION</span></span>
<span data-ttu-id="10df4-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="10df4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="10df4-107">EXAMPLES</span></span>

### <span data-ttu-id="10df4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="10df4-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="10df4-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="10df4-110">두 번째 명령은 $AppGw에 대 한 Settings01 라는 백 엔드 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="10df4-111">마지막 명령은 $Settings에 저장 된 백 엔드 HTTP 설정 개체의 연결 드레이닝 구성을 False로 설정 하 고 DrainTimeoutInSec를 3600로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="10df4-112">변수</span><span class="sxs-lookup"><span data-stu-id="10df4-112">PARAMETERS</span></span>

### <span data-ttu-id="10df4-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="10df4-113">-BackendHttpSettings</span></span>
<span data-ttu-id="10df4-114">백 엔드 http 설정</span><span class="sxs-lookup"><span data-stu-id="10df4-114">The backend http settings</span></span>

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

### <span data-ttu-id="10df4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10df4-115">-DefaultProfile</span></span>
<span data-ttu-id="10df4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10df4-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="10df4-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="10df4-118">연결 드레이닝이 활성 상태인 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="10df4-119">허용 되는 값은 1 초에서 3600 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10df4-120">-사용</span><span class="sxs-lookup"><span data-stu-id="10df4-120">-Enabled</span></span>
<span data-ttu-id="10df4-121">연결 드레이닝이 사용 되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10df4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10df4-122">CommonParameters</span></span>
<span data-ttu-id="10df4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10df4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10df4-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10df4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10df4-125">입력</span><span class="sxs-lookup"><span data-stu-id="10df4-125">INPUTS</span></span>

### <span data-ttu-id="10df4-126">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="10df4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="10df4-127">출력</span><span class="sxs-lookup"><span data-stu-id="10df4-127">OUTPUTS</span></span>

### <span data-ttu-id="10df4-128">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="10df4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="10df4-129">상속자</span><span class="sxs-lookup"><span data-stu-id="10df4-129">NOTES</span></span>

## <span data-ttu-id="10df4-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10df4-130">RELATED LINKS</span></span>

[<span data-ttu-id="10df4-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10df4-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="10df4-132">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="10df4-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="10df4-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10df4-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="10df4-134">새로운 AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10df4-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="10df4-135">제거-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10df4-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

