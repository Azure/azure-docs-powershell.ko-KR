---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046191"
---
# New-AzureVMSqlServerAutoPatchingConfig

## SYNOPSIS
가상 컴퓨터 자동 패칭에 대 한 구성 개체를 만듭니다.

## 구문과

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureVMSqlServerAutoPatchingConfig** cmdlet은 가상 컴퓨터 자동 패칭에 대 한 구성 개체를 만듭니다.

## 예제의

### 예제 1: 자동 패치를 구성 하는 구성 개체 만들기
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

이 명령은 Set-AzureVMSqlServerExtension를 사용 하 여 자동 패치를 구성 하는 데 사용할 수 있는 구성 개체를 만듭니다.

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용
가상 컴퓨터에 대 한 자동 패치가 활성화 되어 있음을 나타냅니다.
자동 패치 기능을 사용 하도록 설정 하면 cmdlet에서 Windows 업데이트를 대화형 모드로 전환 합니다.
자동 패치를 사용 하지 않도록 설정 하면 Windows 업데이트 설정이 변경 되지 않습니다.

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

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
유지 관리 창의 기간을 지정 합니다.
자동화 된 패치는 해당 창 외부의 가상 컴퓨터 가용성에 영향을 줄 수 있는 작업을 수행 하지 않도록 합니다.
30 분 단위로만 증가할 수 있습니다.

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
이번에는 업데이트 설치가 시작 되는 시간과 시간으로 반올림 되는 시간을 정의 합니다.

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### AutoPatchingSettings
이 cmdlet은 자동 패칭에 대 한 설정을 포함 하는 개체를 반환 합니다.

## 상속자

## 관련 링크

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[제거-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


