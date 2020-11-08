---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 6482c6e6804b9d59ddbd752d20f39d3316b75f8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056352"
---
# <span data-ttu-id="629ce-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="629ce-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="629ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="629ce-102">SYNOPSIS</span></span>
<span data-ttu-id="629ce-103">클러스터 구성 개체에 Hadoop 구성 값 사용자 지정 및/또는 하이브 공유 라이브러리 사용자 지정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="629ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="629ce-104">SYNTAX</span></span>

### <span data-ttu-id="629ce-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="629ce-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="629ce-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="629ce-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="629ce-107">설명은</span><span class="sxs-lookup"><span data-stu-id="629ce-107">DESCRIPTION</span></span>
<span data-ttu-id="629ce-108">**AzHDInsightConfigValue** cmdlet은 core-site.xml 또는 hive-site.xml와 같은 Hadoop 구성 값 사용자 지정을 추가 하 고 New-AzHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 대 한 하이브 공유 라이브러리 사용자 지정을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="629ce-109">예제의</span><span class="sxs-lookup"><span data-stu-id="629ce-109">EXAMPLES</span></span>

### <span data-ttu-id="629ce-110">예제 1: 클러스터 구성 개체에 사용자 지정 구성 값 추가</span><span class="sxs-lookup"><span data-stu-id="629ce-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="629ce-111">이 명령은-hadoop-001 이라는 클러스터에 Hadoop 구성 값을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="629ce-112">변수</span><span class="sxs-lookup"><span data-stu-id="629ce-112">PARAMETERS</span></span>

### <span data-ttu-id="629ce-113">-구성</span><span class="sxs-lookup"><span data-stu-id="629ce-113">-Config</span></span>
<span data-ttu-id="629ce-114">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="629ce-115">이 개체는 New-AzHDInsightClusterConfig cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="629ce-116">-코어</span><span class="sxs-lookup"><span data-stu-id="629ce-116">-Core</span></span>
<span data-ttu-id="629ce-117">이 HDInsight 클러스터의 핵심 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629ce-118">-DefaultProfile</span></span>
<span data-ttu-id="629ce-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="629ce-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="629ce-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="629ce-120">-HBaseEnv</span></span>
<span data-ttu-id="629ce-121">이 HDInsight 클러스터의 HBase Env 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="629ce-122">-HBaseSite</span></span>
<span data-ttu-id="629ce-123">이 HDInsight 클러스터의 HBase 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-124">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="629ce-124">-Hdfs</span></span>
<span data-ttu-id="629ce-125">이 HDInsight 클러스터의 HDFS 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="629ce-126">-HiveEnv</span></span>
<span data-ttu-id="629ce-127">이 HDInsight 클러스터의 하이브 Env 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="629ce-128">-HiveSite</span></span>
<span data-ttu-id="629ce-129">이 HDInsight 클러스터의 하이브 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="629ce-130">-MapRed</span></span>
<span data-ttu-id="629ce-131">이 HDInsight 클러스터의 MapRed 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-132">-고가</span><span class="sxs-lookup"><span data-stu-id="629ce-132">-OozieEnv</span></span>
<span data-ttu-id="629ce-133">이 HDInsight 클러스터의 Oozie Env 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="629ce-134">-OozieSite</span></span>
<span data-ttu-id="629ce-135">이 HDInsight 클러스터의 Oozie 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="629ce-136">-RServer</span></span>
<span data-ttu-id="629ce-137">RServer 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="629ce-138">RServer 클러스터에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="629ce-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="629ce-139">-Spark2Defaults</span></span>
<span data-ttu-id="629ce-140">이 HDInsight 클러스터의 Spark2 Defaults 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="629ce-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="629ce-142">이 HDInsight 클러스터의 Spark2 Thrift SparkConf 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="629ce-143">-SparkDefaults</span></span>
<span data-ttu-id="629ce-144">이 HDInsight 클러스터의 Spark 기본값 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="629ce-145">-SparkThriftConf</span></span>
<span data-ttu-id="629ce-146">이 HDInsight 클러스터의 Spark Thrift SparkConf 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-147">-폭풍</span><span class="sxs-lookup"><span data-stu-id="629ce-147">-Storm</span></span>
<span data-ttu-id="629ce-148">이 HDInsight 클러스터의 폭풍 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="629ce-149">-Tez</span></span>
<span data-ttu-id="629ce-150">이 HDInsight 클러스터의 Tez 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="629ce-151">-WebHCat</span></span>
<span data-ttu-id="629ce-152">이 HDInsight 클러스터의 WebHCat 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="629ce-153">-Yarn</span></span>
<span data-ttu-id="629ce-154">이 HDInsight 클러스터의 YARN 사이트 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="629ce-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629ce-155">CommonParameters</span></span>
<span data-ttu-id="629ce-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="629ce-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629ce-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="629ce-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629ce-158">입력</span><span class="sxs-lookup"><span data-stu-id="629ce-158">INPUTS</span></span>

### <span data-ttu-id="629ce-159">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="629ce-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="629ce-160">출력</span><span class="sxs-lookup"><span data-stu-id="629ce-160">OUTPUTS</span></span>

### <span data-ttu-id="629ce-161">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="629ce-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="629ce-162">상속자</span><span class="sxs-lookup"><span data-stu-id="629ce-162">NOTES</span></span>

## <span data-ttu-id="629ce-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="629ce-163">RELATED LINKS</span></span>

[<span data-ttu-id="629ce-164">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="629ce-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


