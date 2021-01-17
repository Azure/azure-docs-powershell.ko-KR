---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 840a1bef17fd736dbe3144f9fd8d382a78bcfd87
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492177"
---
# New-AzApplicationGatewayBackendHttpSetting

## SYNOPSIS
애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정을 만듭니다.

## 구문

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
New-AzApplicationGatewayBackendHttpSetting cmdlet은 애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정을 만듭니다.
백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용됩니다.

## 예제

### 예제 1: 백 엔드 HTTP 설정 만들기
```powershell
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

이 명령은 쿠키 기반에 대한 기본 설정이 비활성화된 HTTP 프로토콜을 사용하여 포트 80에서 Setting01이라는 백 엔드 HTTP 설정을 만듭니다.
설정은 $Setting 변수에 저장됩니다.

### 예제 2

애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정을 만듭니다. (자동Generated)

<!-- Aladdin Generated Example -->
```powershell
New-AzApplicationGatewayBackendHttpSetting -CookieBasedAffinity Enabled -Name 'Setting01' -PickHostNameFromBackendAddress -Port 80 -Probe <PSApplicationGatewayProbe> -Protocol http -RequestTimeout <Int32>
```

## PARAMETERS

### -AffinityCookieName
Affinity 쿠키에 사용할 쿠키 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationCertificates
애플리케이션 게이트웨이에 대한 인증 인증서를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionDraining
백end http 설정 리소스의 연결 드레인입니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CookieBasedAffinity
백 엔드 서버 풀에 대해 쿠키 기반의 효율성을 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -HostName
백end 서버로 보낼 호스트 헤더를 설정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
이 cmdlet에서 만드는 백 엔드 HTTP 설정의 이름을 지정합니다.

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

### -Path
모든 HTTP 요청에 대한 사전으로 사용되어야 하는 경로입니다.
이 매개 변수에 대한 값이 제공되지 않았다면 경로가 추가되지 않습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendAddress
호스트 헤더를 백end 서버의 호스트 이름에서 선택해야 하는지 플래그를 지정합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
백 엔드 서버 풀의 포트를 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Probe
백 엔드 서버 풀과 연결하기 위해 프로브를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeId
백 엔드 서버 풀과 연결하기 위해 프로브의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
애플리케이션 게이트웨이와 백 엔드 서버 간의 통신에 사용할 프로토콜을 지정합니다.
이 매개 변수에 허용되는 값은 Http 및 Https입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestTimeout
요청 시간 시간 값을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedRootCertificate
Application Gateway 신뢰할 수 있는 루트 인증서

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings

## 참고 사항

## 관련 링크

[Add-AzApplicationGatewayBackendHttpSetting](./Add-AzApplicationGatewayBackendHttpSetting.md)

[Get-AzApplicationGatewayBackendHttpSetting](./Get-AzApplicationGatewayBackendHttpSetting.md)

[Remove-AzApplicationGatewayBackendHttpSetting](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[Set-AzApplicationGatewayBackendHttpSetting](./Set-AzApplicationGatewayBackendHttpSetting.md)

