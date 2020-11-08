---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218220"
---
# <span data-ttu-id="af82f-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="af82f-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="af82f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af82f-102">SYNOPSIS</span></span>
<span data-ttu-id="af82f-103">이동 모음에서 이동 리소스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="af82f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af82f-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af82f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="af82f-105">DESCRIPTION</span></span>
<span data-ttu-id="af82f-106">이동 모음에서 이동 리소스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="af82f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="af82f-107">EXAMPLES</span></span>

### <span data-ttu-id="af82f-108">예제 1: move collection에 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-108">Example 1: Adding a resource to the move collection.</span></span>
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

<span data-ttu-id="af82f-109">지정 된 구독 내의 이동 모음에 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="af82f-110">변수</span><span class="sxs-lookup"><span data-stu-id="af82f-110">PARAMETERS</span></span>

### <span data-ttu-id="af82f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af82f-111">-AsJob</span></span>
<span data-ttu-id="af82f-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="af82f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="af82f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af82f-113">-DefaultProfile</span></span>
<span data-ttu-id="af82f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af82f-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="af82f-115">-DependsOnOverride</span></span>
<span data-ttu-id="af82f-116">리소스 종속성 이동 재정의를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="af82f-117">생성 하려면 DEPENDSONOVERRIDE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="af82f-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="af82f-118">-ExistingTargetId</span></span>
<span data-ttu-id="af82f-119">리소스의 기존 대상 팔 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="af82f-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="af82f-120">-MoveCollectionName</span></span>
<span data-ttu-id="af82f-121">이동 컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="af82f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="af82f-122">-Name</span></span>
<span data-ttu-id="af82f-123">이동 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-123">The Move Resource Name.</span></span>

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

### <span data-ttu-id="af82f-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af82f-124">-NoWait</span></span>
<span data-ttu-id="af82f-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="af82f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af82f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af82f-126">-ResourceGroupName</span></span>
<span data-ttu-id="af82f-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="af82f-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="af82f-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="af82f-129">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-129">The resource type.</span></span>
<span data-ttu-id="af82f-130">예를 들어 값은 Microsoft. Compute/virtualMachines 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="af82f-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="af82f-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="af82f-132">대상 리소스 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="af82f-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="af82f-133">-SourceId</span></span>
<span data-ttu-id="af82f-134">리소스의 소스 팔 Id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="af82f-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="af82f-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="af82f-136">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-136">The resource type.</span></span>
<span data-ttu-id="af82f-137">예를 들어 값은 Microsoft. Compute/virtualMachines 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="af82f-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="af82f-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="af82f-139">대상 리소스 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="af82f-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af82f-140">-SubscriptionId</span></span>
<span data-ttu-id="af82f-141">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="af82f-142">-확인</span><span class="sxs-lookup"><span data-stu-id="af82f-142">-Confirm</span></span>
<span data-ttu-id="af82f-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af82f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af82f-144">-WhatIf</span></span>
<span data-ttu-id="af82f-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af82f-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af82f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af82f-147">CommonParameters</span></span>
<span data-ttu-id="af82f-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af82f-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af82f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af82f-150">입력</span><span class="sxs-lookup"><span data-stu-id="af82f-150">INPUTS</span></span>

## <span data-ttu-id="af82f-151">출력</span><span class="sxs-lookup"><span data-stu-id="af82f-151">OUTPUTS</span></span>

### <span data-ttu-id="af82f-152">Api20191001Preview. IMoveResource에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="af82f-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="af82f-153">상속자</span><span class="sxs-lookup"><span data-stu-id="af82f-153">NOTES</span></span>

<span data-ttu-id="af82f-154">별칭과</span><span class="sxs-lookup"><span data-stu-id="af82f-154">ALIASES</span></span>

<span data-ttu-id="af82f-155">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="af82f-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af82f-156">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af82f-157">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="af82f-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af82f-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: 리소스 종속성 이동 재정의를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="af82f-159">`[Id <String>]`: 종속 리소스의 ARM ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="af82f-160">`[TargetId <String>]`: 종속 리소스에 대 한 MoveResource 또는 리소스 ARM ID 중 하나의 리소스 팔 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af82f-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="af82f-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af82f-161">RELATED LINKS</span></span>

