---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045434"
---
# Set-AzureTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 프로필에서 끝점의 속성을 업데이트 합니다.

## 구문과

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureTrafficManagerEndpoint** Cmdlet은 Microsoft Azure Traffic Manager 프로필의 끝점 속성을 업데이트 합니다.
끝점이 현재 프로필에 없으면이 cmdlet이 끝점을 만듭니다.
끝점을 추가한 후 파이프라인 연산자를 사용 하 여 결과를 **Set-AzureTrafficManagerProfile** cmdlet에 전달 합니다.
해당 cmdlet이 Azure에 연결 하 여 변경 내용을 저장 합니다.

## 예제의

### 예제 1: 프로필의 끝점 업데이트
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

첫 번째 명령은 **AzureTrafficManagerProfile** cmdlet을 사용 하 여 ContosoProfile 이라는 프로필을 가져오고이를 $TrafficManagerProfile 변수에 저장 합니다.

두 번째 명령은 $TrafficManagerProfile에 저장 된 Traffic Manager 프로필의 끝점을 업데이트 합니다.
끝점에는 도메인 이름 ContosoApp02.cloudapp.net 있습니다.
또한이 명령은 끝점의 상태, 형식, 두께 및 위치를 지정 합니다.
이 명령은 수정 된 프로필을 **Set-AzureTrafficManagerProfile** cmdlet에 전달 하 여 Azure에 연결 하 여 변경 내용을 저장 합니다.

## 변수

### -DomainName
수정할 끝점의 도메인 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
Cmdlet이 추가 하는 끝점의 위치를 지정 합니다.
Azure 위치 여야 합니다.

이 매개 변수는 부하 분산 메서드가 "성능"으로 설정 된 프로필에서 "모든" 또는 "TrafficManager" 형식의 끝점에 대 한 값을 포함 해야 합니다.
사용할 수 있는 값은 Azure 지역 이름에 나열 되어  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ 있습니다.

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

### -MinChildEndpoints
이 끝점을 온라인으로 간주 하기 위해 중첩 된 프로필이 온라인 상태 여야 하는 최소 끝점 수를 지정 합니다.

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

### -상태
모니터링 끝점의 상태를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 수
- 비활성화

사용 값을 지정 하면 트래픽 관리자가 끝점을 모니터링 하 고 부하 분산 메서드는 트래픽을 관리할 때이를 고려 합니다.

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

### -TrafficManagerProfile
끝점을 수정할 Traffic Manager 프로필 개체를 지정 합니다.

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

### -Type
끝점 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 

- CloudService
- AzureWebsite
- TrafficManager

- 이상 

둘 이상의 AzureWebsite 끝점을 사용할 경우 끝점은 서로 다른 데이터 센터에 있어야 합니다.

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

### -중량
Cmdlet이 추가 하는 끝점의 두께를 지정 합니다.
이 매개 변수의 유효한 값 범위는 \[ 1, 1000 \] 입니다.

이 매개 변수는 RoundRobin 부하 분산 정책에만 사용 됩니다.

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
이 cmdlet은 업데이트 된 프로필에 대 한 정보를 포함 하는 Traffic Manager 프로필 개체를 생성 합니다.

## 상속자

## 관련 링크

[추가-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[제거-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


