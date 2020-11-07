---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: aed780d75280f38ba8fa99052c3af0cd8bbe9612
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874401"
---
# New-AzTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필을 만듭니다.

## 구문과

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새 AzTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 만듭니다.
*Name* 매개 변수 및 필수 설정을 지정 합니다.
이 cmdlet은 새 프로필을 나타내는 local 개체를 반환 합니다.

이 cmdlet은 Traffic Manager 끝점을 구성 하지 않습니다.
Add-AzTrafficManagerEndpointConfig cmdlet을 사용 하 여 로컬 프로필 개체를 업데이트할 수 있습니다.
그런 다음 Set-AzTrafficManagerProfile cmdlet을 사용 하 여 Traffic Manager 변경 내용을 업로드 합니다.
또는 New-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 추가할 수 있습니다.

## 예제의

### 예제 1: 프로필 만들기
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

이 명령은 리소스 그룹 ResourceGroup11에서 ContosoProfile 이라는 Azure Traffic Manager 프로필을 만듭니다.
DNS FQDN은 contosoapp.trafficmanager.net입니다.

## 변수

### -CustomHeader
검색 요청에 대 한 사용자 지정 헤더 이름 및 값 쌍의 목록입니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -ExpectedStatusCodeRange
프로브 요청에 대해 예상 되는 HTTP 상태 코드 범위 목록입니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxReturn
다중값 라우팅 메서드를 사용 하 여 프로필에 대해 반환 되는 최대 응답 수입니다.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorIntervalInSeconds
트래픽 관리자가이 프로필에서 각 끝점의 상태를 확인 하는 간격 (초)입니다. 기본값은 30입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPath
끝점 상태를 모니터링 하는 데 사용 되는 경로를 지정 합니다.
끝점 도메인 이름에 상대적인 값을 지정 합니다.
이 값은 슬래시 (/)로 시작 해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -모니터 포트
끝점 상태를 모니터링 하는 데 사용 되는 TCP 포트를 지정 합니다.
유효한 값은 1부터 65535 까지의 정수입니다.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -모니터 프로토콜
끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.
유효한 값은 다음과 같습니다.

- HTTP
- HTTPS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorTimeoutInSeconds
트래픽 관리자가이 프로필의 끝점에 상태 검사에 응답할 수 있도록 허용 하는 시간 (초)입니다. 기본값은 10입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorToleratedNumberOfFailures
실패 한 연속 상태 검사 수는이 프로필의 끝점을 선언 하기 전에 트래픽 관리자 tolerates에서 다음 번의 연속 되지 않은 상태 검사 후에 성능이 저하 됩니다. 기본값은 3입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 만드는 Traffic Manager 프로필의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileStatus
프로필의 상태를 지정 합니다.
유효한 값은 사용 및 사용 안 함입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RelativeDnsName
이 트래픽 관리자 프로필이 제공 하는 상대 DNS 이름을 지정 합니다.
Traffic Manager는 Azure 트래픽 관리자가 프로필의 FQDN (정규화 된 도메인 이름)을 형성 하는 데 사용 하는 DNS 도메인 이름 및이 값을 결합 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 Traffic Manager 프로필을 만듭니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficRoutingMethod
트래픽 라우팅 방법을 지정 합니다.
이 메서드는 들어오는 DNS 쿼리에 대 한 응답으로 반환 되는 끝점 트래픽 관리자를 확인 합니다.
유효한 값은 다음과 같습니다.

- 성능을
- 중
- 중요도
- 지역을

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
TTL (Time to Live) 값을 지정 합니다.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### TrafficManager. TrafficManagerProfile/.

## 상속자

## 관련 링크

[추가-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Disable-AzTrafficManagerProfile](./Disable-AzTrafficManagerProfile.md)

[Enable-AzTrafficManagerProfile](./Enable-AzTrafficManagerProfile.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[제거-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


