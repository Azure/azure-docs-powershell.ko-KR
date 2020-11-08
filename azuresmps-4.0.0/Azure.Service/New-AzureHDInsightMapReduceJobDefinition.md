---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045916"
---
# New-AzureHDInsightMapReduceJobDefinition

## SYNOPSIS
새 MapReduce 작업을 정의 합니다.

## 구문과

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.
이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.
최신 버전의 Azure PowerShell HDInsight를 사용 하세요.

새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

**AzureHDInsightMapReduceJobDefinition** cmdlet은 새 MapReduce 작업을 정의 하 여 Azure HDInsight 클러스터에서 실행 됩니다.

## 예제의

### 예제 1: MapReduce 작업 정의, 작업 실행 및 출력 가져오기
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

첫 번째 명령은 현재 구독의 ID를 가져온 다음 $SubId 변수에 저장 합니다.

두 번째 명령은 $Clustername 변수에 이름 MyCluster를 할당 합니다.

세 번째 명령은 **새 AzureHDInsightMapReduceJobDefinition** cmdlet을 사용 하 여 MapReduce 작업 정의를 만든 다음이를 $WordCountJob 변수에 저장 합니다.

네 번째 명령은 다음 cmdlet을 사용 하 여 일련의 작업을 수행 합니다. 

- $ClusterName에서 작업을 시작 하려면 **-AzureHDInsightJob** 을 실행 합니다. 
- **Wait-AzureHDInsightJob** 작업이 완료 될 때까지 기다리거나 완료 진행률을 표시 합니다.
- 작업 출력을 가져오는 **AzureHDInsightJobOutput** .

## 변수

### -인수
Hadoop 작업에 대 한 인수 배열을 지정 합니다.
인수는 각 작업에 명령줄 인수로 전달 됩니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClassName
"JAR (Java Archive)" 파일에서 작업 클래스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -정의
작업을 실행할 때 설정할 Hadoop 구성 값을 지정 합니다.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -파일
작업에 필요한 WASB 파일 배열을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JarFile
MapReduce 작업의 코드 및 종속성을 포함 하는 JAR 파일의 정규화 된 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
MapReduce 작업의 이름을 지정 합니다.
이 매개 변수는 선택 사항입니다.
이 매개 변수를 지정 하지 않으면 *ClassName* 매개 변수의 값이 사용 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LibJars
작업에 대 한 참조 배열을 지정 합니다.

```yaml
Type: String[]
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

### -StatusFolder
종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력과 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.

```yaml
Type: String
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

[Get-AzureHDInsightJobOutput](./Get-AzureHDInsightJobOutput.md)

[새로운 AzureHDInsightHiveJobDefinition](./New-AzureHDInsightHiveJobDefinition.md)

[새로운 AzureHDInsightPigJobDefinition](./New-AzureHDInsightPigJobDefinition.md)

[새로운 AzureHDInsightSqoopJobDefinition](./New-AzureHDInsightSqoopJobDefinition.md)

[시작-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Wait-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)


