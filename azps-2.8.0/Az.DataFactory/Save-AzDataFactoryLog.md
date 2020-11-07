---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 976f00f62cfda991e7d1aff349a0b04807dbbe1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696983"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Azure HDInsight 처리에서 로그 파일을 다운로드 합니다.

## 구문과

### ByFactoryName (기본값)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDataFactoryLog** Cmdlet은 문 돼지 또는 Hive 프로젝트의 Azure HDInsight 처리 또는 사용자 지정 작업을 로컬 하드 드라이브에 연결 하는 로그 파일을 다운로드 합니다.
먼저 Get-AzDataFactoryRun cmdlet을 실행 하 여 데이터 조각에 대 한 활동의 ID를 가져온 다음 해당 ID를 사용 하 여 HDInsight 클러스터와 연결 된 BLOB (binary large object) 저장소에서 로그 파일을 검색 합니다.
*Downloadlogs* 매개 변수를 지정 하지 않으면 cmdlet은 로그 파일의 위치를 반환 합니다.
출력 디렉터리 ( *output* 매개 변수)를 지정 하지 않고 *downloadlogs* 를 지정 하면 로그 파일이 기본 문서 폴더로 다운로드 됩니다.
출력 폴더 ( *출력* )와 함께 *downloadlogs* 를 지정 하면 로그 파일이 지정 된 폴더에 다운로드 됩니다.

## 예제의

### 예제 1: 특정 폴더에 로그 파일 저장
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

이 명령은 841b77c9-d56c-48d1-99a3-8c16c3e77d39의 ID를 사용 하 여 작업 실행에 대 한 로그 파일을 저장 합니다. 라는 리소스 그룹의 LogProcessingFactory 이라는 data factory의 파이프라인에 속해 있습니다.
로그 파일이 C:\Test 폴더에 저장 됩니다.

### 예제 2: 기본 문서 폴더에 로그 파일 저장
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

이 명령은 로그 파일을 문서 폴더에 저장 합니다 (기본값).

### 예제 3: 로그 파일의 위치 가져오기
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

이 명령은 로그 파일의 위치를 반환 합니다.
*Downloadlogs* 는 지정 되지 않음에 유의 하세요.

## 변수

### -DataFactory
**PSDataFactory** 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Data factory의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 로그 파일을 다운로드 합니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -DownloadLogs
이 cmdlet이 로그 파일을 로컬 컴퓨터에 다운로드 함을 나타냅니다.
*출력* 폴더를 지정 하지 않으면 파일은 하위 폴더 아래의 문서 폴더에 저장 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
데이터 조각에 대 한 활동 실행의 ID를 지정 합니다.
Get-AzDataFactoryRun cmdlet을 사용 하 여 ID를 가져옵니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -출력
다운로드 한 로그 파일이 저장 되는 출력 폴더를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 data factory를 만듭니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. 문자열

## 출력

### DataFactories를 실행 합니다. PSRunLogInfo

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[새로운 AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[제거-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[일시 중단-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


