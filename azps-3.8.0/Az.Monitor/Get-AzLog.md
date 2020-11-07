---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: f6d0181562d9d43c12fbcfd046350e9d930f2320
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877357"
---
# Get-AzLog

## SYNOPSIS
활동 로그 이벤트를 검색 합니다.

## 구문과

### GetByCorrelationId
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceId
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzLog** Cmdlet은 활동 로그 이벤트를 검색 합니다.
이벤트는 현재 구독 ID, 상관 관계 ID, 리소스 그룹, 리소스 ID 또는 리소스 공급자와 연결 될 수 있습니다.

## 예제의

### 예제 1: 구독 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 사용자의 구독 ID와 연결 된 최대 1000 이벤트를 나열 합니다.

### 예제 2: 최대 개수의 이벤트를 사용 하 여 구독 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -MaxRecord 100
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 사용자의 구독 ID와 연결 된 최대 100 이벤트를 나열 합니다.

### 예제 3: 시작 시간으로 구독 ID를 사용 하 여 이벤트 로그를 가져옵니다.
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

이 명령은 2017 년 6 월에 발생 한 사용자의 구독 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 해당 날짜/시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우 30 개의 현지 시간입니다.

### 예제 4: 시작 시간 및 종료 시간을 사용 하 여 구독 ID를 기준으로 이벤트 로그를 가져옵니다.
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

이 명령은 2017 년 4 월에 발생 한 사용자의 구독 ID와 연결 된 이벤트 (최대 1000, 현지 시간 30 개, 2017 년 4 월 1 일 이전)를 나열 합니다. 전체 날짜/시간 범위가 현재 날짜/시간 (예: 보존 기간)에서 90 일 보다 오래 된 경우에는 30 현지 시간입니다.

### 예제 5: 상관 관계 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 
**참고** :이는 일반적으로 하나의 이벤트입니다.

### 예제 6: 최대 이벤트 수를 사용 하 여 상관 관계 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 상관 관계 ID와 연결 된 최대 100 이벤트를 나열 합니다. 
**참고** :이는 일반적으로 하나의 이벤트입니다.

### 예제 7: 상관 관계 ID 및 시작 시간을 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

이 명령은 2017 년에 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우-05-22T04:30:00 현지 시간.
**참고** :이는 일반적으로 하나의 이벤트입니다.

### 예제 8: 시작 시간과 종료 시간을 사용 하 여 상관 관계 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

이 명령은 2017 년 4 월에 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 현지 시간을 보존 기간 이라고 합니다.

### 예제 9: 리소스 그룹에 대 한 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

이 명령은 1000에서 현재 날짜/시간 으로부터 7 일 동안 지정 된 리소스 그룹과 연결 된 이벤트를 나열 합니다.

### 예제 10: 최대 이벤트 수를 사용 하 여 리소스 그룹에 대 한 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

이 명령은 현재 날짜/시간 으로부터 7 일 동안 지정 된 리소스 그룹과 연결 된 100 이벤트를 모두 나열 합니다.

### 예제 11: 시작 시간별로 리소스 그룹에 대 한 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

이 명령은 2017 년에 발생 한 특정 리소스 그룹과 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.

### 예제 12: 시작 시간 및 종료 시간을 사용 하 여 리소스 그룹에 대 한 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 그룹과 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 로컬 시간 (즉, 보존 기간)

### 예제 13: 리소스 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 ID와 연결 된 최대 1000 이벤트를 나열 합니다.

### 예제 14: 최대 이벤트 수를 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 ID와 연결 된 최대 100 이벤트를 나열 합니다.

### 예제 15: 시작 시간을 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

이 명령은 2017 년에 발생 한 특정 리소스 ID와 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.

### 예제 16: 시작 시간 및 종료 시간을 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 ID와 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일이 하 인 경우: 30 현지 시간을 보존 기간 이라고 합니다.

### 예제 17: 리소스 공급자를 기준으로 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 공급자와 연결 된 1000 이벤트를 모두 나열 합니다.

### 예제 18: 최대 이벤트 수를 사용 하 여 리소스 공급자에 의해 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 공급자와 연결 된 100 이벤트를 모두 나열 합니다.

### 예제 19: 시작 시간을 사용 하 여 리소스 공급자에의 한 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

이 명령은 2017 년에 발생 한 특정 리소스 공급자와 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.

### 예제 20: 시작 시간 및 종료 시간을 사용 하 여 리소스 공급자에의 한 이벤트 로그 가져오기
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 공급자에 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하지만 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 현지 시간입니다.

## 변수

### -발신자
발신자를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CorrelationId
상관 관계 ID를 지정 합니다.
이 매개 변수는 필수입니다.

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -DetailedOutput
이 cmdlet에 자세한 출력이 표시 됨을 나타냅니다.
기본적으로 출력이 요약 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
현지 시간으로 쿼리의 종료 시간을 지정 합니다.
기본값은 현재 시간입니다.
값은 *StartTime* 보다 이후 여야 합니다.
Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 가져올 수 있습니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
지정 된 필터에 대해 반입할 총 레코드 수를 지정 합니다.
기본값은 1000이 고 최대 허용 값은 10만입니다. 음수 값과 0은 무시 되 고 기본값을 사용 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
리소스 공급자별 필터를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
현지 시간으로 쿼리의 시작 시간을 지정 합니다.
기본값은 *EndTime* 에서 7 일을 뺀 값입니다.
Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 가져올 수 있습니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
상태를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### System. 문자열

### System.webserver 매개 변수

### 시스템. i i.

## 출력

### PSEventData를 통해 출력 합니다.

## 상속자

## 관련 링크
