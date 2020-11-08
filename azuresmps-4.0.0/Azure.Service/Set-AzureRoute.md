---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045823"
---
# Set-AzureRoute

## SYNOPSIS
경로 테이블에 경로를 만듭니다.

## 구문과

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Set-AzureRoute** cmdlet은 경로 테이블에 경로를 만듭니다.
새 경로는 경로 테이블과 연결 된 가상 컴퓨터 바로 다음에 적용 됩니다.

## 예제의

### 예제 1: 가상 기기 다음 홉 경로 추가
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

이 명령은 지정 된 위치에 ApplianceRouteTable 이라는 경로 테이블을 만듭니다.
명령이 현재 cmdlet에 경로 테이블을 전달 합니다.
현재 cmdlet은 VirtualAppliance 다음 홉 유형인 ApplianceRoute03 이라는 경로를 추가 합니다.
이 명령은 경로의 다음 홉 IP 주소와 주소 접두사를 지정 합니다.

### 예제 2: 인터넷 다음 홉 경로 추가
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

이 명령은 ApplianceRouteTable 이라는 경로 테이블을 가져옵니다.
명령이 현재 cmdlet에 경로 테이블을 전달 합니다.
현재 cmdlet은 인터넷 다음 홉 유형인 InternetRoute 라는 경로를 추가 합니다.
명령은 경로에 대 한 주소 접두사를 지정 합니다.

## 변수

### -AddressPrefix
새 경로의 주소 접두사를 지정 합니다.

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

### -NextHopIpAddress
이 경로를 사용 하는 트래픽에 대 한 다음 홉 인 기기의 IP 주소를 지정 합니다.
*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 값을 지정 합니다.

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

### -NextHopType
이 경로를 사용 하는 트래픽에 대 한 다음 홉 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 

- VPNGateway
- VNETLocal
- 인터넷
- VirtualAppliance
- L

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

### -RouteName
이 cmdlet에 추가 되는 새 경로의 이름을 지정 합니다.

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

### -RouteTable
이 cmdlet이 새 경로를 추가 하는 경로 테이블을 지정 합니다.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[제거-AzureRoute](./Remove-AzureRoute.md)


