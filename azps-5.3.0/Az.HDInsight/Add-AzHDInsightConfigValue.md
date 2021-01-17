---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489640"
---
# <span data-ttu-id="0e6d1-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="0e6d1-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="0e6d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6d1-103">Hadoop 구성 값 사용자 지정 및/또는 Hive 공유 라이브러리 사용자 지정을 클러스터 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="0e6d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e6d1-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e6d1-105">설명</span><span class="sxs-lookup"><span data-stu-id="0e6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="0e6d1-106">**Add-AzHDInsightConfigValue** cmdlet은 core-site.xml 또는 hive-site.xml 및/또는 Hive 공유 라이브러리 사용자 지정과 같은 Hadoop 구성 값 사용자 지정을 New-AzHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="0e6d1-107">예제</span><span class="sxs-lookup"><span data-stu-id="0e6d1-107">EXAMPLES</span></span>

### <span data-ttu-id="0e6d1-108">예제 1: 클러스터 구성 개체에 사용자 지정 구성 값 추가</span><span class="sxs-lookup"><span data-stu-id="0e6d1-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
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
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="0e6d1-109">이 명령은 hadoop-001이라는 클러스터에 Hadoop 구성 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0e6d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e6d1-110">PARAMETERS</span></span>

### <span data-ttu-id="0e6d1-111">-Config</span><span class="sxs-lookup"><span data-stu-id="0e6d1-111">-Config</span></span>
<span data-ttu-id="0e6d1-112">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="0e6d1-113">이 개체는 New-AzHDInsightClusterConfig cmdlet에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="0e6d1-114">-Core</span><span class="sxs-lookup"><span data-stu-id="0e6d1-114">-Core</span></span>
<span data-ttu-id="0e6d1-115">이 HDInsight 클러스터의 핵심 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6d1-116">-DefaultProfile</span></span>
<span data-ttu-id="0e6d1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e6d1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e6d1-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="0e6d1-118">-HBaseEnv</span></span>
<span data-ttu-id="0e6d1-119">이 HDInsight 클러스터의 HBase Env 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="0e6d1-120">-HBaseSite</span></span>
<span data-ttu-id="0e6d1-121">이 HDInsight 클러스터의 HBase 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="0e6d1-122">-Hdfs</span></span>
<span data-ttu-id="0e6d1-123">이 HDInsight 클러스터의 HDFS 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="0e6d1-124">-HiveEnv</span></span>
<span data-ttu-id="0e6d1-125">이 HDInsight 클러스터의 Hive Env 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="0e6d1-126">-HiveSite</span></span>
<span data-ttu-id="0e6d1-127">이 HDInsight 클러스터의 Hive 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="0e6d1-128">-MapRed</span></span>
<span data-ttu-id="0e6d1-129">이 HDInsight 클러스터의 MapRed 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="0e6d1-130">-OozieEnv</span></span>
<span data-ttu-id="0e6d1-131">이 HDInsight 클러스터의 Oozie Env 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="0e6d1-132">-OozieSite</span></span>
<span data-ttu-id="0e6d1-133">이 HDInsight 클러스터의 Oozie 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="0e6d1-134">-RServer</span></span>
<span data-ttu-id="0e6d1-135">RServer 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="0e6d1-136">RServer 클러스터에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="0e6d1-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="0e6d1-137">-Spark2Defaults</span></span>
<span data-ttu-id="0e6d1-138">이 HDInsight 클러스터의 Spark2 기본값 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="0e6d1-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="0e6d1-140">이 HDInsight 클러스터의 Spark2 Thrift SparkConf 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="0e6d1-141">-SparkDefaults</span></span>
<span data-ttu-id="0e6d1-142">이 HDInsight 클러스터의 Spark 기본값 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="0e6d1-143">-SparkThriftConf</span></span>
<span data-ttu-id="0e6d1-144">이 HDInsight 클러스터의 Spark Thrift SparkConf 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="0e6d1-145">-Storm</span></span>
<span data-ttu-id="0e6d1-146">이 HDInsight 클러스터의 Storm 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="0e6d1-147">-Tez</span></span>
<span data-ttu-id="0e6d1-148">이 HDInsight 클러스터의 Tez 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="0e6d1-149">-WebHCat</span></span>
<span data-ttu-id="0e6d1-150">이 HDInsight 클러스터의 WebHCat 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-151">-Yarn</span><span class="sxs-lookup"><span data-stu-id="0e6d1-151">-Yarn</span></span>
<span data-ttu-id="0e6d1-152">이 HDInsight 클러스터의 YARN 사이트 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0e6d1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6d1-153">CommonParameters</span></span>
<span data-ttu-id="0e6d1-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6d1-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6d1-156">입력</span><span class="sxs-lookup"><span data-stu-id="0e6d1-156">INPUTS</span></span>

### <span data-ttu-id="0e6d1-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0e6d1-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0e6d1-158">출력</span><span class="sxs-lookup"><span data-stu-id="0e6d1-158">OUTPUTS</span></span>

### <span data-ttu-id="0e6d1-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0e6d1-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0e6d1-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e6d1-160">NOTES</span></span>

## <span data-ttu-id="0e6d1-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e6d1-161">RELATED LINKS</span></span>

[<span data-ttu-id="0e6d1-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0e6d1-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


