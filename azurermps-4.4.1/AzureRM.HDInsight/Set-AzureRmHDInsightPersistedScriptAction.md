---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28c608711e222ce85d4ea959caa6c4afe7bafaaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537199"
---
# Set-AzureRmHDInsightPersistedScriptAction

## SYNOPSIS
이전에 실행 한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmHDInsightPersistedScriptAction** cmdlet은 이전에 실행 된 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.
지정 된 스크립트 작업은 이전에 성공 해야 합니다.
Azure HDInsight 클러스터의 크기를 조정할 때마다 스크립트 작업이 실행 됩니다.

## 예제의

### 예제 1: 이전에 성공한 스크립트 작업을 유지 하거나 클러스터 확장에서 실행 하도록 설정
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

이 명령은 이전에 성공한 스크립트 작업을 지속형 스크립트 작업으로 설정 합니다.

## 변수

### -ClusterName
클러스터의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptExecutionId
유지 하도록 승격할 스크립트 작업의 실행 ID를 지정 합니다.
이 스크립트 동작은 승격 되려면 성공이 필요 합니다.
Get-AzureRmHDInsightScriptActionHistory를 사용 하 여 스크립트 작업 실행 ID를 찾을 수 있습니다.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### 시스템. i a o

## 상속자

## 관련 링크

[Get-AzureRmHDInsightPersistedScriptAction](./Get-AzureRmHDInsightPersistedScriptAction.md)

[제거-AzureRmHDInsightPersistedScriptAction](./Remove-AzureRmHDInsightPersistedScriptAction.md)


