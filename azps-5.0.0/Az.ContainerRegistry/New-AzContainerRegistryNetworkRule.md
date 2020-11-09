---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304130"
---
# <span data-ttu-id="3fc97-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3fc97-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="3fc97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc97-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc97-103">네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-103">Create a network rule.</span></span>

## <span data-ttu-id="3fc97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fc97-104">SYNTAX</span></span>

### <span data-ttu-id="3fc97-105">ByVirtualNetworkRule (기본값)</span><span class="sxs-lookup"><span data-stu-id="3fc97-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fc97-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="3fc97-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fc97-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3fc97-107">DESCRIPTION</span></span>
<span data-ttu-id="3fc97-108">현재 powershell 세션에서 네트워크 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="3fc97-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3fc97-109">EXAMPLES</span></span>

### <span data-ttu-id="3fc97-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fc97-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="3fc97-111">Virtualnetwork 규칙 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="3fc97-112">변수</span><span class="sxs-lookup"><span data-stu-id="3fc97-112">PARAMETERS</span></span>

### <span data-ttu-id="3fc97-113">-작업</span><span class="sxs-lookup"><span data-stu-id="3fc97-113">-Action</span></span>
<span data-ttu-id="3fc97-114">네트워크 규칙의 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-114">The action of network rule.</span></span>

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

### <span data-ttu-id="3fc97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc97-115">-DefaultProfile</span></span>
<span data-ttu-id="3fc97-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fc97-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3fc97-117">-IPAddressOrRange</span></span>
<span data-ttu-id="3fc97-118">IP 또는 IP 범위를 CIDR 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="3fc97-119">IPV4 주소만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="3fc97-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3fc97-120">-IPRule</span></span>
<span data-ttu-id="3fc97-121">IPRule를 만들도록 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="3fc97-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3fc97-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3fc97-123">서브넷의 리소스 ID (예:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.)</span><span class="sxs-lookup"><span data-stu-id="3fc97-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="3fc97-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3fc97-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="3fc97-125">VirtualNetworkRule를 만들도록 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="3fc97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc97-126">CommonParameters</span></span>
<span data-ttu-id="3fc97-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fc97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc97-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3fc97-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc97-129">입력</span><span class="sxs-lookup"><span data-stu-id="3fc97-129">INPUTS</span></span>

### <span data-ttu-id="3fc97-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3fc97-130">System.String</span></span>

## <span data-ttu-id="3fc97-131">출력</span><span class="sxs-lookup"><span data-stu-id="3fc97-131">OUTPUTS</span></span>

### <span data-ttu-id="3fc97-132">ContainerRegistry. a s m a 네트워크 규칙</span><span class="sxs-lookup"><span data-stu-id="3fc97-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="3fc97-133">상속자</span><span class="sxs-lookup"><span data-stu-id="3fc97-133">NOTES</span></span>

## <span data-ttu-id="3fc97-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fc97-134">RELATED LINKS</span></span>
