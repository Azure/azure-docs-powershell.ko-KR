---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: c45a829414fd1009f97c99844705e9affab0ef30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526163"
---
# Set-AzureRmApplicationGatewaySslCertificate

## SYNOPSIS
SSL 인증서의 목표 상태를 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmApplicationGatewaySslCertificate** CMDLET은 SSL 인증서의 목표 상태를 설정 합니다.

## 예제의

### 예제 1: SSL 인증서의 목표 상태 설정
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이에서 SSL 인증서에 대 한 목표 상태를 설정 합니다.

## 변수

### -ApplicationGateway
SSL (Secure Socket Layer) 인증서가 연결 되는 응용 프로그램 게이트웨이를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertificateFile
SSL 인증서의 경로를 지정 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
SSL 인증서의 이름을 지정 합니다.

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

### -암호
SSL 인증서의 암호를 지정 합니다.

```yaml
Type: System.Security.SecureString
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

### Microsoft. * PSApplicationGateway
매개 변수: ApplicationGateway (ByValue)

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[추가-AzureRmApplicationGatewaySslCertificate](./Add-AzureRmApplicationGatewaySslCertificate.md)

[Get-AzureRmApplicationGatewaySslCertificate](./Get-AzureRmApplicationGatewaySslCertificate.md)

[새로운 AzureRmApplicationGatewaySslCertificate](./New-AzureRmApplicationGatewaySslCertificate.md)

[제거-AzureRmApplicationGatewaySslCertificate](./Remove-AzureRmApplicationGatewaySslCertificate.md)


