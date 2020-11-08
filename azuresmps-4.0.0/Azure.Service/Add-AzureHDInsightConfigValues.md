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
# Add-AzureHDInsightConfigValues

## SYNOPSIS
HDInsight 클러스터 구성에 Hadoop 구성 값 사용자 지정 또는 하이브 공유 라이브러리 사용자 지정을 추가 합니다.

## 구문과

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.
이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.
최신 버전의 Azure PowerShell HDInsight를 사용 하세요.

새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)를 참조 하세요.
Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출을](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)참조 하세요.
Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure HDInsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx)을 참조 하세요.

**AzureHDInsightConfigValues** cmdlet은 Core-site.xml 또는 Hive-site.xml 같은 Hadoop 구성 값 사용자 지정 또는 하이브 공유 라이브러리 사용자 지정을 Azure HDInsight 클러스터 구성에 추가 합니다.

Cmdlet은 사용자 지정 구성 값을 지정 된 구성 개체에 추가 합니다.
사용자 지정 설정은 클러스터가 배포 될 때 관련 Hadoop 서비스의 구성 파일에 추가 됩니다.

## 예제의

### 예제 1: 클러스터 구성
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

첫 번째 명령은 새 **AzureHDInsightHiveConfiguration** 개체를 만든 다음이를 $HiveConfigValues 변수에 저장 합니다.

다음 5 개의 명령은 Hive에 대 한 구성 값을 만들고 이러한 값을 $HiveConfigValues의 구성원으로 저장 합니다.

일곱 번째 명령은 **AzureHDInsightOozieConfiguration** 개체를 만든 다음이를 $OozieConfigValues 변수에 저장 합니다.
여덟 번째 명령은 Oozie에 대 한 구성 값을 만든 다음 해당 값을 $OozieConfigValues의 구성원으로 저장 합니다.

아홉 번째 명령은 **AzureHDInsightMapReduceConfiguration** 개체를 만든 다음이를 $MapredConfigValues 변수에 저장 합니다.
다음 두 명령은 MapReduce에 대 한 구성 값을 만들고 이러한 값을 $MapredConfigValues의 멤버로 저장 합니다.

12 번째 명령은 **새 AzureHDInsightClusterConfig** cmdlet을 사용 하 여 HDInsight 클러스터 구성을 만든 다음이를 $Config 변수에 저장 합니다.
이 명령은 파이프라인 연산자를 사용 하 여 $Config를 **Set-AzureHDInsightDefaultStorage** cmdlet에 전달 하 여 기본 저장소 설정을 업데이트 하 고 **추가-AzureHDInsightConfigValues** cmdlet으로 새 구성 값을 클러스터 구성에 추가 합니다.

마지막 명령은 파이프라인 연산자를 사용 하 여 $Config를 새 HDInsight 클러스터를 **AzureHDInsightCluster** cmdlet에 전달 하 여 사용자 지정 된 설정을 사용 하 여 새 HDInsight 클러스터를 만듭니다.

## 변수

### -구성
Hadoop 구성을 추가할 구성 개체를 지정 합니다.

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

### -코어
Core-site.xml에 대 한 Hadoop 구성 값의 집합을 지정 합니다.

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

### -HBase
Hbase-site.xml에 대 한 HBase 구성 값의 집합을 지정 합니다.

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

### -Hdfs
Hdfs-site.xml에 대 한 Hadoop 구성 값의 집합을 지정 합니다.

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

### -하이브
Hive-site.xml 및 하이브 공유 라이브러리에 대 한 Hadoop 구성 값 집합을 포함 하 여 Hadoop 하이브 서비스에 대 한 사용자 지정 개체를 지정 합니다.

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

### -MapReduce
MapReduce 및 용량 스케줄러에 대 한 사용자 지정 개체를 지정 합니다.

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

### -Oozie
Oozie-site.xml에 대 한 Hadoop 구성 값 집합을 포함 하 여 Hadoop Oozie 서비스에 대 한 사용자 지정 개체를 지정 합니다.

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

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -Spark
Apache Spark에 대 한 사용자 지정 개체를 지정 합니다.

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

### -폭풍
Apache 스톰의 사용자 지정 개체를 지정 합니다.

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

### -Yarn
Yarn-site.xml에 대 한 사용자 지정 YARN 구성 값 집합을 지정 하 여 Hadoop YARN의 사용자 지정 개체를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[새로운 AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[새로운 AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
