---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 2a1dbf5eea7f772a7819ed341a681adc24134225
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881957"
---
# Set-AzureRmVMSqlServerExtension

## SYNOPSIS
가상 컴퓨터에서 Azure SQL Server 확장을 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVMSqlServerExtension** cmdlet은 가상 컴퓨터의 AzureSQL Server 확장을 설정 합니다.

## 예제의

### 예제 1: 가상 컴퓨터에서 자동 패치 설정 설정
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

첫 번째 명령은 **New AzureVMSqlServerAutoPatchingConfig** cmdlet을 사용 하 여 구성 개체를 만듭니다.
명령은 $AutoPatchingConfig 변수에 구성을 저장 합니다.

두 번째 명령은 Get-AzureRmVM cmdlet을 사용 하 여 Service02 이라는 서비스에서 VirtualMachine11 라는 가상 컴퓨터를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.

현재 cmdlet은 가상 컴퓨터에 대 한 $AutoPatchingConfig에서 자동 패치 설정을 설정 합니다.
명령이 가상 컴퓨터를 Update-AzureRmVM cmdlet에 전달 합니다.

### 예제 2: 가상 컴퓨터에서 자동 백업 설정 설정
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

첫 번째 명령은 **New AzureVMSqlServerAutoBackupConfig** cmdlet을 사용 하 여 구성 개체를 만듭니다.
명령은 $AutoBackupConfig 변수에 구성을 저장 합니다.

두 번째 명령은 Service02 이라는 서비스에서 VirtualMachine11 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.

현재 cmdlet은 가상 컴퓨터에 대 한 $AutoBackupConfig에서 자동 백업 설정을 설정 합니다.
명령이 가상 컴퓨터를 Update-AzureRmVM cmdlet에 전달 합니다.

### 예제 3: 가상 컴퓨터에서 SQL Server 확장 사용 안 함
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

이 명령은 Service03에 VirtualMachine08 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.
이 명령은 해당 가상 컴퓨터에서 SQL Server 가상 컴퓨터 확장을 사용 하지 않도록 설정 합니다.

### 예제 4: 특정 가상 컴퓨터에서 SQL Server 확장 제거
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

이 명령은 Service03에 VirtualMachine08 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.
명령에서 해당 가상 컴퓨터의 SQL Server 가상 컴퓨터 확장을 제거 합니다.

## 변수

### -AutoBackupSettings
SQL Server 자동 백업 설정을 지정 합니다.
**AutoBackupSettings** 개체를 만들려면 New-AzureVMSqlServerAutoBackupConfig cmdlet을 사용 합니다.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
SQL Server 자동 패치 설정을 지정 합니다.
**AutoPatchingSettings** 개체를 만들려면 New-AzureVMSqlServerAutoPatchingConfig cmdlet을 사용 합니다.

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
가상 컴퓨터의 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
확장 하는 SQL Server의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -버전
SQL Server 확장 버전을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
이 cmdlet에서 SQL Server 확장을 설정 하는 가상 컴퓨터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### 이는 PSAzureOperationResponse를 계산 하는 명령입니다.

## 상속자

## 관련 링크

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMSqlServerExtension](./Get-AzureRMVMSqlServerExtension.md)





[제거-AzureRmVMSqlServerExtension](./Remove-AzureRMVMSqlServerExtension.md)

[업데이트-AzureRmVM](./Update-AzureRmVM.md)


