---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 388275b4b182c9f9f054ba4965deebfb2c08556a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869822"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
이 명령을 사용 하 여 사용자는 VPN 게이트웨이에서 미리 구성 된 vpn 설정을 기반으로 Vpn 프로필 패키지를 만들 수 있으며, 예를 들어 일부 루트 인증서와 같이 사용자가 구성 해야 하는 일부 추가 설정이 있습니다.

## 구문과

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
이렇게 하면 사용자가 VPN 게이트웨이에서 미리 구성 된 vpn 설정을 기반으로 Vpn 프로필 패키지를 만들 수 있으며, 예를 들어 일부 루트 인증서와 같이 사용자가 구성 해야 하는 일부 추가 설정이 있습니다.

## 예제의

### 예제 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

이 cmdlet은 ResourceGroup "ContosoResourceGroup"의 "ContosoVirtualNetworkGateway"에 대 한 VPN 클라이언트 프로필 zip 파일을 만드는 데 사용 됩니다. VpnProfileRadiusCert 인증서 파일과 함께 "EAPTLS" 인증 방법을 사용 하도록 구성 된 미리 구성 된 radius 서버에 대해 프로필이 생성 됩니다.

## 변수

### -AuthenticationMethod
인증 방법에서는 값 EAPMSCHAPv2 또는 EAPTLS를 사용할 수 있습니다. EAPMSCHAPv2가 지정 되 면 cmdlet은 EAP-MSCHAPv2 인증 프로토콜을 사용 하는 사용자 이름/암호 인증에 대 한 클라이언트 구성 설치 관리자를 생성 합니다. EAPTLS가 지정 된 경우 cmdlet은 EAP-TLS 프로토콜을 사용 하는 인증서 인증을 위한 클라이언트 구성 설치 관리자를 생성 합니다. "EapTls" 옵션은 신뢰할 수 있는 루트를 업로드 하 여 가상 네트워크 게이트웨이에서 수행 하는 RADIUS 기반 인증서 인증과 인증 인증 모두에 사용할 수 있습니다. Cmdlet은 구성 된 항목을 자동으로 검색 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
클라이언트 루트 인증서 경로 목록

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -이름
자원 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Radius 서버 루트 인증서 경로입니다. 이 매개 변수는 RADIUS 인증을 사용한 EAP-TLS를 사용 하는 경우에 지정 해야 합니다. 클라이언트가 인증 하는 동안 RADIUS 서버의 유효성을 검사 하는 데 사용 하는 RADIUS 루트 인증서를 포함 하는 .cer 파일의 전체 경로 이름입니다.

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

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System.webserver []

## 출력

### PSVpnProfile에 대 한.

## 상속자

## 관련 링크

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
