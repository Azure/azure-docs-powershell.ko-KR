---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494614"
---
# <span data-ttu-id="d642b-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d642b-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d642b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d642b-102">SYNOPSIS</span></span>
<span data-ttu-id="d642b-103">작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-103">Deletes the workspace.</span></span>

## <span data-ttu-id="d642b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d642b-104">SYNTAX</span></span>

### <span data-ttu-id="d642b-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="d642b-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d642b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d642b-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d642b-107">설명</span><span class="sxs-lookup"><span data-stu-id="d642b-107">DESCRIPTION</span></span>
<span data-ttu-id="d642b-108">작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-108">Deletes the workspace.</span></span>

## <span data-ttu-id="d642b-109">예제</span><span class="sxs-lookup"><span data-stu-id="d642b-109">EXAMPLES</span></span>

### <span data-ttu-id="d642b-110">예제 1: Databricks 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="d642b-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="d642b-111">이 명령은 리소스 그룹에서 Databricks 작업 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="d642b-112">예제 2: 개체에 따라 Databricks 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="d642b-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="d642b-113">이 명령은 리소스 그룹에서 Databricks 작업 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="d642b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d642b-114">PARAMETERS</span></span>

### <span data-ttu-id="d642b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d642b-115">-AsJob</span></span>
<span data-ttu-id="d642b-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d642b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d642b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d642b-117">-DefaultProfile</span></span>
<span data-ttu-id="d642b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d642b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d642b-119">-InputObject</span></span>
<span data-ttu-id="d642b-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d642b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d642b-121">-Name</span></span>
<span data-ttu-id="d642b-122">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d642b-123">-NoWait</span></span>
<span data-ttu-id="d642b-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="d642b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d642b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d642b-125">-PassThru</span></span>
<span data-ttu-id="d642b-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d642b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d642b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d642b-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-128">The name of the resource group.</span></span>
<span data-ttu-id="d642b-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d642b-130">-SubscriptionId</span></span>
<span data-ttu-id="d642b-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d642b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d642b-132">-Confirm</span></span>
<span data-ttu-id="d642b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d642b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d642b-134">-WhatIf</span></span>
<span data-ttu-id="d642b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d642b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d642b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d642b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d642b-137">CommonParameters</span></span>
<span data-ttu-id="d642b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d642b-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d642b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d642b-140">입력</span><span class="sxs-lookup"><span data-stu-id="d642b-140">INPUTS</span></span>

### <span data-ttu-id="d642b-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d642b-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d642b-142">출력</span><span class="sxs-lookup"><span data-stu-id="d642b-142">OUTPUTS</span></span>

### <span data-ttu-id="d642b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d642b-143">System.Boolean</span></span>

## <span data-ttu-id="d642b-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d642b-144">NOTES</span></span>

<span data-ttu-id="d642b-145">별칭</span><span class="sxs-lookup"><span data-stu-id="d642b-145">ALIASES</span></span>

<span data-ttu-id="d642b-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d642b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d642b-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d642b-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d642b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d642b-149">INPUTOBJECT: <IDatabricksIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d642b-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d642b-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d642b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d642b-151">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d642b-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d642b-153">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d642b-154">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d642b-155">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d642b-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d642b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d642b-156">RELATED LINKS</span></span>

