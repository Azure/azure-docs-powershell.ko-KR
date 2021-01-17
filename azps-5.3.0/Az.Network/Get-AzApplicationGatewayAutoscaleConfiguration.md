---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489967"
---
# <span data-ttu-id="f4687-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4687-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f4687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4687-102">SYNOPSIS</span></span>
<span data-ttu-id="f4687-103">Application Gateway의 자동 조정 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4687-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="f4687-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4687-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4687-105">설명</span><span class="sxs-lookup"><span data-stu-id="f4687-105">DESCRIPTION</span></span>
<span data-ttu-id="f4687-106">**Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet은 Application Gateway의 자동 크기 조정 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4687-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="f4687-107">예제</span><span class="sxs-lookup"><span data-stu-id="f4687-107">EXAMPLES</span></span>

### <span data-ttu-id="f4687-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4687-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="f4687-109">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $gw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f4687-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f4687-110">두 번째 명령은 애플리케이션 게이트웨이에서 자동 조정 구성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="f4687-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="f4687-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4687-111">PARAMETERS</span></span>

### <span data-ttu-id="f4687-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4687-112">-ApplicationGateway</span></span>
<span data-ttu-id="f4687-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4687-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f4687-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4687-114">-DefaultProfile</span></span>
<span data-ttu-id="f4687-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4687-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4687-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4687-116">CommonParameters</span></span>
<span data-ttu-id="f4687-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4687-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4687-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4687-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4687-119">입력</span><span class="sxs-lookup"><span data-stu-id="f4687-119">INPUTS</span></span>

### <span data-ttu-id="f4687-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4687-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4687-121">출력</span><span class="sxs-lookup"><span data-stu-id="f4687-121">OUTPUTS</span></span>

### <span data-ttu-id="f4687-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4687-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f4687-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4687-123">NOTES</span></span>

## <span data-ttu-id="f4687-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4687-124">RELATED LINKS</span></span>

[<span data-ttu-id="f4687-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4687-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f4687-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4687-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f4687-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4687-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
