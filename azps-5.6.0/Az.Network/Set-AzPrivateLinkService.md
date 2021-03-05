---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: fc0e3ad0bcc86a0ad49450393a79c6c60540ba23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001056"
---
# <span data-ttu-id="3ec98-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="3ec98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec98-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec98-103">개인 링크 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-103">Updates a private link service.</span></span>

## <span data-ttu-id="3ec98-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ec98-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ec98-105">설명</span><span class="sxs-lookup"><span data-stu-id="3ec98-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec98-106">**Set-AzPrivateLinkService** cmdlet은 개인 링크 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="3ec98-107">예제</span><span class="sxs-lookup"><span data-stu-id="3ec98-107">EXAMPLES</span></span>

### <span data-ttu-id="3ec98-108">1: 개인 링크 서비스를 만들고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="3ec98-109">이 예제에서는 mypls라는 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="3ec98-110">그런 다음 메모리 내 ipConfiguratiuon 개체에서 해당 ipConfigurations를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="3ec98-111">그런 Set-AzPrivateLinkService cmdlet은 서비스 쪽에서 수정된 개인 링크 서비스 상태를 작성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="3ec98-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ec98-112">PARAMETERS</span></span>

### <span data-ttu-id="3ec98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ec98-113">-AsJob</span></span>
<span data-ttu-id="3ec98-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3ec98-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec98-115">-DefaultProfile</span></span>
<span data-ttu-id="3ec98-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ec98-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-117">-PrivateLinkService</span></span>
<span data-ttu-id="3ec98-118">개인 링크 서비스를 설정해야 하는 상태를 나타내는 개인 링크 서비스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec98-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec98-119">CommonParameters</span></span>
<span data-ttu-id="3ec98-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ec98-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec98-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ec98-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec98-122">입력</span><span class="sxs-lookup"><span data-stu-id="3ec98-122">INPUTS</span></span>

### <span data-ttu-id="3ec98-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="3ec98-124">출력</span><span class="sxs-lookup"><span data-stu-id="3ec98-124">OUTPUTS</span></span>

### <span data-ttu-id="3ec98-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="3ec98-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ec98-126">NOTES</span></span>

## <span data-ttu-id="3ec98-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ec98-127">RELATED LINKS</span></span>

[<span data-ttu-id="3ec98-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="3ec98-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="3ec98-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ec98-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


