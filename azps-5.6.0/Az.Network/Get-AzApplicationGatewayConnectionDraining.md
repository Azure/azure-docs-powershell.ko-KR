---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3d1df3262fa9cee55d5aa49c026b7b1e681b5c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996585"
---
# <span data-ttu-id="fde06-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fde06-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="fde06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde06-102">SYNOPSIS</span></span>
<span data-ttu-id="fde06-103">백 엔드 HTTP 설정 개체의 연결 드레인 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="fde06-104">구문</span><span class="sxs-lookup"><span data-stu-id="fde06-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fde06-105">설명</span><span class="sxs-lookup"><span data-stu-id="fde06-105">DESCRIPTION</span></span>
<span data-ttu-id="fde06-106">**Get-AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레인 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="fde06-107">예제</span><span class="sxs-lookup"><span data-stu-id="fde06-107">EXAMPLES</span></span>

### <span data-ttu-id="fde06-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fde06-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="fde06-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fde06-110">두 번째 명령은 $AppGw 설정이라는 백 엔드 HTTP 설정을 $Settings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="fde06-111">마지막 명령은 백 엔드 HTTP 설정에서 연결 드레인 구성을 $Settings 및 $ConnectionDraining 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="fde06-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fde06-112">PARAMETERS</span></span>

### <span data-ttu-id="fde06-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fde06-113">-BackendHttpSettings</span></span>
<span data-ttu-id="fde06-114">백end http 설정</span><span class="sxs-lookup"><span data-stu-id="fde06-114">The backend http settings</span></span>

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

### <span data-ttu-id="fde06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde06-115">-DefaultProfile</span></span>
<span data-ttu-id="fde06-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fde06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde06-117">CommonParameters</span></span>
<span data-ttu-id="fde06-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fde06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde06-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fde06-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde06-120">입력</span><span class="sxs-lookup"><span data-stu-id="fde06-120">INPUTS</span></span>

### <span data-ttu-id="fde06-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fde06-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="fde06-122">출력</span><span class="sxs-lookup"><span data-stu-id="fde06-122">OUTPUTS</span></span>

### <span data-ttu-id="fde06-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fde06-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="fde06-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fde06-124">NOTES</span></span>

## <span data-ttu-id="fde06-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fde06-125">RELATED LINKS</span></span>

[<span data-ttu-id="fde06-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fde06-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="fde06-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fde06-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="fde06-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fde06-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="fde06-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fde06-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="fde06-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fde06-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
