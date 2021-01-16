---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357309"
---
# <span data-ttu-id="791d1-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="791d1-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="791d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="791d1-102">SYNOPSIS</span></span>
<span data-ttu-id="791d1-103">HDInsight 클러스터의 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="791d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="791d1-104">SYNTAX</span></span>

### <span data-ttu-id="791d1-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="791d1-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="791d1-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="791d1-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="791d1-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="791d1-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="791d1-108">설명</span><span class="sxs-lookup"><span data-stu-id="791d1-108">DESCRIPTION</span></span>
<span data-ttu-id="791d1-109">**Get-AzHDInsightHost** cmdlet은 HDInsight 클러스터의 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="791d1-110">예제</span><span class="sxs-lookup"><span data-stu-id="791d1-110">EXAMPLES</span></span>

### <span data-ttu-id="791d1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="791d1-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="791d1-112">이 명령은 클러스터 이름을 사용하여 클러스터의 호스트 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="791d1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="791d1-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="791d1-114">이 명령은 파이프라인이 있는 클러스터의 호스트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="791d1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="791d1-115">PARAMETERS</span></span>

### <span data-ttu-id="791d1-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="791d1-116">-ClusterName</span></span>
<span data-ttu-id="791d1-117">클러스터의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="791d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791d1-118">-DefaultProfile</span></span>
<span data-ttu-id="791d1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="791d1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="791d1-120">-InputObject</span></span>
<span data-ttu-id="791d1-121">입력 개체를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="791d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="791d1-123">리소스 그룹의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="791d1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="791d1-124">-ResourceId</span></span>
<span data-ttu-id="791d1-125">리소스 ID를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="791d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791d1-126">CommonParameters</span></span>
<span data-ttu-id="791d1-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="791d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791d1-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="791d1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791d1-129">입력</span><span class="sxs-lookup"><span data-stu-id="791d1-129">INPUTS</span></span>

### <span data-ttu-id="791d1-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="791d1-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="791d1-131">출력</span><span class="sxs-lookup"><span data-stu-id="791d1-131">OUTPUTS</span></span>

### <span data-ttu-id="791d1-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="791d1-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="791d1-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="791d1-133">NOTES</span></span>

## <span data-ttu-id="791d1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="791d1-134">RELATED LINKS</span></span>
