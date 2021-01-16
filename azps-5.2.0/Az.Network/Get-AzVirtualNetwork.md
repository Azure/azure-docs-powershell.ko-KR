---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356121"
---
# <span data-ttu-id="34636-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34636-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="34636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34636-102">SYNOPSIS</span></span>
<span data-ttu-id="34636-103">리소스 그룹의 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34636-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="34636-104">구문</span><span class="sxs-lookup"><span data-stu-id="34636-104">SYNTAX</span></span>

### <span data-ttu-id="34636-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="34636-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34636-106">확장</span><span class="sxs-lookup"><span data-stu-id="34636-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34636-107">설명</span><span class="sxs-lookup"><span data-stu-id="34636-107">DESCRIPTION</span></span>
<span data-ttu-id="34636-108">**Get-AzVirtualNetwork** cmdlet은 하나 이상의 가상 네트워크 n개 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34636-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="34636-109">예제</span><span class="sxs-lookup"><span data-stu-id="34636-109">EXAMPLES</span></span>

### <span data-ttu-id="34636-110">1: 가상 네트워크 검색</span><span class="sxs-lookup"><span data-stu-id="34636-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="34636-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyVirtualNetwork라는 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34636-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="34636-112">2: 필터를 사용하여 가상 네트워크 나열</span><span class="sxs-lookup"><span data-stu-id="34636-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="34636-113">이 명령은 "MyVirtualNetwork"로 시작하는 모든 가상 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34636-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="34636-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34636-114">PARAMETERS</span></span>

### <span data-ttu-id="34636-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34636-115">-DefaultProfile</span></span>
<span data-ttu-id="34636-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34636-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34636-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="34636-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34636-118">-Name</span><span class="sxs-lookup"><span data-stu-id="34636-118">-Name</span></span>
<span data-ttu-id="34636-119">이 cmdlet이 얻을 가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34636-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="34636-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34636-120">-ResourceGroupName</span></span>
<span data-ttu-id="34636-121">가상 네트워크가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34636-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="34636-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34636-122">CommonParameters</span></span>
<span data-ttu-id="34636-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34636-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34636-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34636-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34636-125">입력</span><span class="sxs-lookup"><span data-stu-id="34636-125">INPUTS</span></span>

### <span data-ttu-id="34636-126">System.String</span><span class="sxs-lookup"><span data-stu-id="34636-126">System.String</span></span>

## <span data-ttu-id="34636-127">출력</span><span class="sxs-lookup"><span data-stu-id="34636-127">OUTPUTS</span></span>

### <span data-ttu-id="34636-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34636-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="34636-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34636-129">NOTES</span></span>

## <span data-ttu-id="34636-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34636-130">RELATED LINKS</span></span>

[<span data-ttu-id="34636-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34636-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="34636-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34636-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="34636-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34636-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


