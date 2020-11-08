---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046467"
---
# Remove-AzureStorSimpleDeviceBackup

## SYNOPSIS
백업 개체를 삭제 합니다.

## 구문과

### IdentifyById (기본값)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Remove-AzureStorSimpleDeviceBackup** cmdlet은 단일 백업 개체를 삭제 합니다.
이미 삭제 된 백업을 삭제 하려고 하면이 cmdlet은 오류를 반환 합니다.

## 예제의

### 예제 1: 장치에 대 한 백업 제거
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

이 명령은 Contoso63-AppVm 이라는 장치에 대해 지정 된 ID를 가진 백업을 제거 합니다.
이 명령은 **백업** 개체를 제거 하는 작업을 시작한 다음 **taskresponse** 개체를 반환 합니다.
작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.

### 예제 2: ID를 사용 하 여 장치에 대 한 첫 번째 백업 제거
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

첫 번째 명령은 Contoso63 이라는 장치에 대 한 백업을 가져온 다음 $Backup 변수에 저장 합니다.

두 번째 명령은 Contoso63 이라는 장치에서 백업을 삭제 합니다.
이 명령은 표준 점 표기법을 사용 하 여 $Backup 배열의 첫 번째 요소의 **InstanceId** 속성을 참조 합니다.
이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.

### 예제 3: 파이프라인을 사용 하 여 디바이스의 첫 번째 백업 제거
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

첫 번째 명령은 Contoso63 이라는 장치에 대 한 백업을 가져온 다음 $Backup 변수에 저장 합니다.

두 번째 명령은 $Backup 배열에 저장 된 첫 번째 개체를 현재 cmdlet에 전달 합니다.
해당 cmdlet은 Contoso63 이라는 장치에서 해당 백업을 삭제 합니다.
이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.

## 변수

### -백업
삭제할 **백업** 개체를 지정 합니다.
**백업** 개체를 얻으려면 **Get-AzureStorSimpleDeviceBackup** cmdlet을 사용 합니다.

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupId
삭제할 백업의 인스턴스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -장치 이름
백업을 삭제할 StorSimple 장치의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
Azure 프로필을 지정 합니다.

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

### -WaitForComplete
이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.

```yaml
Type: SwitchParameter
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

### 백업할

## 출력

### TaskStatusInfo, TaskResponse
이 cmdlet은 *Waitforcomplete* 매개 변수를 지정 하지 않으면 **TaskStatusInfo** 개체를 반환 합니다. 해당 매개 변수를 지정 하지 않으면 **taskresponse** 개체를 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


