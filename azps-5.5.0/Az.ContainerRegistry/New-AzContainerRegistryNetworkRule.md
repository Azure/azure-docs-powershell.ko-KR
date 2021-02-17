---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196900"
---
# <span data-ttu-id="4b233-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b233-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="4b233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b233-102">SYNOPSIS</span></span>
<span data-ttu-id="4b233-103">네트워크 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-103">Create a network rule.</span></span>

## <span data-ttu-id="4b233-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b233-104">SYNTAX</span></span>

### <span data-ttu-id="4b233-105">ByVirtualNetworkRule(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b233-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b233-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="4b233-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b233-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b233-107">DESCRIPTION</span></span>
<span data-ttu-id="4b233-108">현재 PowerShell 세션에서 네트워크 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="4b233-109">예제</span><span class="sxs-lookup"><span data-stu-id="4b233-109">EXAMPLES</span></span>

### <span data-ttu-id="4b233-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b233-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="4b233-111">virtualnetwork 규칙 집합을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="4b233-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b233-112">PARAMETERS</span></span>

### <span data-ttu-id="4b233-113">-Action</span><span class="sxs-lookup"><span data-stu-id="4b233-113">-Action</span></span>
<span data-ttu-id="4b233-114">네트워크 규칙의 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-114">The action of network rule.</span></span>

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

### <span data-ttu-id="4b233-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b233-115">-DefaultProfile</span></span>
<span data-ttu-id="4b233-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b233-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4b233-117">-IPAddressOrRange</span></span>
<span data-ttu-id="4b233-118">IP 또는 IP 범위를 CIDR 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="4b233-119">IPV4 주소만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="4b233-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="4b233-120">-IPRule</span></span>
<span data-ttu-id="4b233-121">IPRule을 만들 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="4b233-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4b233-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="4b233-123">서브넷의 리소스 ID(예: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}).</span><span class="sxs-lookup"><span data-stu-id="4b233-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="4b233-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b233-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="4b233-125">VirtualNetworkRule을 만들 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="4b233-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b233-126">CommonParameters</span></span>
<span data-ttu-id="4b233-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b233-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b233-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b233-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b233-129">입력</span><span class="sxs-lookup"><span data-stu-id="4b233-129">INPUTS</span></span>

### <span data-ttu-id="4b233-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4b233-130">System.String</span></span>

## <span data-ttu-id="4b233-131">출력</span><span class="sxs-lookup"><span data-stu-id="4b233-131">OUTPUTS</span></span>

### <span data-ttu-id="4b233-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b233-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="4b233-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b233-133">NOTES</span></span>

## <span data-ttu-id="4b233-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b233-134">RELATED LINKS</span></span>
