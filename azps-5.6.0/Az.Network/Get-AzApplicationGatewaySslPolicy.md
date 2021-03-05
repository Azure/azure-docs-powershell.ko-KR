---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994042"
---
# <span data-ttu-id="93ab9-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="93ab9-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="93ab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="93ab9-103">애플리케이션 게이트웨이의 SSL 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="93ab9-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="93ab9-104">구문</span><span class="sxs-lookup"><span data-stu-id="93ab9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93ab9-105">설명</span><span class="sxs-lookup"><span data-stu-id="93ab9-105">DESCRIPTION</span></span>
<span data-ttu-id="93ab9-106">**Get-AzApplicationGatewaySslPolicy** cmdlet은 애플리케이션 게이트웨이의 SSL 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="93ab9-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="93ab9-107">예제</span><span class="sxs-lookup"><span data-stu-id="93ab9-107">EXAMPLES</span></span>

### <span data-ttu-id="93ab9-108">1:</span><span class="sxs-lookup"><span data-stu-id="93ab9-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="93ab9-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="93ab9-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="93ab9-110">두 번째 명령은 애플리케이션 게이트웨이라는 변수에 저장된 Application Gateway에서 ssl 정책을 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="93ab9-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="93ab9-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="93ab9-111">PARAMETERS</span></span>

### <span data-ttu-id="93ab9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93ab9-112">-ApplicationGateway</span></span>
<span data-ttu-id="93ab9-113">이 cmdlet이 얻을 SSL 정책의 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93ab9-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="93ab9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ab9-114">-DefaultProfile</span></span>
<span data-ttu-id="93ab9-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93ab9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ab9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ab9-116">CommonParameters</span></span>
<span data-ttu-id="93ab9-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93ab9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ab9-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93ab9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ab9-119">입력</span><span class="sxs-lookup"><span data-stu-id="93ab9-119">INPUTS</span></span>

### <span data-ttu-id="93ab9-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93ab9-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93ab9-121">출력</span><span class="sxs-lookup"><span data-stu-id="93ab9-121">OUTPUTS</span></span>

### <span data-ttu-id="93ab9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="93ab9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="93ab9-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93ab9-123">NOTES</span></span>
* <span data-ttu-id="93ab9-124">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="93ab9-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="93ab9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93ab9-125">RELATED LINKS</span></span>

[<span data-ttu-id="93ab9-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="93ab9-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="93ab9-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="93ab9-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


