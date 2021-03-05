---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980203"
---
# Get-AzActivityLog

## SYNOPSIS
활동 로그 이벤트를 검색합니다.

## 구문

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzActivityLog cmdlet은 활동 로그 이벤트를 검색합니다. 이벤트는 현재 구독 ID, 상관 관계 ID, 리소스 그룹, 리소스 ID 또는 리소스 공급자와 연결될 수 있습니다.

## 예제

### 예제 1: 구독 ID로 이벤트 로그를 하세요.
```
PS C:\>Get-AzActivityLog
```

이 명령은 현재 날짜/시간으로부터 7일이 지난 사용자의 구독 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.

### 예제 2: 최대 이벤트 수가 있는 구독 ID로 이벤트 로그를 얻게 됩니다.
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

이 명령은 현재 날짜/시간으로부터 7일 동안 진행된 사용자의 구독 ID와 연결된 대부분의 100개 이벤트를 나열합니다.

### 예제 3: 시작 시간을 사용하여 구독 ID로 이벤트 로그를 얻습니다.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

이 명령은 해당 날짜/시간이 현재 날짜/시간보다 90일이 지난 경우 2017-06-01T10:30 로컬 시간 이후의 사용자 구독 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.

### 예제 4: 시작 시간 및 종료 시간을 사용하여 구독 ID로 이벤트 로그를 얻습니다.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

이 명령은 2017-04-01T10:30 로컬 시간 또는 2017-04-14T11:30 이전 날짜/시간 범위가 현재 날짜/시간의 90일보다 오래되지 않은 경우 사용자의 구독 ID와 연결된 이벤트의 대부분을 나열합니다.

### 예제 5: 상관 관계 ID로 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

이 명령은 현재 날짜/시간에서 7일 동안 일어났습니다. 
**참고**: 일반적으로 하나의 이벤트입니다.

### 예제 6: 최대 이벤트 수가 있는 상관 관계 ID로 이벤트 로그를 얻게 됩니다.
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 상관 관계 ID와 연결된 100개 이벤트가 나열됩니다. 
**참고**: 일반적으로 하나의 이벤트입니다.

### 예제 7: 상관 관계 ID로 이벤트 로그 및 시작 시간 확인
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 상관 관계 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.
**참고**: 일반적으로 하나의 이벤트입니다.

### 예제 8: 시작 시간 및 종료 시간과 상관 관계 ID로 이벤트 로그를 얻
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

이 명령은 2017-04-15T04:30 로컬 시간 이전이나 2017-04-25T12:30 이전의 지정된 상관 관계 ID와 관련된 대부분의 1000개 이벤트를 나열합니다. 즉, 전체 날짜/시간 범위가 현재 날짜/시간에서 90일을 넘지 않는 경우 로컬 시간입니다.

### 예제 9: 리소스 그룹에 대한 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

이 명령은 현재 날짜/시간으로부터 7일 동안 일어났습니다.

### 예제 10: 최대 이벤트 수가 있는 리소스 그룹에 대한 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

이 명령은 현재 날짜/시간으로부터 7일 동안 일어났습니다.

### 예제 11: 시작 시간으로 리소스 그룹에 대한 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 리소스 그룹과 연결된 대부분의 1000개 이벤트를 나열합니다.

### 예제 12: 시작 시간 및 종료 시간이 있는 리소스 그룹에 대한 이벤트 로그를 얻
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

이 명령은 2017-04-15T04:30 로컬 시간 이전의 지정된 리소스 그룹과 연결된 대부분의 1000개 이벤트를 나열합니다. 전체 날짜/시간 범위가 현재 날짜/시간의 90일보다 오래되지 않은 경우 2017-04-25T12:30 로컬 시간 이전의 기간입니다.

### 예제 13: 리소스 ID로 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

이 명령은 현재 날짜/시간으로부터 7일 동안 일어났습니다.

### 예제 14: 최대 이벤트 수가 있는 리소스 ID로 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 리소스 ID와 연결된 대부분의 100개 이벤트를 나열합니다.

### 예제 15: 시작 시간을 사용하여 리소스 ID로 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 리소스 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.

### 예제 16: 시작 시간 및 종료 시간을 사용하여 리소스 ID로 이벤트 로그를 얻
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

이 명령은 2017-04-15T04:30 로컬 시간 이전이나 2017-04-25T12:30 이전의 지정된 리소스 ID와 연결된 대부분의 1000개 이벤트가 나열됩니다.

### 예제 17: 리소스 공급자에 의해 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 리소스 공급자와 연결된 대부분의 1000개 이벤트를 나열합니다.

### 예제 18: 최대 이벤트 수를 사용하여 리소스 공급자에 의해 이벤트 로그를 얻게 됩니다.
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 리소스 공급자와 연결된 대부분의 100개 이벤트를 나열합니다.

### 예제 19: 시작 시간을 사용하여 리소스 공급자에 의해 이벤트 로그를 얻다
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 리소스 공급자와 연결된 대부분의 1000개 이벤트를 나열합니다.

### 예제 20: 시작 시간 및 종료 시간을 사용하여 리소스 공급자에 의해 이벤트 로그를 얻게 됩니다.
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

이 명령은 2017-04-15T04:30 로컬 시간 이후에 일어났지만 전체 날짜/시간 범위가 현재 날짜/시간의 90일보다 오래되지 않은 경우 2017-04-25T12:30 로컬 시간 이전의 지정된 리소스 공급자와 연결된 대부분의 1000개 이벤트를 나열합니다.

## 매개 변수

### -Caller
인치할 이벤트의 호출자

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
The CorrelationId

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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
이벤트의 모든 세부 정보가 있는 개체를 반환합니다(기본값은 일부 특성만 반환하는 것입니다. 예: 세부 정보 없음).

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
쿼리의 endTime

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
인출할 레코드의 최대 수입니다.
별칭: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

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
The ResourceId

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
ResourceProvider 이름

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
쿼리의 상관 관계Id

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
인치할 이벤트의 상태

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## 출력

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## 참고 사항

## 관련 링크
