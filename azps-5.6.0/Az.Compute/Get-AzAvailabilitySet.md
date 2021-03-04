---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: 223f309fb0381f75a6398c44209baa2f3eb3bc22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969387"
---
# <span data-ttu-id="f2528-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2528-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="f2528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2528-102">SYNOPSIS</span></span>
<span data-ttu-id="f2528-103">리소스 그룹에서 Azure 가용성 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="f2528-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2528-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2528-105">설명</span><span class="sxs-lookup"><span data-stu-id="f2528-105">DESCRIPTION</span></span>
<span data-ttu-id="f2528-106">**Get-AzAvailabilitySet** cmdlet은 리소스 그룹에서 Azure 가용성 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="f2528-107">얻을 특정 가용성 집합의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="f2528-108">예제</span><span class="sxs-lookup"><span data-stu-id="f2528-108">EXAMPLES</span></span>

### <span data-ttu-id="f2528-109">예제 1: 특정 가용성 집합을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f2528-110">이 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f2528-111">예제 2: 모든 가용성 집합 사용</span><span class="sxs-lookup"><span data-stu-id="f2528-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f2528-112">이 명령은 ResourceGroup11이라는 리소스 그룹의 모든 가용성 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f2528-113">예제 3: 필터링을 사용하여 모든 가용성 집합 사용</span><span class="sxs-lookup"><span data-stu-id="f2528-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f2528-114">이 명령은 "AvailabilitySet0"로 시작하는 ResourceGroup11이라는 리소스 그룹의 모든 가용성 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="f2528-115">예제 4: AvailabilitySet0부터 시작하는 이름으로 모든 가용성 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="f2528-116">이 명령은 "AvailabilitySet0"로 시작하는 모든 가용성 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="f2528-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2528-117">PARAMETERS</span></span>

### <span data-ttu-id="f2528-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2528-118">-DefaultProfile</span></span>
<span data-ttu-id="f2528-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2528-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f2528-120">-Name</span></span>
<span data-ttu-id="f2528-121">이 cmdlet에서 얻을 가용성 집합의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f2528-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2528-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2528-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f2528-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2528-124">CommonParameters</span></span>
<span data-ttu-id="f2528-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2528-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2528-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2528-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2528-127">입력</span><span class="sxs-lookup"><span data-stu-id="f2528-127">INPUTS</span></span>

### <span data-ttu-id="f2528-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f2528-128">System.String</span></span>

## <span data-ttu-id="f2528-129">출력</span><span class="sxs-lookup"><span data-stu-id="f2528-129">OUTPUTS</span></span>

### <span data-ttu-id="f2528-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2528-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f2528-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2528-131">NOTES</span></span>

## <span data-ttu-id="f2528-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2528-132">RELATED LINKS</span></span>

[<span data-ttu-id="f2528-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2528-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="f2528-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2528-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


