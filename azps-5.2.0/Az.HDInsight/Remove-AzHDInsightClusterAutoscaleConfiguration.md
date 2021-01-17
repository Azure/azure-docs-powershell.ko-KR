---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322951"
---
# <span data-ttu-id="2aa4d-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2aa4d-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="2aa4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa4d-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa4d-103">HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="2aa4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2aa4d-104">SYNTAX</span></span>

### <span data-ttu-id="2aa4d-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2aa4d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa4d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa4d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa4d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa4d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa4d-108">설명</span><span class="sxs-lookup"><span data-stu-id="2aa4d-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa4d-109">**Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet은 HDInsight 클러스터의 자동 크기 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="2aa4d-110">예제</span><span class="sxs-lookup"><span data-stu-id="2aa4d-110">EXAMPLES</span></span>

### <span data-ttu-id="2aa4d-111">예제 1: HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="2aa4d-112">이 명령은 HDInsight 클러스터의 자동 조정 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="2aa4d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aa4d-113">PARAMETERS</span></span>

### <span data-ttu-id="2aa4d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aa4d-114">-AsJob</span></span>
<span data-ttu-id="2aa4d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2aa4d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aa4d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2aa4d-116">-ClusterName</span></span>
<span data-ttu-id="2aa4d-117">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="2aa4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa4d-118">-DefaultProfile</span></span>
<span data-ttu-id="2aa4d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa4d-120">-InputObject</span></span>
<span data-ttu-id="2aa4d-121">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="2aa4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2aa4d-123">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="2aa4d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa4d-124">-ResourceId</span></span>
<span data-ttu-id="2aa4d-125">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="2aa4d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aa4d-126">-Confirm</span></span>
<span data-ttu-id="2aa4d-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa4d-128">-WhatIf</span></span>
<span data-ttu-id="2aa4d-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2aa4d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa4d-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa4d-131">CommonParameters</span></span>
<span data-ttu-id="2aa4d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa4d-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2aa4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa4d-134">입력</span><span class="sxs-lookup"><span data-stu-id="2aa4d-134">INPUTS</span></span>

### <span data-ttu-id="2aa4d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2aa4d-135">System.String</span></span>

### <span data-ttu-id="2aa4d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2aa4d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="2aa4d-137">출력</span><span class="sxs-lookup"><span data-stu-id="2aa4d-137">OUTPUTS</span></span>

### <span data-ttu-id="2aa4d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2aa4d-138">System.Boolean</span></span>

## <span data-ttu-id="2aa4d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2aa4d-139">NOTES</span></span>

## <span data-ttu-id="2aa4d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2aa4d-140">RELATED LINKS</span></span>

<span data-ttu-id="2aa4d-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2aa4d-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
