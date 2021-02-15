---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197337"
---
# <span data-ttu-id="c3403-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c3403-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="c3403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3403-102">SYNOPSIS</span></span>
<span data-ttu-id="c3403-103">Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c3403-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3403-104">SYNTAX</span></span>

### <span data-ttu-id="c3403-105">CreateByNameAndEnableAutoScaleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c3403-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3403-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3403-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3403-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3403-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3403-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3403-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3403-109">설명</span><span class="sxs-lookup"><span data-stu-id="c3403-109">DESCRIPTION</span></span>
<span data-ttu-id="c3403-110">**New-AzSynapseSparkPool** cmdlet은 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c3403-111">예제</span><span class="sxs-lookup"><span data-stu-id="c3403-111">EXAMPLES</span></span>

### <span data-ttu-id="c3403-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3403-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c3403-113">이 명령은 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c3403-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3403-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c3403-115">이 명령은 자동 크기 조정이 활성화된 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="c3403-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="c3403-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c3403-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="c3403-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="c3403-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c3403-119">이 명령은 파이프라인을 통해 자동 크기 조정이 활성화된 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="c3403-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3403-120">PARAMETERS</span></span>

### <span data-ttu-id="c3403-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3403-121">-AsJob</span></span>
<span data-ttu-id="c3403-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c3403-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3403-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="c3403-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="c3403-124">유휴 시간(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-124">Number of minutes idle.</span></span> <span data-ttu-id="c3403-125">자동 일시 중지를 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="c3403-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="c3403-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="c3403-127">지정된 Spark 풀에 할당할 노드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c3403-128">자동 크기 조정을 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="c3403-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="c3403-130">지정된 Spark 풀에 할당할 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c3403-131">자동 크기 조정을 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3403-132">-DefaultProfile</span></span>
<span data-ttu-id="c3403-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3403-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="c3403-134">-EnableAutoPause</span></span>
<span data-ttu-id="c3403-135">자동 일시 중지를 사용하도록 설정해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="c3403-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="c3403-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="c3403-137">환경 구성 파일("PIP 고정" 출력).</span><span class="sxs-lookup"><span data-stu-id="c3403-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="c3403-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c3403-138">-Name</span></span>
<span data-ttu-id="c3403-139">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c3403-140">-NodeCount</span></span>
<span data-ttu-id="c3403-141">지정된 Spark 풀에 할당할 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c3403-142">-NodeSize</span></span>
<span data-ttu-id="c3403-143">지정된 Spark 풀에 할당된 노드에 사용할 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c3403-144">자동 크기 조정을 사용할 수 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3403-145">-ResourceGroupName</span></span>
<span data-ttu-id="c3403-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="c3403-147">-SparkVersion</span></span>
<span data-ttu-id="c3403-148">Apache Spark 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-148">Apache Spark version.</span></span>
<span data-ttu-id="c3403-149">허용되는 값: 2.4</span><span class="sxs-lookup"><span data-stu-id="c3403-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="c3403-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3403-150">-Tag</span></span>
<span data-ttu-id="c3403-151">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="c3403-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3403-152">-WorkspaceName</span></span>
<span data-ttu-id="c3403-153">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c3403-154">-WorkspaceObject</span></span>
<span data-ttu-id="c3403-155">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3403-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3403-156">-Confirm</span></span>
<span data-ttu-id="c3403-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3403-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3403-158">-WhatIf</span></span>
<span data-ttu-id="c3403-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c3403-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3403-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3403-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3403-161">CommonParameters</span></span>
<span data-ttu-id="c3403-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3403-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3403-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3403-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3403-164">입력</span><span class="sxs-lookup"><span data-stu-id="c3403-164">INPUTS</span></span>

### <span data-ttu-id="c3403-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c3403-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c3403-166">출력</span><span class="sxs-lookup"><span data-stu-id="c3403-166">OUTPUTS</span></span>

### <span data-ttu-id="c3403-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c3403-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c3403-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3403-168">NOTES</span></span>

## <span data-ttu-id="c3403-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3403-169">RELATED LINKS</span></span>
