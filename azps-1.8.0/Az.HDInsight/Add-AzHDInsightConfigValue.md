---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: e5d0e3b7ca23bb335e6b29f56feefefb07018e07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868325"
---
# <span data-ttu-id="b81e3-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="b81e3-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="b81e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b81e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b81e3-103">클러스터 구성 개체에 Hadoop 구성 값 사용자 지정 및/또는 하이브 공유 라이브러리 사용자 지정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="b81e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b81e3-104">SYNTAX</span></span>

### <span data-ttu-id="b81e3-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="b81e3-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b81e3-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="b81e3-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b81e3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b81e3-107">DESCRIPTION</span></span>
<span data-ttu-id="b81e3-108">**AzHDInsightConfigValue** cmdlet은 core-site.xml 또는 hive-site.xml와 같은 Hadoop 구성 값 사용자 지정을 추가 하 고 New-AzHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 대 한 하이브 공유 라이브러리 사용자 지정을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="b81e3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b81e3-109">EXAMPLES</span></span>

### <span data-ttu-id="b81e3-110">예제 1: 클러스터 구성 개체에 사용자 지정 구성 값 추가</span><span class="sxs-lookup"><span data-stu-id="b81e3-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="b81e3-111">이 명령은-hadoop-001 이라는 클러스터에 Hadoop 구성 값을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b81e3-112">변수</span><span class="sxs-lookup"><span data-stu-id="b81e3-112">PARAMETERS</span></span>

### <span data-ttu-id="b81e3-113">-구성</span><span class="sxs-lookup"><span data-stu-id="b81e3-113">-Config</span></span>
<span data-ttu-id="b81e3-114">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b81e3-115">이 개체는 New-AzHDInsightClusterConfig cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="b81e3-116">-코어</span><span class="sxs-lookup"><span data-stu-id="b81e3-116">-Core</span></span>
<span data-ttu-id="b81e3-117">이 HDInsight 클러스터의 핵심 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b81e3-118">-DefaultProfile</span></span>
<span data-ttu-id="b81e3-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b81e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b81e3-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="b81e3-120">-HBaseEnv</span></span>
<span data-ttu-id="b81e3-121">이 HDInsight 클러스터의 HBase Env 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="b81e3-122">-HBaseSite</span></span>
<span data-ttu-id="b81e3-123">이 HDInsight 클러스터의 HBase 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-124">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="b81e3-124">-Hdfs</span></span>
<span data-ttu-id="b81e3-125">이 HDInsight 클러스터의 HDFS 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="b81e3-126">-HiveEnv</span></span>
<span data-ttu-id="b81e3-127">이 HDInsight 클러스터의 하이브 Env 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="b81e3-128">-HiveSite</span></span>
<span data-ttu-id="b81e3-129">이 HDInsight 클러스터의 하이브 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="b81e3-130">-MapRed</span></span>
<span data-ttu-id="b81e3-131">이 HDInsight 클러스터의 MapRed 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-132">-고가</span><span class="sxs-lookup"><span data-stu-id="b81e3-132">-OozieEnv</span></span>
<span data-ttu-id="b81e3-133">이 HDInsight 클러스터의 Oozie Env 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="b81e3-134">-OozieSite</span></span>
<span data-ttu-id="b81e3-135">이 HDInsight 클러스터의 Oozie 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="b81e3-136">-RServer</span></span>
<span data-ttu-id="b81e3-137">RServer 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="b81e3-138">RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="b81e3-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="b81e3-139">-Spark2Defaults</span></span>
<span data-ttu-id="b81e3-140">이 HDInsight 클러스터의 Spark2 Defaults 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81e3-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="b81e3-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="b81e3-142">이 HDInsight 클러스터의 Spark2 Thrift SparkConf 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81e3-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="b81e3-143">-SparkDefaults</span></span>
<span data-ttu-id="b81e3-144">이 HDInsight 클러스터의 Spark 기본값 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81e3-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="b81e3-145">-SparkThriftConf</span></span>
<span data-ttu-id="b81e3-146">이 HDInsight 클러스터의 Spark Thrift SparkConf 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81e3-147">-폭풍</span><span class="sxs-lookup"><span data-stu-id="b81e3-147">-Storm</span></span>
<span data-ttu-id="b81e3-148">이 HDInsight 클러스터의 폭풍 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="b81e3-149">-Tez</span></span>
<span data-ttu-id="b81e3-150">이 HDInsight 클러스터의 Tez 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="b81e3-151">-WebHCat</span></span>
<span data-ttu-id="b81e3-152">이 HDInsight 클러스터의 WebHCat 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="b81e3-153">-Yarn</span></span>
<span data-ttu-id="b81e3-154">이 HDInsight 클러스터의 YARN 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b81e3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81e3-155">CommonParameters</span></span>
<span data-ttu-id="b81e3-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b81e3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81e3-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b81e3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81e3-158">입력</span><span class="sxs-lookup"><span data-stu-id="b81e3-158">INPUTS</span></span>

### <span data-ttu-id="b81e3-159">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="b81e3-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b81e3-160">출력</span><span class="sxs-lookup"><span data-stu-id="b81e3-160">OUTPUTS</span></span>

### <span data-ttu-id="b81e3-161">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="b81e3-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b81e3-162">상속자</span><span class="sxs-lookup"><span data-stu-id="b81e3-162">NOTES</span></span>

## <span data-ttu-id="b81e3-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b81e3-163">RELATED LINKS</span></span>

[<span data-ttu-id="b81e3-164">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b81e3-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


