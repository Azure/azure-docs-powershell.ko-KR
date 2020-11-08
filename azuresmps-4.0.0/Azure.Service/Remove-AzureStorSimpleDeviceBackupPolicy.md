---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046464"
---
# Remove-AzureStorSimpleDeviceBackupPolicy

## SYNOPSIS
기존 백업 정책을 제거 합니다.

## 구문과

### IdentifyById (기본값)
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet은 기존 **backuppolicy** 개체를 제거 합니다.
백업 정책을 제거 하면 해당 정책에 따라 더 이상 백업이 수행 되지 않습니다.
이 cmdlet는 삭제 된 정책과 연결 된 모든 일정도 삭제 합니다.

## 예제의

### 예제 1: 백업 정책 제거
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

이 명령은이 정책을 기반으로 더 이상 백업이 만들어지지 않도록 인스턴스 ID 03710b4c-82c1-40ca-be5c-40289dc49642 인 **Backuppolicy** 를 제거 합니다.
이 명령으로이 정책과 연결 된 모든 일정이 삭제 됩니다.
이 명령은 **Backuppolicy** 개체를 제거 하는 작업을 시작한 다음 **taskresponse** 개체를 반환 합니다.
작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.

### 예제 2: 장치에 대 한 백업 정책의 첫 번째 제거
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

첫 번째 명령은 Contoso63 이라는 장치에 대 한 백업 정책을 가져온 다음이를 $Policies 변수에 저장 합니다.

두 번째 명령은 Contoso63에서 첫 번째 백업 정책을 제거 합니다.
명령에서는 표준 도트 구문을 사용 하 여 $Policies에서 첫 번째 항목의 **InstanceId** 속성을 식별 합니다.
이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로 명령이 작업을 완료 한 다음 작업에 대 한 **TaskStatusInfo** 개체를 반환 합니다.

### 예제 3: 파이프라인을 사용 하 여 백업 정책 제거
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

이 명령은 **Get-AzureStorSimpleDeviceBackupPolicy** 를 사용 하 여 **backuppolicydetails** 개체를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 전달 합니다.
현재 cmdlet은 TSQAVolume01_Default 라는 백업 정책을 제거 합니다.

## 변수

### -BackupPolicy
삭제할 **Backuppolicydetails** 개체를 지정 합니다.
**Backuppolicydetails** 개체를 가져오려면 **AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 합니다.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
삭제할 **Backuppolicy** 개체의 인스턴스 ID를 지정 합니다.

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
백업 정책을 삭제할 StorSimple 장치의 이름을 지정 합니다.

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

### BackupPolicyDetails
이 cmdlet은 **Backuppolicydetails** 개체를 수락 하 여 삭제 합니다.

## 출력

### TaskStatusInfo, TaskResponse
*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.
해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[새로운 AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


