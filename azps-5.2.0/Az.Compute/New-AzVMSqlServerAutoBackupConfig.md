---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 952a9160a20492fe49e7f79019ca68e3bc241e57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331370"
---
# New-AzVMSqlServerAutoBackupConfig

## SYNOPSIS
자동 백업에 대한 SQL Server 만듭니다.

## 구문

### StorageUriSqlServerAutoBackup(기본값)
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzVMSqlServerAutoBackupConfig** cmdlet은 자동 백업에 대한 SQL Server 만듭니다.

## 예제

### 예제 1: 저장소 URI 및 계정 키를 사용하여 자동 백업 구성 만들기
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

이 명령은 저장소 URI 및 계정 키를 지정하여 자동 백업 구성 개체를 만듭니다.
자동 백업이 사용하도록 설정되어 있으며 자동 백업은 10일 동안 유지됩니다.
이 명령은 결과 값을 $AutoBackupConfig 저장합니다.
Set-AzVMSqlServerExtension cmdlet과 같은 다른 cmdlet에 대해 이 구성 항목을 지정할 수 있습니다.

### 예제 2: 저장소 컨텍스트를 사용하여 자동 백업 구성 만들기
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

첫 번째 명령은 저장소 컨텍스트를 만든 다음 저장소 $StorageContext 저장합니다.
자세한 내용은 New-AzStorageContext를 참조하세요.
두 번째 명령은 저장소 컨텍스트를 지정하여 자동 백업 구성 개체를 $StorageContext.
자동 백업이 사용하도록 설정되어 있으며 자동 백업은 10일 동안 유지됩니다.

### 예제 3: 암호화 및 암호가 있는 저장소 컨텍스트를 사용하여 자동 백업 구성 만들기
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

이 명령은 자동 백업 구성 개체를 만들고 저장합니다.
이 명령은 이전 예제에서 만든 저장소 컨텍스트를 지정합니다.
이 명령은 암호로 암호화를 사용할 수 있습니다.
암호는 이전에 $CertificatePassword 변수에 보안 문자열로 $CertificatePassword.
보안 문자열을 만들 경우 ConvertTo-SecureString cmdlet을 사용 합니다.

## PARAMETERS

### -BackupScheduleType
Backup 일정 유형, 수동 또는 자동화

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
암호화된 백업을 수행하는 데 사용되는 인증서를 암호화하는 SQL Server 지정합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Enable
가상 머신에 대한 자동화된 SQL Server 사용하도록 설정되어 있습니다.
이 매개 변수를 지정하는 경우 자동화된 백업은 모든 현재 및 새 데이터베이스에 대한 백업 일정을 설정합니다.
그러면 이 일정에 따라 관리되는 Backup 설정이 업데이트됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
이 cmdlet에서 암호화를 사용할 수 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Sql Server 전체 백업 빈도( 매일 또는 매주)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
Sql Server 전체 백업이 시작되는 하루 중 시간(0-23)

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Sql Server 전체 백업 창(시간)

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
Sql Server 로그 백업 빈도(1-60분마다 한 번)

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
백업을 유지할 일 수를 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
백업을 저장하는 데 사용할 저장소 계정을 지정합니다.
**AzureStorageContext** 개체를 얻습니다. New-AzStorageContext cmdlet을 사용합니다.
기본값은 가상 머신의 가상 머신과 연결된 SQL Server 계정입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Blob Storage 계정의 스토리지 키를 지정합니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Blob Storage 계정의 URI(Uniform Resource Identifier)를 지정합니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

### System.Uri

### System.Security.SecureString

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

## 참고 사항

## 관련 링크

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


