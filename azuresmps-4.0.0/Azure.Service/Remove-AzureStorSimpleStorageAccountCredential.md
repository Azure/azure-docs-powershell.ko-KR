---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046449"
---
# Remove-AzureStorSimpleStorageAccountCredential

## SYNOPSIS
기존 저장소 계정 자격 증명을 삭제 합니다.

## 구문과

### IdentifyByName
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**제거-AzureStorSimpleStorageAccountCredential** cmdlet은 기존 저장소 계정 자격 증명을 삭제 합니다.
이름을 기준으로 계정을 지정 하거나 **Get-AzureStorSimpleStorageAccountCredential** cmdlet을 사용 하 여 삭제할 **storageaccountcredential** 개체를 가져옵니다.

## 예제의

### 예제 1: 저장소 계정 자격 증명 제거
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

이 명령은 ContosoStorage07 이라는 저장소 계정에 대 한 계정 자격 증명을 제거 합니다.
이 명령은 *Force* 매개 변수를 지정 합니다.
Cmdlet은 확인 메시지를 표시 하지 않고 자격 증명을 제거 합니다.

### 예제 2: 파이프라인 연산자를 사용 하 여 저장소 계정 자격 증명 제거
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

이 명령은 **Get-Azurestorsimplestoragecredential** cmdlet을 사용 하 여 ContosoStorage07 이라는 저장소 계정을 가져온 다음 현재 cmdlet에 해당 개체를 전달 합니다.
현재 cmdlet은 해당 저장소 계정에 대 한 자격 증명을 제거 합니다.
이 명령은 *Waitforcomplete* 매개 변수를 지정 합니다.
Cmdlet은 제거 작업을 완료할 때까지 콘솔에 컨트롤을 반환 하지 않습니다.

## 변수

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

### -SAC
제거할 **Storageaccountcredential** 개체로 자격 증명을 지정 합니다.
**Storageaccountcredential** 개체를 가져오려면 **Get-AzureStorSimpleStorageAccountCredential** cmdlet을 사용 합니다.

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
삭제할 저장소 계정 자격 증명의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
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

### StorageAccountCredential
이 cmdlet은 파이프라인을 사용 하 여 **Storageaccountcredential** 개체를 받아들입니다.

## 출력

### TaskStatusInfo
*Waitforcomplete* 매개 변수를 지정 하는 경우이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleStorageAccountCredential](./Get-AzureStorSimpleStorageAccountCredential.md)

[새-AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[Set-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


