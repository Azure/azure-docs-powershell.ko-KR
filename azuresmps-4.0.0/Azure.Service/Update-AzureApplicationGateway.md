---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045844"
---
# Update-AzureApplicationGateway

## SYNOPSIS
응용 프로그램 게이트웨이를 업데이트 합니다.

## 구문과

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**업데이트-AzureApplicationGateway** cmdlet이 기존 application gateway를 업데이트 합니다.

## 예제의

### 예제 1: 이름을 사용 하 여 응용 프로그램 게이트웨이 수정
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

첫 번째 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 중지 합니다.
가상 네트워크 또는 서브넷을 수정할 수 있으려면 먼저 응용 프로그램 게이트웨이를 중지 해야 합니다.

두 번째 명령은 ApplicationGateway06 라는 응용 프로그램 게이트웨이의 가상 서브넷과 서브넷을 수정 합니다.

### 예제 2: 응용 프로그램 게이트웨이의 추가 속성 수정
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이에 대 한 인스턴스 수, 게이트웨이 크기 및 설명을 수정 합니다.
이 명령은 application gateway에 대 한 가상 네트워크 또는 서브넷을 수정 하지 않습니다.
따라서이 명령을 실행 하기 전에 응용 프로그램 게이트웨이를 중지할 필요가 없습니다.

### 예제 3: 파이프라인을 사용 하 여 응용 프로그램 게이트웨이 수정
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

첫 번째 명령은 **Get-AzureApplicationGateway** cmdlet을 사용 하 여 ApplicationGateway06 라는 응용 프로그램 게이트웨이를 가져옵니다.
명령이 $ApplicationGateway 변수에 저장 합니다.

두 번째 명령은 값 매체에 대 한. m **size** 속성을 할당 합니다.

마지막 명령은 현재 cmdlet에 업데이트 된 $ApplicationGateway을 전달 합니다.

## 변수

### -설명
이 cmdlet가 응용 프로그램 게이트웨이에 할당 하는 설명을 지정 합니다.

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

### --게이트웨이 크기
이 cmdlet이 응용 프로그램 게이트웨이에 할당 하는 크기를 지정 합니다.
유효한 값은 다음과 같습니다.

- Small
- 높음이나
- 용량의

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

### -InstanceCount
이 cmdlet이 응용 프로그램 게이트웨이에 할당 하는 인스턴스 수를 지정 합니다.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
이 cmdlet이 업데이트 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -서브넷
이 cmdlet이 응용 프로그램 게이트웨이를 배포 하는 서브넷의 배열을 지정 합니다.

응용 프로그램 게이트웨이가 실행 되는 동안에는 서브넷을 업데이트할 수 없습니다.
응용 프로그램 게이트웨이를 중지 하려면 Stop-AzureApplicationGateway cmdlet을 사용 합니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
이 cmdlet이 응용 프로그램 게이트웨이를 배포 하는 가상 네트워크를 지정 합니다.

응용 프로그램 게이트웨이가 실행 되는 동안에는 가상 네트워크를 업데이트할 수 없습니다.
응용 프로그램 게이트웨이를 중지 하려면 **stop-AzureApplicationGateway** 를 사용 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### WindowsAzure의. i a m a 관리 응답

## 상속자

## 관련 링크

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[새 AzureApplicationGateway](./New-AzureApplicationGateway.md)

[-AzureApplicationGateway 제거](./Remove-AzureApplicationGateway.md)

[시작-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
