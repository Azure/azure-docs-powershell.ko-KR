---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529028"
---
# Get-AzureRmBackupJob

## SYNOPSIS
백업 작업을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### FiltersSet (기본값)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Joblistfilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmBackupJob** cmdlet은 특정 자격 증명 모음에 대 한 Azure 백업 작업을 가져옵니다.

## 예제의

### 예제 1: 백업 자격 증명 모음의 모든 작업 가져오기
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.
명령이 $Vault 변수에 해당 개체를 저장 합니다.

두 번째 명령은 $Vault의 자격 증명 모음에 대 한 모든 작업을 가져옵니다.

### 예제 2: 완료 된 작업 가져오기
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

이 명령은 $Vault의 자격 증명 모음에서 완료 된 작업을 가져옵니다.

### 예제 3: 지난 주에 실패 한 작업 가져오기
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

이 명령은 $Vault의 자격 증명 모음에서 지난 주에 실패 한 작업을 가져옵니다.
*From* 매개 변수는 지난 7 일의 시간을 지정 합니다.
명령에서 *To* 매개 변수에 대 한 값을 지정 하지 않습니다.
따라서 현재 시간에 대 한 기본값을 사용 합니다.

### 예제 4: 완료 되는 진행 중인 작업에 대 한 백업 폴링
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.

스크립트의 첫 번째 줄은 진행 중인 $Vault의 모든 작업을 가져온 다음 해당 작업을 $Jobs 배열 변수에 저장 합니다.

두 번째 줄은 $Jobs 배열의 첫 번째 작업을 $Job 변수에 저장 합니다.

세 번째 줄은 작업이 완료 될 때까지 작업의 현재 상태를 확인 하는 **while** 루프를 시작 합니다.
**While** 키워드에 대 한 자세한 내용은를 입력 `Get-Help about_While` 합니다.

**While** 루프는 콘솔에 메시지를 기록 하 고 10 초 동안 대기한 다음 $Job 변수를 업데이트 합니다.
이 스크립트는 기존 $Job 값을 사용 하 여 $Job 변수를 업데이트 하 고 현재 cmdlet을 통해 작업의 현재 상태를 가져옵니다.
Windows PowerShell cmdlet에 대 한 자세한 내용은 및를 입력 `Get-Help Write-Host` `Get-Help Start-Sleep` 합니다.

스크립트의 마지막 줄에서 스크립트가 완료 되었음을 알 수 있습니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -보낸 사람
이 cmdlet이 가져오는 작업에 대 한 시간 범위의 시작을 **DateTime** 개체로 지정 합니다.
**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.
**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -작업
이 cmdlet이 가져오는 작업을 지정 합니다.
**AzureRmBackupJob** 개체를 가져오려면 Get-AzureRmBackupJob cmdlet을 사용 합니다.

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
이 cmdlet이 가져오는 작업의 ID를 지정 합니다.
ID는 **AzureRmBackupJob** 개체의 **InstanceId** 속성입니다.
**AzureRmBackupJob** 개체를 얻으려면 AzureRmBackupJob를 사용 합니다.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -작업
이 cmdlet이 가져오는 작업의 연산을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 백업할 
- ConfigureBackup 
- DeleteBackupData 
- 등록이 
- 복원한 
- 문서 
- 을

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -상태
이 cmdlet이 가져오는 작업의 상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- InProgress
- 못함
- 되었습니다
- ...
- 완료
- CompletedWithWarnings 

이 매개 변수를 지정 하 여 진행 중인 모든 작업 또는 실패 한 모든 작업을 찾을 수 있습니다.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
이 cmdlet이 가져오는 작업에 대 한 시간 범위의 끝을 **DateTime** 개체로 지정 합니다.
기본값은 현재 시스템 시간입니다.
이 매개 변수를 지정 하는 경우에도 *From* 매개 변수를 지정 해야 합니다.

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
이 cmdlet이 백업 작업을 가져오는 컨테이너 유형을 지정 합니다.
현재만 지원 되는 값은 Add-azurevm입니다.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -저장실
이 cmdlet이 작업을 가져오는 백업 자격 증명 모음을 지정 합니다.
**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### AzureRmBackupVault

## 출력

### AzureRmBackupJob[]
이 cmdlet은 하나 이상의 백업 작업을 반환 합니다.

## 상속자
* 않아야

## 관련 링크

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[중지-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


