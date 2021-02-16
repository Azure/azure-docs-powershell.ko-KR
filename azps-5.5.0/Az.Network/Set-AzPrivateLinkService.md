---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184169"
---
# <span data-ttu-id="74f85-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="74f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f85-102">SYNOPSIS</span></span>
<span data-ttu-id="74f85-103">개인 링크 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-103">Updates a private link service.</span></span>

## <span data-ttu-id="74f85-104">구문</span><span class="sxs-lookup"><span data-stu-id="74f85-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f85-105">설명</span><span class="sxs-lookup"><span data-stu-id="74f85-105">DESCRIPTION</span></span>
<span data-ttu-id="74f85-106">**Set-AzPrivateLinkService** cmdlet은 개인 링크 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="74f85-107">예제</span><span class="sxs-lookup"><span data-stu-id="74f85-107">EXAMPLES</span></span>

### <span data-ttu-id="74f85-108">1: 개인 링크 서비스를 만들고 해당 링크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="74f85-109">이 예제에서는 mypls라는 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="74f85-110">그런 다음 메모리 내 ipConfiguratiuon 개체에서 해당 ipConfigurations를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="74f85-111">그런 Set-AzPrivateLinkService cmdlet은 서비스 쪽에서 수정된 개인 링크 서비스 상태를 작성하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="74f85-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f85-112">PARAMETERS</span></span>

### <span data-ttu-id="74f85-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74f85-113">-AsJob</span></span>
<span data-ttu-id="74f85-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="74f85-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74f85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f85-115">-DefaultProfile</span></span>
<span data-ttu-id="74f85-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f85-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-117">-PrivateLinkService</span></span>
<span data-ttu-id="74f85-118">개인 링크 서비스를 설정해야 하는 상태를 나타내는 개인 링크 서비스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="74f85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f85-119">CommonParameters</span></span>
<span data-ttu-id="74f85-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74f85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f85-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74f85-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f85-122">입력</span><span class="sxs-lookup"><span data-stu-id="74f85-122">INPUTS</span></span>

### <span data-ttu-id="74f85-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="74f85-124">출력</span><span class="sxs-lookup"><span data-stu-id="74f85-124">OUTPUTS</span></span>

### <span data-ttu-id="74f85-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="74f85-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74f85-126">NOTES</span></span>

## <span data-ttu-id="74f85-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74f85-127">RELATED LINKS</span></span>

[<span data-ttu-id="74f85-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="74f85-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="74f85-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="74f85-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


