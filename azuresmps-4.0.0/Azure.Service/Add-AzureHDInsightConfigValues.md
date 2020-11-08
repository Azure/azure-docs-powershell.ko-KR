---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045728"
---
# <span data-ttu-id="e733c-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="e733c-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="e733c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e733c-102">SYNOPSIS</span></span>
<span data-ttu-id="e733c-103">HDInsight 클러스터 구성에 Hadoop 구성 값 사용자 지정 또는 하이브 공유 라이브러리 사용자 지정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e733c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e733c-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e733c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e733c-105">DESCRIPTION</span></span>
<span data-ttu-id="e733c-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e733c-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e733c-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="e733c-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e733c-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e733c-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e733c-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출을](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e733c-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e733c-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure HDInsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e733c-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e733c-112">**AzureHDInsightConfigValues** cmdlet은 Core-site.xml 또는 Hive-site.xml 같은 Hadoop 구성 값 사용자 지정 또는 하이브 공유 라이브러리 사용자 지정을 Azure HDInsight 클러스터 구성에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="e733c-113">Cmdlet은 사용자 지정 구성 값을 지정 된 구성 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="e733c-114">사용자 지정 설정은 클러스터가 배포 될 때 관련 Hadoop 서비스의 구성 파일에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="e733c-115">예제의</span><span class="sxs-lookup"><span data-stu-id="e733c-115">EXAMPLES</span></span>

### <span data-ttu-id="e733c-116">예제 1: 클러스터 구성</span><span class="sxs-lookup"><span data-stu-id="e733c-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="e733c-117">첫 번째 명령은 새 **AzureHDInsightHiveConfiguration** 개체를 만든 다음이를 $HiveConfigValues 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="e733c-118">다음 5 개의 명령은 Hive에 대 한 구성 값을 만들고 이러한 값을 $HiveConfigValues의 구성원으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="e733c-119">일곱 번째 명령은 **AzureHDInsightOozieConfiguration** 개체를 만든 다음이를 $OozieConfigValues 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="e733c-120">여덟 번째 명령은 Oozie에 대 한 구성 값을 만든 다음 해당 값을 $OozieConfigValues의 구성원으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="e733c-121">아홉 번째 명령은 **AzureHDInsightMapReduceConfiguration** 개체를 만든 다음이를 $MapredConfigValues 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="e733c-122">다음 두 명령은 MapReduce에 대 한 구성 값을 만들고 이러한 값을 $MapredConfigValues의 멤버로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="e733c-123">12 번째 명령은 **새 AzureHDInsightClusterConfig** cmdlet을 사용 하 여 HDInsight 클러스터 구성을 만든 다음이를 $Config 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="e733c-124">이 명령은 파이프라인 연산자를 사용 하 여 $Config를 **Set-AzureHDInsightDefaultStorage** cmdlet에 전달 하 여 기본 저장소 설정을 업데이트 하 고 **추가-AzureHDInsightConfigValues** cmdlet으로 새 구성 값을 클러스터 구성에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="e733c-125">마지막 명령은 파이프라인 연산자를 사용 하 여 $Config를 새 HDInsight 클러스터를 **AzureHDInsightCluster** cmdlet에 전달 하 여 사용자 지정 된 설정을 사용 하 여 새 HDInsight 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="e733c-126">변수</span><span class="sxs-lookup"><span data-stu-id="e733c-126">PARAMETERS</span></span>

### <span data-ttu-id="e733c-127">-구성</span><span class="sxs-lookup"><span data-stu-id="e733c-127">-Config</span></span>
<span data-ttu-id="e733c-128">Hadoop 구성을 추가할 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-129">-코어</span><span class="sxs-lookup"><span data-stu-id="e733c-129">-Core</span></span>
<span data-ttu-id="e733c-130">Core-site.xml에 대 한 Hadoop 구성 값의 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="e733c-131">-HBase</span></span>
<span data-ttu-id="e733c-132">Hbase-site.xml에 대 한 HBase 구성 값의 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-133">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="e733c-133">-Hdfs</span></span>
<span data-ttu-id="e733c-134">Hdfs-site.xml에 대 한 Hadoop 구성 값의 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-135">-하이브</span><span class="sxs-lookup"><span data-stu-id="e733c-135">-Hive</span></span>
<span data-ttu-id="e733c-136">Hive-site.xml 및 하이브 공유 라이브러리에 대 한 Hadoop 구성 값 집합을 포함 하 여 Hadoop 하이브 서비스에 대 한 사용자 지정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="e733c-137">-MapReduce</span></span>
<span data-ttu-id="e733c-138">MapReduce 및 용량 스케줄러에 대 한 사용자 지정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="e733c-139">-Oozie</span></span>
<span data-ttu-id="e733c-140">Oozie-site.xml에 대 한 Hadoop 구성 값 집합을 포함 하 여 Hadoop Oozie 서비스에 대 한 사용자 지정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="e733c-141">-Profile</span></span>
<span data-ttu-id="e733c-142">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e733c-143">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="e733c-144">-Spark</span></span>
<span data-ttu-id="e733c-145">Apache Spark에 대 한 사용자 지정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-145">Specifies a customization object for Apache Spark.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-146">-폭풍</span><span class="sxs-lookup"><span data-stu-id="e733c-146">-Storm</span></span>
<span data-ttu-id="e733c-147">Apache 스톰의 사용자 지정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-147">Specifies a customization object for Apache Storm.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-148">-Yarn</span><span class="sxs-lookup"><span data-stu-id="e733c-148">-Yarn</span></span>
<span data-ttu-id="e733c-149">Yarn-site.xml에 대 한 사용자 지정 YARN 구성 값 집합을 지정 하 여 Hadoop YARN의 사용자 지정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e733c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e733c-150">CommonParameters</span></span>
<span data-ttu-id="e733c-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e733c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e733c-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e733c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e733c-153">입력</span><span class="sxs-lookup"><span data-stu-id="e733c-153">INPUTS</span></span>

## <span data-ttu-id="e733c-154">출력</span><span class="sxs-lookup"><span data-stu-id="e733c-154">OUTPUTS</span></span>

## <span data-ttu-id="e733c-155">상속자</span><span class="sxs-lookup"><span data-stu-id="e733c-155">NOTES</span></span>

## <span data-ttu-id="e733c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e733c-156">RELATED LINKS</span></span>

[<span data-ttu-id="e733c-157">새로운 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e733c-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e733c-158">새로운 AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e733c-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="e733c-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="e733c-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
