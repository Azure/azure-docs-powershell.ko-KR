---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959952"
---
# <span data-ttu-id="07087-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="07087-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="07087-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07087-102">SYNOPSIS</span></span>
<span data-ttu-id="07087-103">Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07087-104">구문</span><span class="sxs-lookup"><span data-stu-id="07087-104">SYNTAX</span></span>

### <span data-ttu-id="07087-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="07087-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07087-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07087-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07087-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07087-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07087-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07087-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07087-109">설명</span><span class="sxs-lookup"><span data-stu-id="07087-109">DESCRIPTION</span></span>
<span data-ttu-id="07087-110">**Update-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07087-111">예제</span><span class="sxs-lookup"><span data-stu-id="07087-111">EXAMPLES</span></span>

### <span data-ttu-id="07087-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="07087-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="07087-113">이 명령은 Azure Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="07087-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="07087-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="07087-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="07087-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="07087-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="07087-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="07087-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="07087-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="07087-119">이 명령은 리소스 ID를 사용하여 Azure Synapse Analytics SQL 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="07087-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="07087-120">PARAMETERS</span></span>

### <span data-ttu-id="07087-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07087-121">-AsJob</span></span>
<span data-ttu-id="07087-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="07087-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07087-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07087-123">-DefaultProfile</span></span>
<span data-ttu-id="07087-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07087-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07087-125">-InputObject</span></span>
<span data-ttu-id="07087-126">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="07087-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07087-127">-Name</span><span class="sxs-lookup"><span data-stu-id="07087-127">-Name</span></span>
<span data-ttu-id="07087-128">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07087-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07087-129">-PassThru</span></span>
<span data-ttu-id="07087-130">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07087-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="07087-131">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="07087-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="07087-132">-PerformanceLevel</span></span>
<span data-ttu-id="07087-133">SQL 풀에 할당할 서비스 계층 및 SQL 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="07087-134">예를 들어 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="07087-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="07087-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07087-135">-ResourceGroupName</span></span>
<span data-ttu-id="07087-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07087-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07087-137">-ResourceId</span></span>
<span data-ttu-id="07087-138">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07087-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="07087-139">-Tag</span></span>
<span data-ttu-id="07087-140">문자열, 리소스와 연결된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07087-141">-Version</span><span class="sxs-lookup"><span data-stu-id="07087-141">-Version</span></span>
<span data-ttu-id="07087-142">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="07087-143">예를 들어 2 또는 3.</span><span class="sxs-lookup"><span data-stu-id="07087-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="07087-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07087-144">-WorkspaceName</span></span>
<span data-ttu-id="07087-145">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07087-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07087-146">-WorkspaceObject</span></span>
<span data-ttu-id="07087-147">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07087-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07087-148">-확인</span><span class="sxs-lookup"><span data-stu-id="07087-148">-Confirm</span></span>
<span data-ttu-id="07087-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07087-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07087-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07087-150">-WhatIf</span></span>
<span data-ttu-id="07087-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="07087-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07087-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07087-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07087-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07087-153">CommonParameters</span></span>
<span data-ttu-id="07087-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07087-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07087-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07087-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07087-156">입력</span><span class="sxs-lookup"><span data-stu-id="07087-156">INPUTS</span></span>

### <span data-ttu-id="07087-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07087-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="07087-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="07087-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="07087-159">출력</span><span class="sxs-lookup"><span data-stu-id="07087-159">OUTPUTS</span></span>

### <span data-ttu-id="07087-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="07087-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="07087-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07087-161">NOTES</span></span>

## <span data-ttu-id="07087-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07087-162">RELATED LINKS</span></span>
