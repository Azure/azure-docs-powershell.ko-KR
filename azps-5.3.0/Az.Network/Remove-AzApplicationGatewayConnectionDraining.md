---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378806"
---
# <span data-ttu-id="c7a82-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c7a82-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="c7a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a82-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a82-103">백 엔드 HTTP 설정 개체의 연결 드레인 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a82-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c7a82-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7a82-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a82-105">설명</span><span class="sxs-lookup"><span data-stu-id="c7a82-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a82-106">**Remove-AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레이팅 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a82-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="c7a82-107">예제</span><span class="sxs-lookup"><span data-stu-id="c7a82-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a82-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7a82-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="c7a82-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a82-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c7a82-110">두 번째 명령은 $AppGw Settings01이라는 백 엔드 HTTP 설정을 $Settings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a82-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="c7a82-111">마지막 명령은 백 엔드 HTTP 설정에 저장된 백 엔드 HTTP 설정의 연결 드레인 구성을 $Settings.</span><span class="sxs-lookup"><span data-stu-id="c7a82-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="c7a82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7a82-112">PARAMETERS</span></span>

### <span data-ttu-id="c7a82-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c7a82-113">-BackendHttpSettings</span></span>
<span data-ttu-id="c7a82-114">백end http 설정</span><span class="sxs-lookup"><span data-stu-id="c7a82-114">The backend http settings</span></span>

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

### <span data-ttu-id="c7a82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a82-115">-DefaultProfile</span></span>
<span data-ttu-id="c7a82-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a82-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a82-117">CommonParameters</span></span>
<span data-ttu-id="c7a82-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a82-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7a82-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a82-120">입력</span><span class="sxs-lookup"><span data-stu-id="c7a82-120">INPUTS</span></span>

### <span data-ttu-id="c7a82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c7a82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c7a82-122">출력</span><span class="sxs-lookup"><span data-stu-id="c7a82-122">OUTPUTS</span></span>

### <span data-ttu-id="c7a82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c7a82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c7a82-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7a82-124">NOTES</span></span>

## <span data-ttu-id="c7a82-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7a82-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7a82-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7a82-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c7a82-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c7a82-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c7a82-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c7a82-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c7a82-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c7a82-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="c7a82-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c7a82-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

