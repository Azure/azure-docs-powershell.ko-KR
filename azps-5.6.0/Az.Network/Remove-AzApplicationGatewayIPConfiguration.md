---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 610fe3f2ba4867dc1145488dfe789dba051b23bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987751"
---
# <span data-ttu-id="ceda9-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceda9-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ceda9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceda9-102">SYNOPSIS</span></span>
<span data-ttu-id="ceda9-103">애플리케이션 게이트웨이에서 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="ceda9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ceda9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceda9-105">설명</span><span class="sxs-lookup"><span data-stu-id="ceda9-105">DESCRIPTION</span></span>
<span data-ttu-id="ceda9-106">**Remove-AzApplicationGatewayIPConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에서 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ceda9-107">예제</span><span class="sxs-lookup"><span data-stu-id="ceda9-107">EXAMPLES</span></span>

### <span data-ttu-id="ceda9-108">예제 1: Azure 애플리케이션 게이트웨이에서 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="ceda9-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="ceda9-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ceda9-110">두 번째 명령은 서브넷에 저장된 애플리케이션 게이트웨이에서 Subnet02라는 IP 구성을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ceda9-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ceda9-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ceda9-111">PARAMETERS</span></span>

### <span data-ttu-id="ceda9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ceda9-112">-ApplicationGateway</span></span>
<span data-ttu-id="ceda9-113">IP 구성을 제거할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="ceda9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceda9-114">-DefaultProfile</span></span>
<span data-ttu-id="ceda9-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceda9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ceda9-116">-Name</span></span>
<span data-ttu-id="ceda9-117">제거할 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceda9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceda9-118">CommonParameters</span></span>
<span data-ttu-id="ceda9-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ceda9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceda9-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ceda9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceda9-121">입력</span><span class="sxs-lookup"><span data-stu-id="ceda9-121">INPUTS</span></span>

### <span data-ttu-id="ceda9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ceda9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ceda9-123">출력</span><span class="sxs-lookup"><span data-stu-id="ceda9-123">OUTPUTS</span></span>

### <span data-ttu-id="ceda9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ceda9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ceda9-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ceda9-125">NOTES</span></span>

## <span data-ttu-id="ceda9-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceda9-126">RELATED LINKS</span></span>

[<span data-ttu-id="ceda9-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceda9-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ceda9-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceda9-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ceda9-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceda9-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ceda9-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceda9-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


