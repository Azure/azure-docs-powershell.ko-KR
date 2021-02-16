---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179729"
---
# <span data-ttu-id="8dfb9-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfb9-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8dfb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dfb9-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfb9-103">애플리케이션 게이트웨이에 대한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="8dfb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="8dfb9-104">SYNTAX</span></span>

### <span data-ttu-id="8dfb9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfb9-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dfb9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8dfb9-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dfb9-107">설명</span><span class="sxs-lookup"><span data-stu-id="8dfb9-107">DESCRIPTION</span></span>
<span data-ttu-id="8dfb9-108">**New-AzApplicationGatewayIPConfiguration** cmdlet은 애플리케이션 게이트웨이에 대한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="8dfb9-109">IP 구성에는 애플리케이션 게이트웨이가 배포된 서브넷이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="8dfb9-110">예제</span><span class="sxs-lookup"><span data-stu-id="8dfb9-110">EXAMPLES</span></span>

### <span data-ttu-id="8dfb9-111">예제 1: 애플리케이션 게이트웨이에 대한 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="8dfb9-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="8dfb9-112">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="8dfb9-113">두 번째 명령은 이전 명령의 가상 네트워크가 속한 서브넷에 대한 서브넷 구성을 사용하여 $Subnet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="8dfb9-114">세 번째 명령은 다음 명령을 사용하여 IP $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="8dfb9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dfb9-115">PARAMETERS</span></span>

### <span data-ttu-id="8dfb9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfb9-116">-DefaultProfile</span></span>
<span data-ttu-id="8dfb9-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dfb9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8dfb9-118">-Name</span></span>
<span data-ttu-id="8dfb9-119">만들 IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="8dfb9-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="8dfb9-120">-Subnet</span></span>
<span data-ttu-id="8dfb9-121">서브넷 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-121">Specifies the subnet object.</span></span>
<span data-ttu-id="8dfb9-122">애플리케이션 게이트웨이가 배포되는 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfb9-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8dfb9-123">-SubnetId</span></span>
<span data-ttu-id="8dfb9-124">서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="8dfb9-125">애플리케이션 게이트웨이가 배포될 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfb9-126">CommonParameters</span></span>
<span data-ttu-id="8dfb9-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfb9-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8dfb9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfb9-129">입력</span><span class="sxs-lookup"><span data-stu-id="8dfb9-129">INPUTS</span></span>

### <span data-ttu-id="8dfb9-130">없음</span><span class="sxs-lookup"><span data-stu-id="8dfb9-130">None</span></span>

## <span data-ttu-id="8dfb9-131">출력</span><span class="sxs-lookup"><span data-stu-id="8dfb9-131">OUTPUTS</span></span>

### <span data-ttu-id="8dfb9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfb9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8dfb9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8dfb9-133">NOTES</span></span>

## <span data-ttu-id="8dfb9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dfb9-134">RELATED LINKS</span></span>

[<span data-ttu-id="8dfb9-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfb9-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8dfb9-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfb9-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8dfb9-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfb9-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8dfb9-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dfb9-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


