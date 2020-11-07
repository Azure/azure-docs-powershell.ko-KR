---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876990"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
가상 컴퓨터에 자동으로 패치할 구성 개체를 만듭니다.

## 구문과

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## 설명은
**AzVMSqlServerAutoPatchingConfig** cmdlet은 가상 컴퓨터에 자동으로 패치를 적용 하기 위한 구성 개체를 만듭니다.

## 예제의

### 예제 1: 자동 패치를 구성 하는 구성 개체 만들기
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

이 명령은 패칭에 대 한 구성 개체를 만듭니다.
이 명령은 요일을 지정 하 고 유지 관리 기간을 정의 합니다.
이 구성은 이러한 값을 사용 하는 패치를 사용 하도록 설정 합니다.
명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.
Set-AzVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.

## 변수

### -DayOfWeek
업데이트를 설치 해야 하는 요일을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 나타내고
- 월요일
- 시간은
- 일
- 목요일
- 금요일
- 토요일
- 매일

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용
가상 컴퓨터에 대 한 자동 패치가 활성화 되어 있음을 나타냅니다.
자동 패치를 사용 하도록 설정 하면 cmdlet이 Windows Update를 대화형 모드로 전환 합니다.
자동 패치를 사용 하지 않도록 설정 하는 경우 Windows 업데이트 설정이 변경 되지 않습니다.

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

### -MaintenanceWindowDuration
유지 관리 기간의 기간 (분)을 지정 합니다.
자동화 된 패치는 해당 창 외부의 가상 컴퓨터 가용성에 영향을 줄 수 있는 작업을 수행 하지 않도록 방지 합니다.
30 분의 배수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
유지 관리 기간이 시작 되는 시간 (일)을 지정 합니다.
이 시간은 업데이트가 설치 되기 시작 하는 시기를 정의 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
중요 업데이트를 포함 해야 하는지 여부를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### AutoPatchingSettings
이 cmdlet은 자동 패칭에 대 한 설정을 포함 하는 개체를 반환 합니다.

## 상속자

## 관련 링크

[새로운 AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


