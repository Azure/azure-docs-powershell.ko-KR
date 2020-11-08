---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045794"
---
# Set-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필의 속성을 업데이트 합니다.

## 구문과

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureTrafficManagerProfile** Cmdlet은 Microsoft Azure Traffic Manager 프로필의 속성을 업데이트 합니다.

*LoadBalancingMethod* 값을 "장애 조치"로 설정한 프로필의 경우 Add-AzureTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 추가한 끝점의 장애 조치 순서를 확인할 수 있습니다.
자세한 내용은 아래 예제 3을 참조 하세요.

## 예제의

### 예제 1: Traffic Manager 프로필의 TTL 설정
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

이 명령은 Traffic Manager 프로필 개체 MyTrafficManagerProfile에 대 한 TTL을 60 초로 설정 합니다.

### 예제 2: 프로필에 여러 값 설정
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

이 명령은 **AzureTrafficManagerProfile** cmdlet을 사용 하 여 myprofile 이라는 Traffic Manager 프로필을 가져옵니다.
프로필은 RoundRobin 부하 분산 방법, 30 초의 TTL, 모니터 프로토콜 HTTP, 모니터 포트, Traffic Manager 프로필에 대 한 상대 경로를 사용 합니다.

### 예제 3: 원하는 장애 조치 순서에 따라 끝점 순서 변경
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

이 예제에서는 MyProfile에 추가한 끝점을 원하는 장애 조치 순서에 따라 순서를 재정리 합니다.

첫 번째 명령은 MyProfile 이라는 트래픽 관리자 프로필 개체를 가져와 개체를 $Profile 변수에 저장 합니다.

두 번째 명령은 끝점 배열의 끝점을 장애 조치 발생 순서에 따라 다시 정렬 합니다.

마지막 명령은 새 끝점 순서를 사용 하 여 $Profile에 저장 된 Traffic Manager 프로필을 업데이트 합니다.

## 변수

### -LoadBalancingMethod
연결을 배포 하는 데 사용할 부하 분산 방법을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 성능을
- 장애 조치
- RoundRobin

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

### -모니터 포트
끝점 상태를 모니터링 하는 데 사용 되는 포트를 지정 합니다.
유효한 값은 0 보다 크고 65535 보다 작거나 같은 정수 값입니다.

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

### -모니터 프로토콜
끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.
유효한 값은 다음과 같습니다. 

- Http
- Https

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

### -MonitorRelativePath
상태를 검색 하기 위해 끝점 도메인 이름에 상대적인 경로를 지정 합니다.
경로는 다음 제한을 충족 해야 합니다. 

- 경로는 1 ~ 1000 자 여야 합니다.
- 슬래시,/으로 시작 해야 합니다.
- XML 요소를 포함 하지 않아야 \<\> 합니다.
- 이중 슬래시,//를 포함 하지 않아야 합니다.
- 잘못 된 HTML 이스케이프 문자가 포함 되어 있어야 합니다.
예를 들면% XY입니다.

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

### -이름
업데이트할 Traffic Manager 프로필의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -TrafficManagerProfile
프로필을 설정 하는 데 사용 하는 Traffic Manager 프로필 개체를 지정 합니다.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Ttl
DNS 항목을 캐시할 수 있는 시간을 로컬 DNS 확인자에 알리는 DNS TTL (Time to Live)을 지정 합니다.
유효한 값은 30부터 999999 까지의 정수입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition
이 cmdlet은 Traffic Manager 프로필 개체를 생성 합니다.

## 상속자

## 관련 링크

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[새로운 AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[제거-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


