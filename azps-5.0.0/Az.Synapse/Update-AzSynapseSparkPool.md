---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218453"
---
# <span data-ttu-id="86616-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="86616-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="86616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86616-102">SYNOPSIS</span></span>
<span data-ttu-id="86616-103">Synapse Analytics Spark 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="86616-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86616-104">SYNTAX</span></span>

### <span data-ttu-id="86616-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="86616-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86616-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86616-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86616-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86616-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86616-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86616-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86616-109">설명은</span><span class="sxs-lookup"><span data-stu-id="86616-109">DESCRIPTION</span></span>
<span data-ttu-id="86616-110">**업데이트 AzSynapseSparkPool** Cmdlet은 Azure Synapse Analytics Spark 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="86616-111">예제의</span><span class="sxs-lookup"><span data-stu-id="86616-111">EXAMPLES</span></span>

### <span data-ttu-id="86616-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="86616-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="86616-113">이 명령은 Azure Synapse Analytics Spark 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="86616-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="86616-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="86616-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="86616-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="86616-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="86616-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="86616-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="86616-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="86616-119">이 명령은 리소스 ID를 사용 하 여 Azure Synapse Analytics Spark 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="86616-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="86616-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="86616-121">이 명령은 Azure Synapse Analytics Spark 풀에 대 한 자동 크기 조정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="86616-122">예제 6</span><span class="sxs-lookup"><span data-stu-id="86616-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="86616-123">이 명령은 Azure Synapse Analytics Spark 풀에 대 한 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="86616-124">예제 7</span><span class="sxs-lookup"><span data-stu-id="86616-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="86616-125">이 명령은 Azure Synapse Analytics Spark 풀에 대 한 자동 일시 중지를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="86616-126">예제 8</span><span class="sxs-lookup"><span data-stu-id="86616-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="86616-127">이 명령은 Azure Synapse Analytics Spark 풀에 대 한 자동 일시 중지를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="86616-128">변수</span><span class="sxs-lookup"><span data-stu-id="86616-128">PARAMETERS</span></span>

### <span data-ttu-id="86616-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86616-129">-AsJob</span></span>
<span data-ttu-id="86616-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="86616-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86616-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="86616-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="86616-132">유휴 상태인 분 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-132">Number of minutes idle.</span></span> <span data-ttu-id="86616-133">자동 일시 정지가 설정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="86616-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="86616-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="86616-135">지정 된 Spark 풀에 할당할 최대 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="86616-136">자동 크기 조정을 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="86616-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="86616-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="86616-138">지정 된 Spark 풀에 할당할 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="86616-139">자동 크기 조정을 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="86616-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86616-140">-DefaultProfile</span></span>
<span data-ttu-id="86616-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86616-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="86616-142">-EnableAutoPause</span></span>
<span data-ttu-id="86616-143">자동 일시 중지를 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86616-143">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="86616-144">-EnableAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="86616-144">-EnableAutoScale</span></span>
<span data-ttu-id="86616-145">자동 크기 조정을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86616-145">Indicates whether Auto-scale should be enabled</span></span>

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

### <span data-ttu-id="86616-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86616-146">-InputObject</span></span>
<span data-ttu-id="86616-147">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-147">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="86616-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="86616-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="86616-149">환경 구성 파일 ("주사위 멈춤" 출력).</span><span class="sxs-lookup"><span data-stu-id="86616-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="86616-150">-이름</span><span class="sxs-lookup"><span data-stu-id="86616-150">-Name</span></span>
<span data-ttu-id="86616-151">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-151">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="86616-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="86616-152">-NodeCount</span></span>
<span data-ttu-id="86616-153">지정 된 Spark 풀에 할당할 노드의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="86616-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="86616-154">-NodeSize</span></span>
<span data-ttu-id="86616-155">지정 된 Spark 풀에 할당 된 노드에 사용할 코어 및 메모리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="86616-156">자동 크기 조정을 사용 하지 않는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-156">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="86616-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86616-157">-ResourceGroupName</span></span>
<span data-ttu-id="86616-158">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-158">Resource group name.</span></span>

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

### <span data-ttu-id="86616-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86616-159">-ResourceId</span></span>
<span data-ttu-id="86616-160">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-160">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="86616-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="86616-161">-SparkVersion</span></span>
<span data-ttu-id="86616-162">Apache Spark 버전.</span><span class="sxs-lookup"><span data-stu-id="86616-162">Apache Spark version.</span></span>
<span data-ttu-id="86616-163">허용 되는 값: 2.4</span><span class="sxs-lookup"><span data-stu-id="86616-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="86616-164">태그</span><span class="sxs-lookup"><span data-stu-id="86616-164">-Tag</span></span>
<span data-ttu-id="86616-165">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="86616-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="86616-166">-WorkspaceName</span></span>
<span data-ttu-id="86616-167">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-167">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="86616-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="86616-168">-WorkspaceObject</span></span>
<span data-ttu-id="86616-169">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="86616-169">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="86616-170">-확인</span><span class="sxs-lookup"><span data-stu-id="86616-170">-Confirm</span></span>
<span data-ttu-id="86616-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86616-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86616-172">-WhatIf</span></span>
<span data-ttu-id="86616-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="86616-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86616-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86616-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86616-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86616-175">CommonParameters</span></span>
<span data-ttu-id="86616-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86616-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86616-177">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86616-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86616-178">입력</span><span class="sxs-lookup"><span data-stu-id="86616-178">INPUTS</span></span>

### <span data-ttu-id="86616-179">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="86616-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="86616-180">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="86616-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="86616-181">출력</span><span class="sxs-lookup"><span data-stu-id="86616-181">OUTPUTS</span></span>

### <span data-ttu-id="86616-182">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="86616-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="86616-183">상속자</span><span class="sxs-lookup"><span data-stu-id="86616-183">NOTES</span></span>

## <span data-ttu-id="86616-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86616-184">RELATED LINKS</span></span>
