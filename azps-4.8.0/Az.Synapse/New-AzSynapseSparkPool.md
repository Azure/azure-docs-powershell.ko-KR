---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204182"
---
# <span data-ttu-id="372d9-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="372d9-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="372d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372d9-102">SYNOPSIS</span></span>
<span data-ttu-id="372d9-103">Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="372d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="372d9-104">SYNTAX</span></span>

### <span data-ttu-id="372d9-105">CreateByNameAndEnableAutoScaleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="372d9-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372d9-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="372d9-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372d9-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="372d9-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372d9-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="372d9-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372d9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="372d9-109">DESCRIPTION</span></span>
<span data-ttu-id="372d9-110">**AzSynapseSparkPool** Cmdlet은 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="372d9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="372d9-111">EXAMPLES</span></span>

### <span data-ttu-id="372d9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="372d9-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="372d9-113">이 명령은 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="372d9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="372d9-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="372d9-115">이 명령은 자동 크기 조정을 사용 하 여 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="372d9-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="372d9-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="372d9-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="372d9-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="372d9-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="372d9-119">이 명령은 파이프라인을 통해 자동 크기 조정을 사용 하 여 Azure Synapse Analytics Spark 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="372d9-120">변수</span><span class="sxs-lookup"><span data-stu-id="372d9-120">PARAMETERS</span></span>

### <span data-ttu-id="372d9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="372d9-121">-AsJob</span></span>
<span data-ttu-id="372d9-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="372d9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="372d9-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="372d9-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="372d9-124">유휴 상태인 분 수입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-124">Number of minutes idle.</span></span> <span data-ttu-id="372d9-125">자동 일시 정지가 설정 된 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="372d9-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="372d9-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="372d9-127">지정 된 Spark 풀에 할당할 최대 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="372d9-128">자동 크기 조정을 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="372d9-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="372d9-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="372d9-130">지정 된 Spark 풀에 할당할 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="372d9-131">자동 크기 조정을 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="372d9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372d9-132">-DefaultProfile</span></span>
<span data-ttu-id="372d9-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372d9-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="372d9-134">-EnableAutoPause</span></span>
<span data-ttu-id="372d9-135">자동 일시 중지를 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="372d9-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="372d9-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="372d9-137">환경 구성 파일 ("주사위 멈춤" 출력).</span><span class="sxs-lookup"><span data-stu-id="372d9-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="372d9-138">-이름</span><span class="sxs-lookup"><span data-stu-id="372d9-138">-Name</span></span>
<span data-ttu-id="372d9-139">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="372d9-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="372d9-140">-NodeCount</span></span>
<span data-ttu-id="372d9-141">지정 된 Spark 풀에 할당할 노드의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="372d9-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="372d9-142">-NodeSize</span></span>
<span data-ttu-id="372d9-143">지정 된 Spark 풀에 할당 된 노드에 사용할 코어 및 메모리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="372d9-144">자동 크기 조정을 사용 하지 않는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="372d9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372d9-145">-ResourceGroupName</span></span>
<span data-ttu-id="372d9-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-146">Resource group name.</span></span>

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

### <span data-ttu-id="372d9-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="372d9-147">-SparkVersion</span></span>
<span data-ttu-id="372d9-148">Apache Spark 버전.</span><span class="sxs-lookup"><span data-stu-id="372d9-148">Apache Spark version.</span></span>
<span data-ttu-id="372d9-149">허용 되는 값: 2.4</span><span class="sxs-lookup"><span data-stu-id="372d9-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="372d9-150">태그</span><span class="sxs-lookup"><span data-stu-id="372d9-150">-Tag</span></span>
<span data-ttu-id="372d9-151">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="372d9-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="372d9-152">-WorkspaceName</span></span>
<span data-ttu-id="372d9-153">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="372d9-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="372d9-154">-WorkspaceObject</span></span>
<span data-ttu-id="372d9-155">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="372d9-156">-확인</span><span class="sxs-lookup"><span data-stu-id="372d9-156">-Confirm</span></span>
<span data-ttu-id="372d9-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372d9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372d9-158">-WhatIf</span></span>
<span data-ttu-id="372d9-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372d9-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372d9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372d9-161">CommonParameters</span></span>
<span data-ttu-id="372d9-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="372d9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372d9-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="372d9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372d9-164">입력</span><span class="sxs-lookup"><span data-stu-id="372d9-164">INPUTS</span></span>

### <span data-ttu-id="372d9-165">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="372d9-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="372d9-166">출력</span><span class="sxs-lookup"><span data-stu-id="372d9-166">OUTPUTS</span></span>

### <span data-ttu-id="372d9-167">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="372d9-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="372d9-168">상속자</span><span class="sxs-lookup"><span data-stu-id="372d9-168">NOTES</span></span>

## <span data-ttu-id="372d9-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="372d9-169">RELATED LINKS</span></span>
