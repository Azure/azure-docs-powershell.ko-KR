---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 78153558764d12a63d6c1b599da2067338969628
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93688862"
---
# Az 모듈
## 설명은
이 섹션의 항목에서는 Azure Resource Manager (ARM) 프레임 워크의 Microsoft Azure HDInsight에 대 한 Azure PowerShell cmdlet을 설명 합니다. 이러한 cmdlet은 HDInsight 클러스터 및이를 실행 하는 작업을 관리 하는 데 사용 됩니다. 이 cmdlet은 Microsoft Azure. e. e. e m m 네임 스페이스에 존재 합니다.

## Az Cmdlet
### [추가-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
클러스터 구성 개체에 클러스터 id를 추가 합니다.

### [추가-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
클러스터에서 실행 되는 서비스의 버전을 클러스터 구성 개체에 추가 합니다.

### [추가-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
클러스터 구성 개체에 Hadoop 구성 값 사용자 지정 및/또는 하이브 공유 라이브러리 사용자 지정을 추가 합니다.

### [추가-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
클러스터 구성 개체에 Hive 또는 Oozie metastore 역할을 하는 SQL 데이터베이스를 추가 합니다.

### [추가-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
클러스터 구성 개체에 스크립트 작업을 추가 합니다.

### [추가-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
클러스터 구성 개체에 보안 프로필을 추가 합니다.

### [추가-AzHDInsightStorage](Add-AzHDInsightStorage.md)
클러스터 구성 개체에 Azure Storage 키를 추가 합니다.

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
HDInsight 클러스터에서 OMS (Operations Management Suite)를 사용 하지 않도록 설정 하면 관련 로그가 사용 중에 지정 된 OMS 작업 영역으로 이동 하지 않습니다.

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
HDInsight 클러스터에서 OMS (Operations Management Suite)를 사용 하도록 설정 하 고, 사용 중에 지정 된 OMS 작업 영역으로 관련 로그를 보냅니다.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
현재 구독 또는 지정 된 리소스 그룹과 연결 된 모든 Azure HDInsight 클러스터를 가져오고 나열 하거나 특정 클러스터를 검색 합니다.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
클러스터의 작업 목록을 가져와 그 순서 대로 역순으로 나열 하거나 특정 작업을 검색 합니다.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
지정한 클러스터와 연결 된 저장소 계정의 작업에 대 한 로그 출력을 가져옵니다.

### [Get-AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
클러스터의 OMS (Operations Management Suite) 설치 상태를 가져옵니다.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
클러스터에 대 한 지속형 스크립트 작업을 가져와 시간 순서 대로 나열 하거나 지정 된 지속형 스크립트 작업에 대 한 세부 정보를 가져옵니다.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
사용 가능한 위치 및 용량 등의 HDInsight 서비스에 대 한 속성을 가져옵니다.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
클러스터에 대 한 스크립트 작업 기록을 가져오고이를 역순으로 나열 하거나 이전에 실행 된 스크립트 작업의 세부 정보를 가져옵니다.

### [부여-AzHDInsightHttpServicesAccess](Grant-AzHDInsightHttpServicesAccess.md)
클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.

### [부여-AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
Windows 클러스터에 RDP 액세스를 허용 합니다.

### [AzHDInsightHiveJob-호출](Invoke-AzHDInsightHiveJob.md)
HDInsight 클러스터에 하이브 쿼리를 제출 하 고 한 번의 작업으로 쿼리 결과를 검색 합니다.

### [새로운 AzHDInsightCluster](New-AzHDInsightCluster.md)
현재 구독에 대 한 지정 된 리소스 그룹에 Azure HDInsight 클러스터를 만듭니다.

### [새로운 AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Azure HDInsight 클러스터 구성을 설명 하는 유지 되지 않는 클러스터 구성 개체를 만듭니다.

### [새로운 AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
하이브 작업 개체를 만듭니다.

### [새로운 AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
MapReduce 작업 개체를 만듭니다.

### [새로운 AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
문 돼지 job 개체를 만듭니다.

### [새로운 AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Sqoop 작업 개체를 만듭니다.

### [새로운 AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
스트리밍 MapReduce 작업 개체를 만듭니다.

### [제거-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
현재 구독에서 지정 된 HDInsight 클러스터를 제거 합니다.

### [제거-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
HDInsight 클러스터에서 지속형 스크립트 작업을 제거 합니다.

### [철회-AzHDInsightHttpServicesAccess](Revoke-AzHDInsightHttpServicesAccess.md)
클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.

### [철회-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
Windows 클러스터에 대 한 RDP 액세스를 사용 하지 않도록 설정 합니다.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
지정 된 클러스터의 작업자 노드 수를 설정 합니다.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
클러스터 구성 개체에서 기본 저장소 계정 설정을 설정 합니다.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
이전에 실행 한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.

### [시작-AzHDInsightJob](Start-AzHDInsightJob.md)
지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.

### [중지-AzHDInsightJob](Stop-AzHDInsightJob.md)
클러스터에서 실행 중인 지정 된 작업을 중지 합니다.

### [제출-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Azure HDInsight 클러스터에 새 스크립트 작업을 제출 합니다.

### [-AzHDInsightCluster 사용](Use-AzHDInsightCluster.md)
Invoke-RmAzureHDInsightHiveJob cmdlet에 사용할 클러스터를 선택 합니다.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
지정 된 작업의 완료 또는 실패를 기다립니다.

