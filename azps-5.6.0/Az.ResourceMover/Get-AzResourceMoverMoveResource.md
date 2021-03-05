---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: a60d41f27962a1e803067c8172b3e388a31ba601
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000016"
---
# <span data-ttu-id="c1b87-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c1b87-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="c1b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b87-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b87-103">리소스 이동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="c1b87-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1b87-104">SYNTAX</span></span>

### <span data-ttu-id="c1b87-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="c1b87-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c1b87-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="c1b87-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c1b87-107">설명</span><span class="sxs-lookup"><span data-stu-id="c1b87-107">DESCRIPTION</span></span>
<span data-ttu-id="c1b87-108">리소스 이동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="c1b87-109">예제</span><span class="sxs-lookup"><span data-stu-id="c1b87-109">EXAMPLES</span></span>

### <span data-ttu-id="c1b87-110">예제 1: 이동 컬렉션의 모든 리소스에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS"         

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkInterfaces/psdemov
                                    m111, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/PSDemoVM
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : PSDemoVM
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-
                                    vnet, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroup
                                    s/psdemovm-nsg, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemovm111
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemovm111
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm
                                    111
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemorm-vnet
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemorm-vnet
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualNetworkResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-v
                                    net
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualNetworkResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemovm-nsg
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemovm-nsg
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkSecurityGroupResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psde
                                    movm-nsg
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkSecurityGroupResourceSettings
TargetId                          : 
Type                              : 

DependsOn                         : {}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM-target
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemorm
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : DeleteSourcePending
Name                              : psdemorm
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.ResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.ResourceSettings
TargetId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM-target
Type                              :

```

<span data-ttu-id="c1b87-111">이동 컬렉션의 모든 리소스에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="c1b87-112">예제 2: 이동 리소스 이름을 사용하여 이동 컬렉션에서 특정 리소스에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PSDemoVM"   
                                                     
DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkInterfaces/psdemov
                                    m111, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/PSDemoRM}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS/moveResources/PSDemoVM
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : PSDemoVM
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.VirtualMachineResourceSettings
TargetId                          : 
Type                              : 

```

<span data-ttu-id="c1b87-113">이동 리소스 이름을 사용하여 이동 컬렉션에서 특정 리소스에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="c1b87-114">예제 3:SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState와 같은 필터를 사용하여 이동 컬렉션에서 특정 리소스에 대한 세부 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzResourceMoverMoveResource -MoveCollectionName "PS-centralus-westcentralus-demoRMS1" -ResourceGroupName "RG-MoveCollection-demoRMS" -Filter "Properties/SourceResourceName eq 'psdemovm111'"


DependsOn                         : {/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-
                                    vnet, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroup
                                    s/psdemovm-nsg, /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm}
DependsOnOverride                 : {}
ErrorsPropertiesCode              : 
ErrorsPropertiesDetail            : 
ErrorsPropertiesMessage           : 
ErrorsPropertiesTarget            : 
ExistingTargetId                  : 
Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveColle
                                    ctions/PS-centralus-westcentralus-demoRMS1/moveResources/psdemovm111
IsResolveRequired                 : False
JobStatusJobName                  : 
JobStatusJobProgress              : 
MoveStatusErrorsPropertiesCode    : 
MoveStatusErrorsPropertiesDetail  : 
MoveStatusErrorsPropertiesMessage : 
MoveStatusErrorsPropertiesTarget  : 
MoveStatusMoveState               : PreparePending
Name                              : psdemovm111
ProvisioningState                 : Succeeded
ResourceSetting                   : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
SourceId                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm
                                    111
SourceResourceSetting             : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.NetworkInterfaceResourceSettings
TargetId                          : 
Type                              : 

```

<span data-ttu-id="c1b87-115">armid, moveStatusMoveState(확인) 등 필터를 사용하여 이동 컬렉션에서 특정 리소스에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="c1b87-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c1b87-116">PARAMETERS</span></span>

### <span data-ttu-id="c1b87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b87-117">-DefaultProfile</span></span>
<span data-ttu-id="c1b87-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b87-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="c1b87-119">-Filter</span></span>
<span data-ttu-id="c1b87-120">작업에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="c1b87-121">예를 들어 $filter=Properties/ProvisioningState eq 'Succeeded'를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b87-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c1b87-122">-MoveCollectionName</span></span>
<span data-ttu-id="c1b87-123">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c1b87-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c1b87-124">-Name</span></span>
<span data-ttu-id="c1b87-125">리소스 이름 이동.</span><span class="sxs-lookup"><span data-stu-id="c1b87-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b87-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1b87-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c1b87-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1b87-128">-SubscriptionId</span></span>
<span data-ttu-id="c1b87-129">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-129">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b87-130">CommonParameters</span></span>
<span data-ttu-id="c1b87-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b87-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1b87-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b87-133">입력</span><span class="sxs-lookup"><span data-stu-id="c1b87-133">INPUTS</span></span>

## <span data-ttu-id="c1b87-134">출력</span><span class="sxs-lookup"><span data-stu-id="c1b87-134">OUTPUTS</span></span>

### <span data-ttu-id="c1b87-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="c1b87-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveResource</span></span>

## <span data-ttu-id="c1b87-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1b87-136">NOTES</span></span>

<span data-ttu-id="c1b87-137">별칭</span><span class="sxs-lookup"><span data-stu-id="c1b87-137">ALIASES</span></span>

## <span data-ttu-id="c1b87-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1b87-138">RELATED LINKS</span></span>

