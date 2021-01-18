---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: 8102a9ce8ef1117822426d6896edf95d21c46607
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492963"
---
# <span data-ttu-id="b8b59-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="b8b59-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="b8b59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b59-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b59-103">클러스터 구성 개체에 SQL Hive 또는 Oozie metastore 역할을 하는 SQL 데이터베이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="b8b59-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8b59-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8b59-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8b59-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b59-106">**Add-AzHDInsightMetastore** cmdlet은 Hive 또는 Oozie metastore를 New-AzHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="b8b59-107">metastore는 Hive SQL Oozie 또는 둘 다에 대한 메타데이터를 저장하는 데 사용할 수 있는 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="b8b59-108">예제</span><span class="sxs-lookup"><span data-stu-id="b8b59-108">EXAMPLES</span></span>

### <span data-ttu-id="b8b59-109">예제 1: 클러스터 SQL metastore 추가</span><span class="sxs-lookup"><span data-stu-id="b8b59-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="b8b59-110">이 명령은 SQL hadoop-001이라는 클러스터에 데이터베이스 metastore를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

### <span data-ttu-id="b8b59-111">예제 2: 클러스터 구성 개체에 사용자 지정 Ambari 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="b8b59-111">Example 2: Add a custom Ambari database to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Custom Amari database info
PS C:\> $ambariSqlServer = "your-sqlserver-001"
PS C:\> $ambariDb = "your-sqldb-003"
PS C:\> $ambariCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$ambariSqlServer.database.contoso.net" `
                -DatabaseName $ambariDb `
                -Credential $ambariCreds `
                -MetastoreType AmbariDatabase `
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

<span data-ttu-id="b8b59-112">이 명령은 사용자 지정 Ambari 데이터베이스를 your-hadoop-002라는 클러스터에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-112">This command adds a custom Ambari database to the cluster named your-hadoop-002.</span></span>

## <span data-ttu-id="b8b59-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b59-113">PARAMETERS</span></span>

### <span data-ttu-id="b8b59-114">-Config</span><span class="sxs-lookup"><span data-stu-id="b8b59-114">-Config</span></span>
<span data-ttu-id="b8b59-115">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b8b59-116">이 개체는 **New-AzHDInsightClusterConfig** cmdlet에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-116">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="b8b59-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="b8b59-117">-Credential</span></span>
<span data-ttu-id="b8b59-118">AzureSQL 서버 데이터베이스에 사용할 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-118">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b59-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8b59-119">-DatabaseName</span></span>
<span data-ttu-id="b8b59-120">이 metastore에 사용할 AzureSQL 서버 인스턴스의 데이터베이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-120">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="b8b59-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b59-121">-DefaultProfile</span></span>
<span data-ttu-id="b8b59-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b8b59-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8b59-123">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="b8b59-123">-MetastoreType</span></span>
<span data-ttu-id="b8b59-124">metastore의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-124">Specifies the type of metastore.</span></span>
<span data-ttu-id="b8b59-125">가능한 값은 HiveMetastore 또는 OozieMetastore입니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-125">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore, AmbariDatabase

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b59-126">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="b8b59-126">-SqlAzureServerName</span></span>
<span data-ttu-id="b8b59-127">이 metastore에 사용할 AzureSQL 서버 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-127">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b59-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b59-128">CommonParameters</span></span>
<span data-ttu-id="b8b59-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8b59-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b59-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b8b59-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b59-131">입력</span><span class="sxs-lookup"><span data-stu-id="b8b59-131">INPUTS</span></span>

### <span data-ttu-id="b8b59-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b8b59-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b8b59-133">출력</span><span class="sxs-lookup"><span data-stu-id="b8b59-133">OUTPUTS</span></span>

### <span data-ttu-id="b8b59-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b8b59-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b8b59-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8b59-135">NOTES</span></span>

## <span data-ttu-id="b8b59-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8b59-136">RELATED LINKS</span></span>

[<span data-ttu-id="b8b59-137">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b8b59-137">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


