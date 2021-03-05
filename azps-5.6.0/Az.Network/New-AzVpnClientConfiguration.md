---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964123"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
이 명령을 사용하면 사용자가 일부 루트 인증서와 같은 구성해야 할 수 있는 몇 가지 추가 설정 외에도 VPN 게이트웨이에서 미리 구성된 VPN 설정을 기반으로 VPN 프로필 패키지를 만들 수 있습니다.

## 구문

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
이렇게 하면 사용자가 일부 루트 인증서와 같은 구성해야 할 수 있는 추가 설정 외에도 VPN 게이트웨이에서 미리 구성된 VPN 설정을 기반으로 VPN 프로필 패키지를 만들 수 있습니다.

## 예제

### 예제 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

이 cmdlet은 ResourceGroup "ContosoResourceGroup"에서 "ContosoVirtualNetworkGateway"에 대한 VPN 클라이언트 프로필 zip 파일을 만드는 데 사용됩니다. 프로필은 VpnProfileRadiusCert 인증서 파일을 사용하여 "EAPTLS" 인증 방법을 사용하도록 구성된 미리 구성된 반경 서버에 대해 생성됩니다.

## 매개 변수

### -AuthenticationMethod
인증 메서드는 EAPMSCHAPv2 또는 EAPTLS 값을 사용할 수 있습니다. EAPMSCHAPv2를 지정하면 cmdlet은 인증 프로토콜을 사용하는 사용자 이름/암호 인증에 대한 클라이언트 EAP-MSCHAPv2 생성합니다. EAPTLS를 지정한 경우 cmdlet은 EAP-TLS 프로토콜을 사용하는 인증서 인증을 위해 클라이언트 구성 설치 관리자를 생성합니다. "EapTls" 옵션은 신뢰할 수 있는 루트를 업로드하여 Virtual Network Gateway에서 수행한 RADIUS 기반 인증서 인증 및 인증 인증에 모두 사용할 수 있습니다. cmdlet은 구성된 것을 자동으로 감지합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
리소스 이름입니다.

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
Radius 서버 루트 인증서 경로입니다. RADIUS 인증을 사용하는 EAP-TLS를 사용할 때 지정해야 하는 필수 매개 변수입니다. 클라이언트가 인증하는 동안 RADIUS 서버의 유효성을 검사하는 데 사용하는 RADIUS 루트 인증서를 포함하는 .cer 파일의 전체 경로 이름입니다.

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
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### System.String[]

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## 참고 사항

## 관련 링크

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
