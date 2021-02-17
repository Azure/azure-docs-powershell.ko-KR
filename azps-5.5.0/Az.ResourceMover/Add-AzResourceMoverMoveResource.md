---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208557"
---
# <span data-ttu-id="04a79-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="04a79-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="04a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a79-102">SYNOPSIS</span></span>
<span data-ttu-id="04a79-103">이동 컬렉션에서 이동 리소스를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="04a79-104">구문</span><span class="sxs-lookup"><span data-stu-id="04a79-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04a79-105">설명</span><span class="sxs-lookup"><span data-stu-id="04a79-105">DESCRIPTION</span></span>
<span data-ttu-id="04a79-106">이동 컬렉션에서 이동 리소스를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="04a79-107">예제</span><span class="sxs-lookup"><span data-stu-id="04a79-107">EXAMPLES</span></span>

### <span data-ttu-id="04a79-108">예제 1: 이동 컬렉션에 리소스 추가</span><span class="sxs-lookup"><span data-stu-id="04a79-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="04a79-109">지정된 구독 내에서 이동 컬렉션에 리소스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="04a79-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04a79-110">PARAMETERS</span></span>

### <span data-ttu-id="04a79-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04a79-111">-AsJob</span></span>
<span data-ttu-id="04a79-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="04a79-112">Run the command as a job</span></span>

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

### <span data-ttu-id="04a79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a79-113">-DefaultProfile</span></span>
<span data-ttu-id="04a79-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a79-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="04a79-115">-DependsOnOverride</span></span>
<span data-ttu-id="04a79-116">이동 리소스 종속성 오버라이드를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="04a79-117">생성을 위해 DEPENDSONOVERRIDE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="04a79-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a79-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="04a79-118">-ExistingTargetId</span></span>
<span data-ttu-id="04a79-119">리소스의 기존 대상 ARM ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="04a79-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="04a79-120">-MoveCollectionName</span></span>
<span data-ttu-id="04a79-121">컬렉션 이동 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="04a79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="04a79-122">-Name</span></span>
<span data-ttu-id="04a79-123">리소스 이름 이동</span><span class="sxs-lookup"><span data-stu-id="04a79-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a79-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04a79-124">-NoWait</span></span>
<span data-ttu-id="04a79-125">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="04a79-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04a79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a79-126">-ResourceGroupName</span></span>
<span data-ttu-id="04a79-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="04a79-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="04a79-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="04a79-129">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-129">The resource type.</span></span>
<span data-ttu-id="04a79-130">예를 들어 이 값은 Microsoft.Compute/virtualMachines일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="04a79-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="04a79-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="04a79-132">대상 리소스 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="04a79-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="04a79-133">-SourceId</span></span>
<span data-ttu-id="04a79-134">리소스의 원본 ARM 또는 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="04a79-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="04a79-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="04a79-136">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-136">The resource type.</span></span>
<span data-ttu-id="04a79-137">예를 들어 이 값은 Microsoft.Compute/virtualMachines일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="04a79-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="04a79-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="04a79-139">대상 리소스 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="04a79-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04a79-140">-SubscriptionId</span></span>
<span data-ttu-id="04a79-141">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-141">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a79-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04a79-142">-Confirm</span></span>
<span data-ttu-id="04a79-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a79-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a79-144">-WhatIf</span></span>
<span data-ttu-id="04a79-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="04a79-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a79-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a79-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a79-147">CommonParameters</span></span>
<span data-ttu-id="04a79-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a79-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04a79-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a79-150">입력</span><span class="sxs-lookup"><span data-stu-id="04a79-150">INPUTS</span></span>

## <span data-ttu-id="04a79-151">출력</span><span class="sxs-lookup"><span data-stu-id="04a79-151">OUTPUTS</span></span>

### <span data-ttu-id="04a79-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="04a79-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="04a79-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04a79-153">NOTES</span></span>

<span data-ttu-id="04a79-154">별칭</span><span class="sxs-lookup"><span data-stu-id="04a79-154">ALIASES</span></span>

<span data-ttu-id="04a79-155">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="04a79-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04a79-156">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04a79-157">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="04a79-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04a79-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: 이동 리소스 종속성 오버라이드를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="04a79-159">`[Id <String>]`: 종속 리소스의 ARM ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="04a79-160">`[TargetId <String>]`: MoveResource 또는 ARM 리소스 ID의 리소스 ARM ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="04a79-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="04a79-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04a79-161">RELATED LINKS</span></span>

