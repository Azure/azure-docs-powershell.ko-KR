---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213457"
---
# <span data-ttu-id="e5f00-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e5f00-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e5f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f00-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f00-103">Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e5f00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5f00-104">SYNTAX</span></span>

### <span data-ttu-id="e5f00-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e5f00-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5f00-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5f00-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f00-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5f00-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f00-117">설명은</span><span class="sxs-lookup"><span data-stu-id="e5f00-117">DESCRIPTION</span></span>
<span data-ttu-id="e5f00-118">**업데이트 AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e5f00-119">예제의</span><span class="sxs-lookup"><span data-stu-id="e5f00-119">EXAMPLES</span></span>

### <span data-ttu-id="e5f00-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5f00-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="e5f00-121">이 명령은 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="e5f00-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="e5f00-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="e5f00-123">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e5f00-124">예제 3</span><span class="sxs-lookup"><span data-stu-id="e5f00-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="e5f00-125">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e5f00-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="e5f00-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="e5f00-127">이 명령은 리소스 ID를 사용 하 여 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="e5f00-128">변수</span><span class="sxs-lookup"><span data-stu-id="e5f00-128">PARAMETERS</span></span>

### <span data-ttu-id="e5f00-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5f00-129">-AsJob</span></span>
<span data-ttu-id="e5f00-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e5f00-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5f00-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f00-131">-DefaultProfile</span></span>
<span data-ttu-id="e5f00-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f00-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5f00-133">-InputObject</span></span>
<span data-ttu-id="e5f00-134">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-135">-이름</span><span class="sxs-lookup"><span data-stu-id="e5f00-135">-Name</span></span>
<span data-ttu-id="e5f00-136">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5f00-137">-PassThru</span></span>
<span data-ttu-id="e5f00-138">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e5f00-139">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e5f00-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="e5f00-140">-PerformanceLevel</span></span>
<span data-ttu-id="e5f00-141">SQL 풀에 할당할 SQL 서비스 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="e5f00-142">예를 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="e5f00-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f00-143">-ResourceGroupName</span></span>
<span data-ttu-id="e5f00-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5f00-145">-ResourceId</span></span>
<span data-ttu-id="e5f00-146">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-147">-Resume</span><span class="sxs-lookup"><span data-stu-id="e5f00-147">-Resume</span></span>
<span data-ttu-id="e5f00-148">SQL 풀을 다시 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-149">-일시 중단</span><span class="sxs-lookup"><span data-stu-id="e5f00-149">-Suspend</span></span>
<span data-ttu-id="e5f00-150">SQL 풀 일시 중지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-151">태그</span><span class="sxs-lookup"><span data-stu-id="e5f00-151">-Tag</span></span>
<span data-ttu-id="e5f00-152">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-153">-버전</span><span class="sxs-lookup"><span data-stu-id="e5f00-153">-Version</span></span>
<span data-ttu-id="e5f00-154">Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e5f00-155">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-155">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5f00-156">-WorkspaceName</span></span>
<span data-ttu-id="e5f00-157">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-158">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e5f00-158">-WorkspaceObject</span></span>
<span data-ttu-id="e5f00-159">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f00-160">-확인</span><span class="sxs-lookup"><span data-stu-id="e5f00-160">-Confirm</span></span>
<span data-ttu-id="e5f00-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f00-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f00-162">-WhatIf</span></span>
<span data-ttu-id="e5f00-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f00-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f00-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f00-165">CommonParameters</span></span>
<span data-ttu-id="e5f00-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f00-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f00-167">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5f00-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f00-168">입력</span><span class="sxs-lookup"><span data-stu-id="e5f00-168">INPUTS</span></span>

### <span data-ttu-id="e5f00-169">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="e5f00-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e5f00-170">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="e5f00-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e5f00-171">출력</span><span class="sxs-lookup"><span data-stu-id="e5f00-171">OUTPUTS</span></span>

### <span data-ttu-id="e5f00-172">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="e5f00-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e5f00-173">상속자</span><span class="sxs-lookup"><span data-stu-id="e5f00-173">NOTES</span></span>

## <span data-ttu-id="e5f00-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5f00-174">RELATED LINKS</span></span>
