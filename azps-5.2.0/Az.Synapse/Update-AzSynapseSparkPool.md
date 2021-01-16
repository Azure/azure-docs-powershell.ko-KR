---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356342"
---
# <span data-ttu-id="bdde6-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="bdde6-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="bdde6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdde6-102">SYNOPSIS</span></span>
<span data-ttu-id="bdde6-103">Synapse Analytics Spark 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="bdde6-104">구문</span><span class="sxs-lookup"><span data-stu-id="bdde6-104">SYNTAX</span></span>

### <span data-ttu-id="bdde6-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bdde6-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdde6-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdde6-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdde6-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdde6-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdde6-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdde6-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdde6-109">설명</span><span class="sxs-lookup"><span data-stu-id="bdde6-109">DESCRIPTION</span></span>
<span data-ttu-id="bdde6-110">**Update-AzSynapseSparkPool** cmdlet은 Azure Synapse Analytics Spark 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="bdde6-111">예제</span><span class="sxs-lookup"><span data-stu-id="bdde6-111">EXAMPLES</span></span>

### <span data-ttu-id="bdde6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bdde6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="bdde6-113">이 명령은 Azure Synapse Analytics Spark 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="bdde6-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bdde6-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="bdde6-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="bdde6-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bdde6-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="bdde6-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="bdde6-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="bdde6-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="bdde6-119">이 명령은 리소스 ID로 Azure Synapse Analytics Spark 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="bdde6-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="bdde6-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="bdde6-121">이 명령을 사용하면 Azure Synapse Analytics Spark 풀에 대해 자동 크기 조정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="bdde6-122">예제 6</span><span class="sxs-lookup"><span data-stu-id="bdde6-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="bdde6-123">이 명령은 Azure Synapse Analytics Spark 풀에 대한 자동 크기 조정을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="bdde6-124">예제 7</span><span class="sxs-lookup"><span data-stu-id="bdde6-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="bdde6-125">이 명령을 사용하면 Azure Synapse Analytics Spark 풀에 대해 자동 일시 중지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="bdde6-126">예제 8</span><span class="sxs-lookup"><span data-stu-id="bdde6-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="bdde6-127">이 명령은 Azure Synapse Analytics Spark 풀에 대한 자동 일시 중지를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="bdde6-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdde6-128">PARAMETERS</span></span>

### <span data-ttu-id="bdde6-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdde6-129">-AsJob</span></span>
<span data-ttu-id="bdde6-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bdde6-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdde6-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="bdde6-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="bdde6-132">유휴 시간(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-132">Number of minutes idle.</span></span> <span data-ttu-id="bdde6-133">자동 일시 중지를 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="bdde6-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="bdde6-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="bdde6-135">지정된 Spark 풀에 할당할 노드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="bdde6-136">자동 크기 조정을 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="bdde6-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="bdde6-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="bdde6-138">지정된 Spark 풀에 할당할 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="bdde6-139">자동 크기 조정을 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="bdde6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdde6-140">-DefaultProfile</span></span>
<span data-ttu-id="bdde6-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdde6-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="bdde6-142">-EnableAutoPause</span></span>
<span data-ttu-id="bdde6-143">자동 일시 중지를 사용하도록 설정해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="bdde6-144">-EnableAutoScale</span></span>
<span data-ttu-id="bdde6-145">자동 크기 조정을 사용하도록 설정해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdde6-146">-InputObject</span></span>
<span data-ttu-id="bdde6-147">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="bdde6-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="bdde6-149">환경 구성 파일("PIP 고정" 출력).</span><span class="sxs-lookup"><span data-stu-id="bdde6-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="bdde6-150">-Name</span><span class="sxs-lookup"><span data-stu-id="bdde6-150">-Name</span></span>
<span data-ttu-id="bdde6-151">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="bdde6-152">-NodeCount</span></span>
<span data-ttu-id="bdde6-153">지정된 Spark 풀에 할당할 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="bdde6-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="bdde6-154">-NodeSize</span></span>
<span data-ttu-id="bdde6-155">지정된 Spark 풀에 할당된 노드에 사용할 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="bdde6-156">자동 크기 조정을 사용할 수 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdde6-157">-ResourceGroupName</span></span>
<span data-ttu-id="bdde6-158">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdde6-159">-ResourceId</span></span>
<span data-ttu-id="bdde6-160">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="bdde6-161">-SparkVersion</span></span>
<span data-ttu-id="bdde6-162">Apache Spark 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-162">Apache Spark version.</span></span>
<span data-ttu-id="bdde6-163">허용되는 값: 2.4</span><span class="sxs-lookup"><span data-stu-id="bdde6-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="bdde6-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="bdde6-164">-Tag</span></span>
<span data-ttu-id="bdde6-165">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="bdde6-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bdde6-166">-WorkspaceName</span></span>
<span data-ttu-id="bdde6-167">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bdde6-168">-WorkspaceObject</span></span>
<span data-ttu-id="bdde6-169">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdde6-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdde6-170">-Confirm</span></span>
<span data-ttu-id="bdde6-171">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdde6-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdde6-172">-WhatIf</span></span>
<span data-ttu-id="bdde6-173">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bdde6-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdde6-174">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdde6-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdde6-175">CommonParameters</span></span>
<span data-ttu-id="bdde6-176">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bdde6-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdde6-177">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bdde6-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdde6-178">입력</span><span class="sxs-lookup"><span data-stu-id="bdde6-178">INPUTS</span></span>

### <span data-ttu-id="bdde6-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bdde6-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bdde6-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="bdde6-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="bdde6-181">출력</span><span class="sxs-lookup"><span data-stu-id="bdde6-181">OUTPUTS</span></span>

### <span data-ttu-id="bdde6-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="bdde6-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="bdde6-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bdde6-183">NOTES</span></span>

## <span data-ttu-id="bdde6-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdde6-184">RELATED LINKS</span></span>
