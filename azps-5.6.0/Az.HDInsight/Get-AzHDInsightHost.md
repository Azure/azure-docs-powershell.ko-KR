---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012112"
---
# <span data-ttu-id="94a0a-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="94a0a-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="94a0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="94a0a-103">HDInsight 클러스터의 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="94a0a-104">구문</span><span class="sxs-lookup"><span data-stu-id="94a0a-104">SYNTAX</span></span>

### <span data-ttu-id="94a0a-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="94a0a-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a0a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a0a-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a0a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94a0a-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94a0a-108">설명</span><span class="sxs-lookup"><span data-stu-id="94a0a-108">DESCRIPTION</span></span>
<span data-ttu-id="94a0a-109">**Get-AzHDInsightHost** cmdlet에는 HDInsight 클러스터의 호스트가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="94a0a-110">예제</span><span class="sxs-lookup"><span data-stu-id="94a0a-110">EXAMPLES</span></span>

### <span data-ttu-id="94a0a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="94a0a-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="94a0a-112">이 명령은 클러스터 이름이 있는 클러스터의 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="94a0a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="94a0a-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="94a0a-114">이 명령은 파이프라인이 있는 클러스터의 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="94a0a-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="94a0a-115">PARAMETERS</span></span>

### <span data-ttu-id="94a0a-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94a0a-116">-ClusterName</span></span>
<span data-ttu-id="94a0a-117">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a0a-118">-DefaultProfile</span></span>
<span data-ttu-id="94a0a-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a0a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94a0a-120">-InputObject</span></span>
<span data-ttu-id="94a0a-121">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94a0a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a0a-122">-ResourceGroupName</span></span>
<span data-ttu-id="94a0a-123">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a0a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a0a-124">-ResourceId</span></span>
<span data-ttu-id="94a0a-125">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a0a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a0a-126">CommonParameters</span></span>
<span data-ttu-id="94a0a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94a0a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a0a-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94a0a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a0a-129">입력</span><span class="sxs-lookup"><span data-stu-id="94a0a-129">INPUTS</span></span>

### <span data-ttu-id="94a0a-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="94a0a-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="94a0a-131">출력</span><span class="sxs-lookup"><span data-stu-id="94a0a-131">OUTPUTS</span></span>

### <span data-ttu-id="94a0a-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="94a0a-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="94a0a-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94a0a-133">NOTES</span></span>

## <span data-ttu-id="94a0a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94a0a-134">RELATED LINKS</span></span>
