---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045552"
---
# Get-AzureStorSimpleTask

## SYNOPSIS
StorSimple 장치에서 작업의 상태를 가져옵니다.

## 구문과

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-AzureStorSimpleTask** Cmdlet는 Azure StorSimple 장치에서 비동기적으로 실행 되는 작업의 상태를 검색 합니다.

StorSimple 장치를 관리 하는 동안 대부분의 만들기, 읽기, 업데이트 및 삭제 작업이 비동기적으로 실행 될 수 있습니다.
Windows PowerShell은 **TaskId** 를 반환 합니다.
ID를 사용 하 여 작업의 현재 상태를 가져옵니다.

## 예제의

### 예제 1: 작업 상태 가져오기
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

이 명령은 지정 된 ID를 가진 작업의 상태를 가져옵니다.
결과에는 해당 작업의 상태가 완료 됨과 성공한 결과가 표시 됩니다.

## 변수

### -InstanceId
이 cmdlet이 상태를 추적 하는 작업의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### JobStatusInfo
이 cmdlet은 다음 필드를 포함 하는 **TaskStatusInfo** 개체를 반환 합니다. 

- **오류가 발생 했습니다**.
**코드** 와 **메시지가** 포함 된 **errordetails**.
- **TaskId**.
**문자열** 입니다.
상태가 반환 되는 작업의 ID입니다.
- **Tasksteps**.
**IList \<TaskStep\>**.
각 **Taskstep** 개체에는 **세부 정보** , **ErrorCode** , **메시지** , **결과** , **상태가** 포함 됩니다.
- **결과**.
작업의 전체 결과를 포함 하는 **Taskresult** 입니다.
유효한 값은 Failed, Succeeded, PartialSuccess, 취소 됨, 유효 하지 않음입니다.
- **상태** 입니다.
작업의 전체 실행 상태가 포함 된 **Taskstatus** 입니다.
유효한 값은 Inprogress, 유효 하지 않음, 완료 됨입니다.
- **Taskresult**.
**Taskresult** , **결과** 및 **상태** 를 기반으로 계산 되는 값입니다.
유효한 값은 Failed, Succeeded, InProgress, PartialSuccess, 취소 됨, 유효 하지 않음입니다.

## 상속자

## 관련 링크

