---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c41c6afdda39843afa985a53eb572b64f8bcfe19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976064"
---
# <span data-ttu-id="c2f85-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c2f85-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="c2f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f85-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f85-103">Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c2f85-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2f85-104">SYNTAX</span></span>

### <span data-ttu-id="c2f85-105">CreateByNameAndEnableAutoScaleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c2f85-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f85-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f85-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f85-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f85-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f85-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2f85-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f85-109">설명</span><span class="sxs-lookup"><span data-stu-id="c2f85-109">DESCRIPTION</span></span>
<span data-ttu-id="c2f85-110">**New-AzSynapseSparkPool** cmdlet은 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c2f85-111">예제</span><span class="sxs-lookup"><span data-stu-id="c2f85-111">EXAMPLES</span></span>

### <span data-ttu-id="c2f85-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2f85-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c2f85-113">이 명령은 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c2f85-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c2f85-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c2f85-115">이 명령은 자동 크기 조정이 사용하도록 설정된 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="c2f85-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="c2f85-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c2f85-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="c2f85-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="c2f85-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="c2f85-119">이 명령은 파이프라인을 통해 자동 크기 조정이 활성화된 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="c2f85-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2f85-120">PARAMETERS</span></span>

### <span data-ttu-id="c2f85-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2f85-121">-AsJob</span></span>
<span data-ttu-id="c2f85-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c2f85-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2f85-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="c2f85-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="c2f85-124">유휴 시간의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-124">Number of minutes idle.</span></span> <span data-ttu-id="c2f85-125">자동 일시 중지를 사용하도록 설정하면 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="c2f85-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="c2f85-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="c2f85-127">지정된 Spark 풀에 할당할 노드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c2f85-128">자동 크기 조정을 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="c2f85-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="c2f85-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="c2f85-130">지정된 Spark 풀에 할당할 노드의 최소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c2f85-131">자동 크기 조정을 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="c2f85-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f85-132">-DefaultProfile</span></span>
<span data-ttu-id="c2f85-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f85-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="c2f85-134">-EnableAutoPause</span></span>
<span data-ttu-id="c2f85-135">자동 일시 중지를 사용하도록 설정해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="c2f85-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="c2f85-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="c2f85-137">환경 구성 파일("PIP 고정" 출력).</span><span class="sxs-lookup"><span data-stu-id="c2f85-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="c2f85-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c2f85-138">-Name</span></span>
<span data-ttu-id="c2f85-139">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c2f85-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c2f85-140">-NodeCount</span></span>
<span data-ttu-id="c2f85-141">지정된 Spark 풀에 할당할 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="c2f85-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c2f85-142">-NodeSize</span></span>
<span data-ttu-id="c2f85-143">지정된 Spark 풀에 할당된 노드에 사용할 코어 및 메모리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c2f85-144">자동 크기 조정을 사용할 수 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="c2f85-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f85-145">-ResourceGroupName</span></span>
<span data-ttu-id="c2f85-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-146">Resource group name.</span></span>

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

### <span data-ttu-id="c2f85-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="c2f85-147">-SparkVersion</span></span>
<span data-ttu-id="c2f85-148">Apache Spark 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-148">Apache Spark version.</span></span>
<span data-ttu-id="c2f85-149">허용 값: 2.4</span><span class="sxs-lookup"><span data-stu-id="c2f85-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="c2f85-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2f85-150">-Tag</span></span>
<span data-ttu-id="c2f85-151">문자열, 리소스와 연결된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="c2f85-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2f85-152">-WorkspaceName</span></span>
<span data-ttu-id="c2f85-153">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c2f85-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2f85-154">-WorkspaceObject</span></span>
<span data-ttu-id="c2f85-155">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c2f85-156">-확인</span><span class="sxs-lookup"><span data-stu-id="c2f85-156">-Confirm</span></span>
<span data-ttu-id="c2f85-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f85-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f85-158">-WhatIf</span></span>
<span data-ttu-id="c2f85-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f85-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f85-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f85-161">CommonParameters</span></span>
<span data-ttu-id="c2f85-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f85-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f85-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2f85-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f85-164">입력</span><span class="sxs-lookup"><span data-stu-id="c2f85-164">INPUTS</span></span>

### <span data-ttu-id="c2f85-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2f85-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c2f85-166">출력</span><span class="sxs-lookup"><span data-stu-id="c2f85-166">OUTPUTS</span></span>

### <span data-ttu-id="c2f85-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c2f85-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c2f85-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2f85-168">NOTES</span></span>

## <span data-ttu-id="c2f85-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2f85-169">RELATED LINKS</span></span>
