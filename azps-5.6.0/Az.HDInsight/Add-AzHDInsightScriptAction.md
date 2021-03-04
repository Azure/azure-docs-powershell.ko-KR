---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: f80ac8dda086910cf83e1d010f2878b6e4ba9362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990159"
---
# <span data-ttu-id="05c65-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="05c65-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="05c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05c65-102">SYNOPSIS</span></span>
<span data-ttu-id="05c65-103">클러스터 구성 개체에 스크립트 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="05c65-104">구문</span><span class="sxs-lookup"><span data-stu-id="05c65-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05c65-105">설명</span><span class="sxs-lookup"><span data-stu-id="05c65-105">DESCRIPTION</span></span>
<span data-ttu-id="05c65-106">**Add-AzHDInsightScriptAction** cmdlet은 New-AzHDInsightClusterConfig 만든 HDInsight 구성 개체에 스크립트 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="05c65-107">스크립트 작업은 추가 소프트웨어를 설치하거나 Windows 또는 Linux 클러스터의 경우 각각 Windows PowerShell 또는 Bash 스크립트를 사용하여 Hadoop 클러스터에서 실행되는 애플리케이션의 구성을 변경하는 데 사용되는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="05c65-108">스크립트 작업은 HDInsight 클러스터가 배포될 때 클러스터 노드에서 실행하고 클러스터의 노드가 HDInsight 구성을 완료한 후에 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="05c65-109">스크립트 작업은 시스템 관리자 계정 권한 아래에서 실행하며 클러스터 노드에 대한 전체 액세스 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="05c65-110">지정된 순서로 실행할 스크립트 작업 목록을 각 클러스터에 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="05c65-111">예제</span><span class="sxs-lookup"><span data-stu-id="05c65-111">EXAMPLES</span></span>

### <span data-ttu-id="05c65-112">예제 1: 클러스터 구성 개체에 스크립트 작업 추가</span><span class="sxs-lookup"><span data-stu-id="05c65-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="05c65-113">이 명령은 클러스터 만들기가 끝날 때 실행될 your-hadoop-001 클러스터의 헤드 및 Worker 노드에 대한 스크립트 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="05c65-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="05c65-114">PARAMETERS</span></span>

### <span data-ttu-id="05c65-115">-Config</span><span class="sxs-lookup"><span data-stu-id="05c65-115">-Config</span></span>
<span data-ttu-id="05c65-116">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="05c65-117">이 개체는 **New-AzHDInsightClusterConfig** cmdlet에 의해 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05c65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c65-118">-DefaultProfile</span></span>
<span data-ttu-id="05c65-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="05c65-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05c65-120">-Name</span><span class="sxs-lookup"><span data-stu-id="05c65-120">-Name</span></span>
<span data-ttu-id="05c65-121">스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-121">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c65-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="05c65-122">-NodeType</span></span>
<span data-ttu-id="05c65-123">스크립트 작업을 실행할 노드 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="05c65-124">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05c65-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="05c65-125">HeadNode</span></span>
- <span data-ttu-id="05c65-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="05c65-126">WorkerNode</span></span>
- <span data-ttu-id="05c65-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="05c65-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c65-128">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="05c65-128">-Parameters</span></span>
<span data-ttu-id="05c65-129">스크립트 작업의 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c65-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="05c65-130">-Uri</span></span>
<span data-ttu-id="05c65-131">스크립트 작업(PowerShell 또는 Bash 스크립트)에 대한 공용 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c65-132">CommonParameters</span></span>
<span data-ttu-id="05c65-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05c65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c65-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05c65-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c65-135">입력</span><span class="sxs-lookup"><span data-stu-id="05c65-135">INPUTS</span></span>

### <span data-ttu-id="05c65-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="05c65-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="05c65-137">출력</span><span class="sxs-lookup"><span data-stu-id="05c65-137">OUTPUTS</span></span>

### <span data-ttu-id="05c65-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="05c65-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="05c65-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05c65-139">NOTES</span></span>

## <span data-ttu-id="05c65-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05c65-140">RELATED LINKS</span></span>

[<span data-ttu-id="05c65-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="05c65-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


