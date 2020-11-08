---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047809"
---
# <span data-ttu-id="15195-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="15195-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="15195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15195-102">SYNOPSIS</span></span>
<span data-ttu-id="15195-103">작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-103">Deletes the workspace.</span></span>

## <span data-ttu-id="15195-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15195-104">SYNTAX</span></span>

### <span data-ttu-id="15195-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="15195-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15195-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15195-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15195-107">설명은</span><span class="sxs-lookup"><span data-stu-id="15195-107">DESCRIPTION</span></span>
<span data-ttu-id="15195-108">작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-108">Deletes the workspace.</span></span>

## <span data-ttu-id="15195-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15195-109">EXAMPLES</span></span>

### <span data-ttu-id="15195-110">예제 1: Databricks 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="15195-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="15195-111">이 명령은 리소스 그룹에서 Databricks 작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="15195-112">예제 2: Databricks 작업 영역을 개체 별로 제거</span><span class="sxs-lookup"><span data-stu-id="15195-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="15195-113">이 명령은 리소스 그룹에서 Databricks 작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="15195-114">변수</span><span class="sxs-lookup"><span data-stu-id="15195-114">PARAMETERS</span></span>

### <span data-ttu-id="15195-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15195-115">-AsJob</span></span>
<span data-ttu-id="15195-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="15195-116">Run the command as a job</span></span>

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

### <span data-ttu-id="15195-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15195-117">-DefaultProfile</span></span>
<span data-ttu-id="15195-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15195-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15195-119">-InputObject</span></span>
<span data-ttu-id="15195-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15195-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15195-121">-이름</span><span class="sxs-lookup"><span data-stu-id="15195-121">-Name</span></span>
<span data-ttu-id="15195-122">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="15195-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15195-123">-NoWait</span></span>
<span data-ttu-id="15195-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="15195-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15195-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15195-125">-PassThru</span></span>
<span data-ttu-id="15195-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15195-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15195-127">-ResourceGroupName</span></span>
<span data-ttu-id="15195-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-128">The name of the resource group.</span></span>
<span data-ttu-id="15195-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15195-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15195-130">-SubscriptionId</span></span>
<span data-ttu-id="15195-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15195-132">-확인</span><span class="sxs-lookup"><span data-stu-id="15195-132">-Confirm</span></span>
<span data-ttu-id="15195-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15195-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15195-134">-WhatIf</span></span>
<span data-ttu-id="15195-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15195-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15195-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15195-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15195-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15195-137">CommonParameters</span></span>
<span data-ttu-id="15195-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15195-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15195-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15195-140">입력</span><span class="sxs-lookup"><span data-stu-id="15195-140">INPUTS</span></span>

### <span data-ttu-id="15195-141">Databricks. IDatabricksIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="15195-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="15195-142">출력</span><span class="sxs-lookup"><span data-stu-id="15195-142">OUTPUTS</span></span>

### <span data-ttu-id="15195-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="15195-143">System.Boolean</span></span>

## <span data-ttu-id="15195-144">상속자</span><span class="sxs-lookup"><span data-stu-id="15195-144">NOTES</span></span>

<span data-ttu-id="15195-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="15195-145">ALIASES</span></span>

<span data-ttu-id="15195-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="15195-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15195-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15195-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="15195-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15195-149">INPUTOBJECT <IDatabricksIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="15195-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15195-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="15195-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15195-151">`[PeeringName <String>]`: 작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="15195-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15195-153">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="15195-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="15195-154">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15195-155">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15195-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="15195-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15195-156">RELATED LINKS</span></span>

