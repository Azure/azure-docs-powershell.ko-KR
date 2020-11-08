---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213120"
---
# <span data-ttu-id="92158-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92158-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="92158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92158-102">SYNOPSIS</span></span>
<span data-ttu-id="92158-103">리소스 그룹의 Azure 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92158-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="92158-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92158-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92158-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92158-105">DESCRIPTION</span></span>
<span data-ttu-id="92158-106">**Get-AzAvailabilitySet** cmdlet은 리소스 그룹의 Azure 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92158-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="92158-107">가져올 특정 가용성 집합의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92158-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="92158-108">예제의</span><span class="sxs-lookup"><span data-stu-id="92158-108">EXAMPLES</span></span>

### <span data-ttu-id="92158-109">예제 1: 특정 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="92158-109">Example 1: Get a specific availability set</span></span>
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

<span data-ttu-id="92158-110">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet03 이라는 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92158-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="92158-111">예제 2: 모든 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="92158-111">Example 2: Get all availability sets</span></span>
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

<span data-ttu-id="92158-112">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 모든 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92158-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="92158-113">예제 3: 필터링을 사용 하 여 모든 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="92158-113">Example 3: Get all availability sets with filtering</span></span>
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

<span data-ttu-id="92158-114">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 "AvailabilitySet0"로 시작 하는 모든 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92158-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="92158-115">예제 4: 이름이 AvailabilitySet0로 시작 하는 모든 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="92158-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
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

<span data-ttu-id="92158-116">이 명령은 "AvailabilitySet0"로 시작 하는 모든 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92158-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="92158-117">변수</span><span class="sxs-lookup"><span data-stu-id="92158-117">PARAMETERS</span></span>

### <span data-ttu-id="92158-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92158-118">-DefaultProfile</span></span>
<span data-ttu-id="92158-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92158-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92158-120">-이름</span><span class="sxs-lookup"><span data-stu-id="92158-120">-Name</span></span>
<span data-ttu-id="92158-121">이 cmdlet이 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92158-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="92158-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92158-122">-ResourceGroupName</span></span>
<span data-ttu-id="92158-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92158-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="92158-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92158-124">CommonParameters</span></span>
<span data-ttu-id="92158-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92158-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92158-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="92158-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92158-127">입력</span><span class="sxs-lookup"><span data-stu-id="92158-127">INPUTS</span></span>

### <span data-ttu-id="92158-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="92158-128">System.String</span></span>

## <span data-ttu-id="92158-129">출력</span><span class="sxs-lookup"><span data-stu-id="92158-129">OUTPUTS</span></span>

### <span data-ttu-id="92158-130">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="92158-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="92158-131">상속자</span><span class="sxs-lookup"><span data-stu-id="92158-131">NOTES</span></span>

## <span data-ttu-id="92158-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92158-132">RELATED LINKS</span></span>

[<span data-ttu-id="92158-133">새로운 AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92158-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="92158-134">제거-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92158-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


