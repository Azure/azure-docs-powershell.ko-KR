---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1919c773eb51f5e2d57333f42cbcc0793d4dad63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001536"
---
# <span data-ttu-id="329b0-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="329b0-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="329b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="329b0-102">SYNOPSIS</span></span>
<span data-ttu-id="329b0-103">Azure HDInsight 클러스터의 자동 조정 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="329b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="329b0-104">SYNTAX</span></span>

### <span data-ttu-id="329b0-105">LoadAutoscaleByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="329b0-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="329b0-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="329b0-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="329b0-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329b0-114">설명</span><span class="sxs-lookup"><span data-stu-id="329b0-114">DESCRIPTION</span></span>
<span data-ttu-id="329b0-115">이 cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration은** Azure HDInsight 클러스터의 자동 크기 조정 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="329b0-116">예제</span><span class="sxs-lookup"><span data-stu-id="329b0-116">EXAMPLES</span></span>

### <span data-ttu-id="329b0-117">예제 1: HDInsight 클러스터의 부하 기반 자동 조정 구성 설정</span><span class="sxs-lookup"><span data-stu-id="329b0-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="329b0-118">이 명령은 Azure HDInsight 클러스터의 부하 기반 자동 조정 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="329b0-119">예제 2: HDInsight 클러스터의 일정 기반 자동 조정 설정</span><span class="sxs-lookup"><span data-stu-id="329b0-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="329b0-120">이 명령은 HDInsight 클러스터의 일정 기반 자동 조정 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="329b0-121">예제 3: 자동 조정 구성을 설정한 다른 클러스터를 기반으로 HDInsight 클러스터의 자동 조정 구성 설정</span><span class="sxs-lookup"><span data-stu-id="329b0-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="329b0-122">이 명령은 다른 클러스터를 기반으로 HDInsight 클러스터의 자동 조정 구성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="329b0-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="329b0-123">PARAMETERS</span></span>

### <span data-ttu-id="329b0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="329b0-124">-AsJob</span></span>
<span data-ttu-id="329b0-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="329b0-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="329b0-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="329b0-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="329b0-127">자동 조정 구성을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="329b0-128">-ClusterName</span></span>
<span data-ttu-id="329b0-129">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-130">-조건</span><span class="sxs-lookup"><span data-stu-id="329b0-130">-Condition</span></span>
<span data-ttu-id="329b0-131">일정 기반 자동 조정의 조건을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329b0-132">-DefaultProfile</span></span>
<span data-ttu-id="329b0-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329b0-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="329b0-134">-InputObject</span></span>
<span data-ttu-id="329b0-135">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="329b0-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="329b0-137">부하 기반 자동 조정의 최대 workernode 수를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="329b0-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="329b0-139">부하 기반 자동 조정의 최소 workernode 수를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="329b0-140">-ResourceGroupName</span></span>
<span data-ttu-id="329b0-141">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="329b0-142">-ResourceId</span></span>
<span data-ttu-id="329b0-143">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-144">-Schedule</span><span class="sxs-lookup"><span data-stu-id="329b0-144">-Schedule</span></span>
<span data-ttu-id="329b0-145">일정 기반 매개 변수 설정</span><span class="sxs-lookup"><span data-stu-id="329b0-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="329b0-146">-TimeZone</span></span>
<span data-ttu-id="329b0-147">일정 기반 자동 조정의 표준 시간대를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="329b0-148">-확인</span><span class="sxs-lookup"><span data-stu-id="329b0-148">-Confirm</span></span>
<span data-ttu-id="329b0-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329b0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329b0-150">-WhatIf</span></span>
<span data-ttu-id="329b0-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329b0-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329b0-153">CommonParameters</span></span>
<span data-ttu-id="329b0-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="329b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329b0-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="329b0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329b0-156">입력</span><span class="sxs-lookup"><span data-stu-id="329b0-156">INPUTS</span></span>

### <span data-ttu-id="329b0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="329b0-157">System.String</span></span>

### <span data-ttu-id="329b0-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="329b0-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="329b0-159">출력</span><span class="sxs-lookup"><span data-stu-id="329b0-159">OUTPUTS</span></span>

### <span data-ttu-id="329b0-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="329b0-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="329b0-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="329b0-161">NOTES</span></span>

## <span data-ttu-id="329b0-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="329b0-162">RELATED LINKS</span></span>

<span data-ttu-id="329b0-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="329b0-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
