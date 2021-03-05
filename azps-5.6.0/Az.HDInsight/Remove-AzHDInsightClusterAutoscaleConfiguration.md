---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c18567cac6edbeb55b0f7442b45748bc3d62bc86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980411"
---
# <span data-ttu-id="dc24c-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc24c-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="dc24c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc24c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc24c-103">HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="dc24c-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc24c-104">SYNTAX</span></span>

### <span data-ttu-id="dc24c-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc24c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc24c-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc24c-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc24c-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc24c-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc24c-108">설명</span><span class="sxs-lookup"><span data-stu-id="dc24c-108">DESCRIPTION</span></span>
<span data-ttu-id="dc24c-109">**Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet은 HDInsight 클러스터의 자동 크기 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="dc24c-110">예제</span><span class="sxs-lookup"><span data-stu-id="dc24c-110">EXAMPLES</span></span>

### <span data-ttu-id="dc24c-111">예제 1: HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="dc24c-112">이 명령은 HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="dc24c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc24c-113">PARAMETERS</span></span>

### <span data-ttu-id="dc24c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc24c-114">-AsJob</span></span>
<span data-ttu-id="dc24c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dc24c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc24c-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dc24c-116">-ClusterName</span></span>
<span data-ttu-id="dc24c-117">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc24c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc24c-118">-DefaultProfile</span></span>
<span data-ttu-id="dc24c-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc24c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc24c-120">-InputObject</span></span>
<span data-ttu-id="dc24c-121">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc24c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc24c-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc24c-123">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc24c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc24c-124">-ResourceId</span></span>
<span data-ttu-id="dc24c-125">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc24c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="dc24c-126">-Confirm</span></span>
<span data-ttu-id="dc24c-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc24c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc24c-128">-WhatIf</span></span>
<span data-ttu-id="dc24c-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc24c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc24c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc24c-131">CommonParameters</span></span>
<span data-ttu-id="dc24c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc24c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc24c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc24c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc24c-134">입력</span><span class="sxs-lookup"><span data-stu-id="dc24c-134">INPUTS</span></span>

### <span data-ttu-id="dc24c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dc24c-135">System.String</span></span>

### <span data-ttu-id="dc24c-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dc24c-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="dc24c-137">출력</span><span class="sxs-lookup"><span data-stu-id="dc24c-137">OUTPUTS</span></span>

### <span data-ttu-id="dc24c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc24c-138">System.Boolean</span></span>

## <span data-ttu-id="dc24c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc24c-139">NOTES</span></span>

## <span data-ttu-id="dc24c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc24c-140">RELATED LINKS</span></span>

<span data-ttu-id="dc24c-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dc24c-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
