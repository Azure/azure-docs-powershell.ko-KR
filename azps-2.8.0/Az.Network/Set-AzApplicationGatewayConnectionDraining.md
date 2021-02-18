---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 042eb9bdff35cb406a879b454b3b78451a89d789
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410539"
---
# <span data-ttu-id="f1b49-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f1b49-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f1b49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b49-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b49-103">백 엔드 HTTP 설정 개체의 연결 드레인 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f1b49-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1b49-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1b49-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1b49-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b49-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레인 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f1b49-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1b49-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b49-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1b49-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="f1b49-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f1b49-110">두 번째 명령은 $AppGw Settings01이라는 백 엔드 HTTP 설정을 $Settings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f1b49-111">마지막 명령은 False로 설정하고 DrainTimeoutInSec을 3600으로 설정하여 $Settings 백 엔드 HTTP 설정 개체의 연결 드레인 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="f1b49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1b49-112">PARAMETERS</span></span>

### <span data-ttu-id="f1b49-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1b49-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f1b49-114">백end http 설정</span><span class="sxs-lookup"><span data-stu-id="f1b49-114">The backend http settings</span></span>

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

### <span data-ttu-id="f1b49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b49-115">-DefaultProfile</span></span>
<span data-ttu-id="f1b49-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1b49-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="f1b49-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="f1b49-118">연결 드레인이 활성 상태인 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="f1b49-119">허용되는 값은 1초에서 3600초입니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="f1b49-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f1b49-120">-Enabled</span></span>
<span data-ttu-id="f1b49-121">연결 드레인을 사용하도록 설정되어 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="f1b49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b49-122">CommonParameters</span></span>
<span data-ttu-id="f1b49-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b49-124">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1b49-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b49-125">입력</span><span class="sxs-lookup"><span data-stu-id="f1b49-125">INPUTS</span></span>

### <span data-ttu-id="f1b49-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1b49-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f1b49-127">출력</span><span class="sxs-lookup"><span data-stu-id="f1b49-127">OUTPUTS</span></span>

### <span data-ttu-id="f1b49-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1b49-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f1b49-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1b49-129">NOTES</span></span>

## <span data-ttu-id="f1b49-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1b49-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1b49-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1b49-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="f1b49-132">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f1b49-132">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f1b49-133">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f1b49-133">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f1b49-134">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f1b49-134">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

