---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: 0fef46fb32c299a0d3117e8168e845777293d496
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963195"
---
# <span data-ttu-id="e7465-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7465-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="e7465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7465-102">SYNOPSIS</span></span>
<span data-ttu-id="e7465-103">네트워크 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-103">Create a network rule.</span></span>

## <span data-ttu-id="e7465-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7465-104">SYNTAX</span></span>

### <span data-ttu-id="e7465-105">ByVirtualNetworkRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="e7465-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7465-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="e7465-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7465-107">설명</span><span class="sxs-lookup"><span data-stu-id="e7465-107">DESCRIPTION</span></span>
<span data-ttu-id="e7465-108">현재 powershell 세션에서 네트워크 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="e7465-109">예제</span><span class="sxs-lookup"><span data-stu-id="e7465-109">EXAMPLES</span></span>

### <span data-ttu-id="e7465-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7465-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="e7465-111">Virtualnetwork 규칙 집합을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="e7465-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7465-112">PARAMETERS</span></span>

### <span data-ttu-id="e7465-113">-Action</span><span class="sxs-lookup"><span data-stu-id="e7465-113">-Action</span></span>
<span data-ttu-id="e7465-114">네트워크 규칙의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-114">The action of network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7465-115">-DefaultProfile</span></span>
<span data-ttu-id="e7465-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7465-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e7465-117">-IPAddressOrRange</span></span>
<span data-ttu-id="e7465-118">CIDR 형식으로 IP 또는 IP 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="e7465-119">IPV4 주소만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="e7465-120">-IPRule</span></span>
<span data-ttu-id="e7465-121">IPRule을 만들 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e7465-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e7465-123">서브넷의 리소스 ID(예: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="e7465-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7465-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="e7465-125">VirtualNetworkRule을 만들 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7465-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7465-126">CommonParameters</span></span>
<span data-ttu-id="e7465-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7465-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7465-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7465-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7465-129">입력</span><span class="sxs-lookup"><span data-stu-id="e7465-129">INPUTS</span></span>

### <span data-ttu-id="e7465-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e7465-130">System.String</span></span>

## <span data-ttu-id="e7465-131">출력</span><span class="sxs-lookup"><span data-stu-id="e7465-131">OUTPUTS</span></span>

### <span data-ttu-id="e7465-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7465-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="e7465-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7465-133">NOTES</span></span>

## <span data-ttu-id="e7465-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7465-134">RELATED LINKS</span></span>
