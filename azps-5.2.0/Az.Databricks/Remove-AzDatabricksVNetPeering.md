---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338685"
---
# <span data-ttu-id="0d950-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="0d950-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="0d950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d950-102">SYNOPSIS</span></span>
<span data-ttu-id="0d950-103">작업 영역 vNetPeering을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="0d950-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d950-104">SYNTAX</span></span>

### <span data-ttu-id="0d950-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="0d950-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0d950-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d950-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d950-107">설명</span><span class="sxs-lookup"><span data-stu-id="0d950-107">DESCRIPTION</span></span>
<span data-ttu-id="0d950-108">작업 영역 vNetPeering을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="0d950-109">예제</span><span class="sxs-lookup"><span data-stu-id="0d950-109">EXAMPLES</span></span>

### <span data-ttu-id="0d950-110">예제 1: 이름으로 databricks의 vnet 피어링 제거</span><span class="sxs-lookup"><span data-stu-id="0d950-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="0d950-111">이 명령은 이름으로 databricks의 vnet 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="0d950-112">예제 2: 개체에 의해 databricks의 vnet 피어링 제거</span><span class="sxs-lookup"><span data-stu-id="0d950-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="0d950-113">이 명령은 개체에 의해 databricks의 vnet 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="0d950-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d950-114">PARAMETERS</span></span>

### <span data-ttu-id="0d950-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d950-115">-AsJob</span></span>
<span data-ttu-id="0d950-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="0d950-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0d950-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d950-117">-DefaultProfile</span></span>
<span data-ttu-id="0d950-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d950-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d950-119">-InputObject</span></span>
<span data-ttu-id="0d950-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0d950-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d950-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0d950-121">-Name</span></span>
<span data-ttu-id="0d950-122">작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="0d950-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0d950-123">-NoWait</span></span>
<span data-ttu-id="0d950-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="0d950-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d950-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d950-125">-PassThru</span></span>
<span data-ttu-id="0d950-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0d950-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d950-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d950-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-128">The name of the resource group.</span></span>
<span data-ttu-id="0d950-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d950-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d950-130">-SubscriptionId</span></span>
<span data-ttu-id="0d950-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0d950-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d950-132">-WorkspaceName</span></span>
<span data-ttu-id="0d950-133">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="0d950-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d950-134">-Confirm</span></span>
<span data-ttu-id="0d950-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d950-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d950-136">-WhatIf</span></span>
<span data-ttu-id="0d950-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d950-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d950-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d950-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d950-139">CommonParameters</span></span>
<span data-ttu-id="0d950-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d950-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d950-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d950-142">입력</span><span class="sxs-lookup"><span data-stu-id="0d950-142">INPUTS</span></span>

### <span data-ttu-id="0d950-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="0d950-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="0d950-144">출력</span><span class="sxs-lookup"><span data-stu-id="0d950-144">OUTPUTS</span></span>

### <span data-ttu-id="0d950-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d950-145">System.Boolean</span></span>

## <span data-ttu-id="0d950-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d950-146">NOTES</span></span>

<span data-ttu-id="0d950-147">별칭</span><span class="sxs-lookup"><span data-stu-id="0d950-147">ALIASES</span></span>

<span data-ttu-id="0d950-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0d950-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d950-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d950-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d950-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d950-151">INPUTOBJECT: <IDatabricksIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d950-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d950-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0d950-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d950-153">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="0d950-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0d950-155">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="0d950-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0d950-157">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d950-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="0d950-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d950-158">RELATED LINKS</span></span>

