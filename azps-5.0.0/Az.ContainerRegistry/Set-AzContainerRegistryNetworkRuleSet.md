---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215578"
---
# <span data-ttu-id="42eec-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="42eec-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="42eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42eec-102">SYNOPSIS</span></span>
<span data-ttu-id="42eec-103">네트워크 규칙 집합을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eec-103">Create or update a network rule set.</span></span> <span data-ttu-id="42eec-104">규칙 집합은 "Premium" 레지스트리에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42eec-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="42eec-105">구문과</span><span class="sxs-lookup"><span data-stu-id="42eec-105">SYNTAX</span></span>

### <span data-ttu-id="42eec-106">AddAddNetworkRuleWithoutInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="42eec-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42eec-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="42eec-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42eec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="42eec-108">DESCRIPTION</span></span>
<span data-ttu-id="42eec-109">네트워크 규칙 집합 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="42eec-109">Create or update a network rule set</span></span>

## <span data-ttu-id="42eec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="42eec-110">EXAMPLES</span></span>

### <span data-ttu-id="42eec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="42eec-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="42eec-112">새 네트워크 규칙 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42eec-112">Create a new network rule set.</span></span>

## <span data-ttu-id="42eec-113">변수</span><span class="sxs-lookup"><span data-stu-id="42eec-113">PARAMETERS</span></span>

### <span data-ttu-id="42eec-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="42eec-114">-DefaultAction</span></span>
<span data-ttu-id="42eec-115">Default 작업, ' 허용 ' 또는 ' 거부 ' 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42eec-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42eec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42eec-116">-DefaultProfile</span></span>
<span data-ttu-id="42eec-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42eec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42eec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42eec-118">-InputObject</span></span>
<span data-ttu-id="42eec-119">PSNetworkRuleSet 집합 입력</span><span class="sxs-lookup"><span data-stu-id="42eec-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42eec-120">-네트워크 규칙</span><span class="sxs-lookup"><span data-stu-id="42eec-120">-NetworkRule</span></span>
<span data-ttu-id="42eec-121">네트워크 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="42eec-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42eec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42eec-122">CommonParameters</span></span>
<span data-ttu-id="42eec-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42eec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42eec-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42eec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42eec-125">입력</span><span class="sxs-lookup"><span data-stu-id="42eec-125">INPUTS</span></span>

### <span data-ttu-id="42eec-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42eec-126">System.String</span></span>

### <span data-ttu-id="42eec-127">ContainerRegistry. a s m a 네트워크 규칙</span><span class="sxs-lookup"><span data-stu-id="42eec-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="42eec-128">출력</span><span class="sxs-lookup"><span data-stu-id="42eec-128">OUTPUTS</span></span>

### <span data-ttu-id="42eec-129">ContainerRegistry. a m m.</span><span class="sxs-lookup"><span data-stu-id="42eec-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="42eec-130">상속자</span><span class="sxs-lookup"><span data-stu-id="42eec-130">NOTES</span></span>

## <span data-ttu-id="42eec-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42eec-131">RELATED LINKS</span></span>
