---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046429"
---
# Set-AzureApplicationGatewayConfig

## SYNOPSIS
응용 프로그램 게이트웨이를 구성 합니다.

## 구문과

### Read-configfile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Set-Azureapplication의 config** cmdlet은 응용 프로그램 게이트웨이를 구성 합니다.

## 예제의

### 예제 1: 구성 개체를 사용 하 여 응용 프로그램 게이트웨이 구성
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

첫 번째 명령은 **Get AzureapplicationApplicationGateway02 config** cmdlet을 사용 하 여 라는 응용 프로그램 게이트웨이에 대 한 구성 개체를 가져옵니다.
명령이 $ConfigReturnObject 변수에 저장 합니다.

두 번째 명령은 $ConfigReturnObject 변수에 저장 된 응용 프로그램 게이트웨이 구성 개체를 사용 하 여 ApplicationGateway06 라는 응용 프로그램에 대 한 구성을 설정 합니다.

### 예제 2: 구성 파일을 사용 하 여 응용 프로그램 게이트웨이 구성
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

이 명령은 지정 된 위치에서 응용 프로그램 게이트웨이 구성 파일을 사용 하 여 ApplicationGateway06 이라는 응용 프로그램에 대 한 구성을 설정 합니다.

### 예제 3: 구성 개체를 사용 하 여 구성 수정
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

첫 번째 명령은 **Get AzureapplicationApplicationGateway06 config** cmdlet을 사용 하 여 라는 응용 프로그램 게이트웨이에 대 한 구성 개체를 가져옵니다.
명령이 $ConfigReturnObject 변수에 저장 합니다.

두 번째 명령은 $ConfigReturnObject에 저장 된 개체의 **port** 속성에 포트 값을 할당 합니다.

마지막 명령은 현재 cmdlet에 업데이트 된 $ConfigReturnObject을 전달 합니다.

## 변수

### -구성
응용 프로그램 게이트웨이 구성 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 구성을 응용 프로그램 게이트웨이에 할당 합니다.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Read-configfile
응용 프로그램 게이트웨이의 구성 파일 경로를 XML 형식으로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 구성을 응용 프로그램 게이트웨이에 할당 합니다.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
이 cmdlet이 구성 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System.webserver, Microsoft Azure. Application게이트웨이 Objectmodel. i m a 구성

## 출력

### WindowsAzure의. i a m a 관리 응답

## 상속자

## 관련 링크

[Get-Azureapplication게이트웨이 구성](./Get-AzureApplicationGatewayConfig.md)


