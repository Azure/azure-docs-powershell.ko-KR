---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207368"
---
# Az.HDInsight 모듈
## 설명
이 섹션의 항목에서는 Azure Resource Manager(ARM) 프레임워크의 Microsoft Azure HDInsight용 Azure PowerShell cmdlet을 ARM 설명합니다. 이러한 cmdlet은 HDInsight 클러스터 및 해당 클러스터에서 실행되는 작업을 관리하는 데 사용됩니다. cmdlet은 Microsoft.Azure.Commands.HDInsight 네임스페이스에 있습니다.

## Az.HDInsight Cmdlet
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
클러스터 구성 개체에 클러스터 ID를 추가합니다.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
클러스터에서 실행되는 서비스에 대한 버전을 클러스터 구성 개체에 추가합니다.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Hadoop 구성 값 사용자 지정 및/또는 Hive 공유 라이브러리 사용자 지정을 클러스터 구성 개체에 추가합니다.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
클러스터 구성 개체에 SQL Hive 또는 Oozie metastore 역할을 하는 SQL 데이터베이스를 추가합니다.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
클러스터 구성 개체에 스크립트 작업을 추가합니다.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
클러스터 구성 개체에 보안 프로필을 추가합니다.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
클러스터 구성 개체에 Azure Storage 키를 추가합니다.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정하면 관련 로그가 활성화 중에 지정된 모니터링 작업 영역으로 흐르는 것을 중지합니다.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
HDInsight 클러스터에서 모니터링을 사용하도록 설정하면 사용하도록 설정하는 동안 지정된 모니터링 작업 영역으로 관련 로그가 전송됩니다.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
현재 구독 또는 지정된 리소스 그룹과 연결된 모든 Azure HDInsight 클러스터를 가져온 후 나열하거나 특정 클러스터를 검색합니다.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
HDInsight 클러스터의 자동 조정 구성을 얻습니다.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
HDInsight 클러스터의 호스트를 나열합니다.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
클러스터에서 작업 목록을 가져온 후 역순으로 나열하거나 특정 작업을 검색합니다.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
지정된 클러스터와 연결된 저장소 계정에서 작업의 로그 출력을 얻습니다.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
클러스터의 모니터링 설치 상태를 얻습니다.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
클러스터에 대한 지속형 스크립트 작업을 얻거나 시간 순서로 나열하거나 지정된 지속형 스크립트 작업에 대한 세부 정보를 얻습니다.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
사용 가능한 위치 및 용량과 같은 HDInsight 서비스에 대한 속성을 얻습니다.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
클러스터에 대한 스크립트 작업 기록을 얻거나 역순으로 나열하거나 이전에 실행한 스크립트 동작의 세부 정보를 얻습니다.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
HDInsight 클러스터에 Hive 쿼리를 제출하고 쿼리 결과를 하나의 작업으로 검색합니다.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
현재 구독에 대해 지정된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Azure HDInsight 클러스터의 자동 조정 구성을 설명하는 지속되지 않는 개체를 만듭니다.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
일정 기반 자동 조정 조건을 만듭니다.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Azure HDInsight 클러스터 구성을 설명하는 비 지속형 클러스터 구성 개체를 만듭니다.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Hive 작업 개체를 만듭니다.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
MapReduce 작업 개체를 만듭니다.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Pig 작업 개체를 만듭니다.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Sqoop 작업 개체를 만듭니다.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Streaming MapReduce 작업 개체를 만듭니다.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
현재 구독에서 지정된 HDInsight 클러스터를 제거합니다.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
HDInsight 클러스터의 자동 조정 구성을 제거합니다.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
HDInsight 클러스터에서 지속된 스크립트 작업을 제거합니다.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
HDInsight 클러스터의 특정 호스트를 다시 시작합니다.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Azure HDInsight 클러스터의 자동 조정 구성을 설정합니다.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
지정된 HDInsight 클러스터의 디스크 암호화 키를 회전합니다.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
지정된 클러스터의 Worker 노드 수를 지정합니다.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
클러스터 구성 개체에서 기본 Storage 계정 설정을 지정합니다.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Azure HDInsight 클러스터의 게이트웨이 HTTP 자격 증명을 설정합니다.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
이전에 실행한 스크립트 작업을 지속형 스크립트 동작으로 설정합니다.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
지정된 클러스터에서 정의된 Azure HDInsight 작업을 시작합니다.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
클러스터에서 지정된 실행 중인 작업을 중지합니다.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Azure HDInsight 클러스터에 새 스크립트 작업을 제출합니다.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
클러스터 cmdlet과 함께 사용할 Invoke-RmAzureHDInsightHiveJob 선택합니다.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
지정된 작업의 완료 또는 실패를 기다릴 수 있습니다.

