---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 84a9ccb86f9fd1d4995ad52e913059181c0b887e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967787"
---
# <span data-ttu-id="f493d-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f493d-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f493d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f493d-102">SYNOPSIS</span></span>
<span data-ttu-id="f493d-103">백 엔드 HTTP 설정 개체의 연결 드레인 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f493d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f493d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f493d-105">설명</span><span class="sxs-lookup"><span data-stu-id="f493d-105">DESCRIPTION</span></span>
<span data-ttu-id="f493d-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레인 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f493d-107">예제</span><span class="sxs-lookup"><span data-stu-id="f493d-107">EXAMPLES</span></span>

### <span data-ttu-id="f493d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f493d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="f493d-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f493d-110">두 번째 명령은 $AppGw 설정이라는 백 엔드 HTTP 설정을 $Settings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f493d-111">마지막 명령은 False 및 DrainTimeoutInSec을 3600으로 설정하여 $Settings 저장된 백 엔드 HTTP 설정 개체의 연결 드레인 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="f493d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f493d-112">PARAMETERS</span></span>

### <span data-ttu-id="f493d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f493d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f493d-114">백end http 설정</span><span class="sxs-lookup"><span data-stu-id="f493d-114">The backend http settings</span></span>

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

### <span data-ttu-id="f493d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f493d-115">-DefaultProfile</span></span>
<span data-ttu-id="f493d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f493d-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="f493d-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="f493d-118">연결 드레인이 활성 상태인 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="f493d-119">허용되는 값은 1초에서 3600초까지입니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="f493d-120">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="f493d-120">-Enabled</span></span>
<span data-ttu-id="f493d-121">연결 드레인을 사용하도록 설정하는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="f493d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f493d-122">CommonParameters</span></span>
<span data-ttu-id="f493d-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f493d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f493d-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f493d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f493d-125">입력</span><span class="sxs-lookup"><span data-stu-id="f493d-125">INPUTS</span></span>

### <span data-ttu-id="f493d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f493d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f493d-127">출력</span><span class="sxs-lookup"><span data-stu-id="f493d-127">OUTPUTS</span></span>

### <span data-ttu-id="f493d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f493d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f493d-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f493d-129">NOTES</span></span>

## <span data-ttu-id="f493d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f493d-130">RELATED LINKS</span></span>

[<span data-ttu-id="f493d-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f493d-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f493d-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f493d-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f493d-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f493d-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f493d-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f493d-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f493d-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f493d-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

