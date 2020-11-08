---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045665"
---
# Get-AzureApplicationGatewayConfig

## SYNOPSIS
응용 프로그램 게이트웨이 구성 컨텍스트를 가져옵니다.

## 구문과

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Get-Azureapplication의 config** Cmdlet은 Azure Application Gateway 구성 컨텍스트를 가져옵니다.
컨텍스트에는 구성 개체와 XML 구성이 모두 포함 됩니다.
XML 구성을 파일에 저장할 수 있습니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이 구성 가져오기 및 파일에 저장
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이에 대 한 구성을 가져옵니다.
이 명령은 지정 된 경로의 파일에 저장 합니다.

## 변수

### -ExportToFile
이 cmdlet이 구성을 XML 형식으로 저장 하는 파일 경로를 지정 합니다.

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
이 cmdlet이 구성 정보를 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.

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

### System. 문자열

## 출력

### Microsoft. Azure. i m m.

## 상속자

## 관련 링크

[Set-Azureapplication게이트웨이 구성](./Set-AzureApplicationGatewayConfig.md)


