---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525315"
---
# New-AzureVMSqlServerAutoBackupConfig

## SYNOPSIS
SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### StorageUriSqlServerAutoBackup (기본값)
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## 설명은
**AzureVMSqlServerAutoBackupConfig** CMDLET은 SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.

## 예제의

### 예제 1: 저장소 URI 및 계정 키를 사용 하 여 자동 백업 구성 만들기
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

이 명령은 저장소 URI 및 계정 키를 지정 하 여 자동 백업 구성 개체를 만듭니다.
자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.
명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.
Set-AzureRmVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.

### 예제 2: 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

첫 번째 명령은 저장소 컨텍스트를 만든 다음 $StorageContext 변수에 저장 합니다.
자세한 내용은 새 AzureStorageContext를 참조 하세요.

두 번째 명령은 $StorageContext에서 저장소 컨텍스트를 지정 하 여 자동 백업 구성 개체를 만듭니다.
자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.

### 예제 3: 암호화 및 암호를 사용 하 여 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

이 명령은 자동 백업 구성 개체를 만들고 저장 합니다.
명령은 이전 예제에서 만든 저장소 컨텍스트를 지정 합니다.
명령이 암호로 암호화를 사용 하도록 설정 합니다.
암호가 이전에 $CertificatePassword 변수에 보안 문자열로 저장 되었습니다.
보안 문자열을 만들려면 ConvertTo-SecureString cmdlet을 사용 합니다.

## 변수

### -BackupScheduleType
백업 일정 유형, 수동 또는 자동

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
시스템 데이터베이스 백업

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
SQL Server 암호화 백업을 수행 하는 데 사용 되는 인증서를 암호화 하는 암호를 지정 합니다.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용
SQL Server 가상 컴퓨터에 대해 자동화 된 백업을 사용할 수 있음을 나타냅니다.
이 매개 변수를 지정 하면 자동 백업이 모든 현재 및 새 데이터베이스에 대 한 백업 일정을 설정 합니다.
이렇게 하면 관리 되는 백업 설정이 다음 일정을 따라 업데이트 됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
이 cmdlet이 암호화를 사용 하도록 설정 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Sql Server 전체 백업 빈도 (매일 또는 매주)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Fullbackupstarth
Sql Server 전체 백업을 시작 해야 하는 날짜의 시간 (0-23)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Sql Server 전체 백업 창 (시간)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
Sql Server 로그 백업 빈도 (1-60 분 마다 한 번)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
백업을 유지할 일 수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
백업을 저장 하는 데 사용 되는 저장소 계정을 지정 합니다.
**Azurestoragecontext** 개체를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.
기본값은 SQL Server 가상 컴퓨터와 연결 된 저장소 계정입니다.

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Blob 저장소 계정의 저장소 키를 지정 합니다.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Blob 저장소 계정의 URI (Uniform Resource Identifier)를 지정 합니다.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

## 상속자

## 관련 링크

[새로운 AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


