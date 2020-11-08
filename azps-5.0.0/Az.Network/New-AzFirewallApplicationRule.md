---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218327"
---
# New-AzFirewallApplicationRule

## SYNOPSIS
방화벽 응용 프로그램 규칙을 만듭니다.

## 구문과

### TargetFqdn (기본값)
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FqdnTag
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzFirewallApplicationRule** Cmdlet은 Azure 방화벽에 대 한 응용 프로그램 규칙을 만듭니다.

## 예제의

### 예제 1:10.0.0.0의 모든 HTTPS 트래픽을 허용 하는 규칙 만들기
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

이 예제는 10.0.0.0에서 포트 443의 모든 HTTPS 트래픽을 허용 하는 규칙을 만듭니다.

### 예제 2:10.0.0.0/24 서브넷에 대 한 Windows을 허용 하는 규칙 만들기
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

이 예제에서는 10.0.0.0/24 도메인에 대 한 Windows 업데이트에 대 한 트래픽을 허용 하는 규칙을 만듭니다.

## 변수

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

### -설명
이 규칙에 대 한 설명을 선택적으로 지정 합니다.

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

### -FqdnTag
이 규칙에 대 한 FQDN 태그 목록을 지정 합니다. [AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet을 사용 하 여 사용 가능한 태그를 검색할 수 있습니다.

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 응용 프로그램 규칙의 이름을 지정 합니다. 이름은 규칙 컬렉션 내에서 고유 해야 합니다.

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

### -프로토콜
이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다. 형식은 <protocol type> 다음과 같습니다. <port> 예를 들어 "http: 80" 또는 "https: 443"입니다.
프로토콜은 TargetFqdn을 사용 하지만 FqdnTag와 함께 사용할 수 없는 경우 필수입니다. 지원 되는 프로토콜은 HTTP 및 HTTPS입니다.

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
규칙의 원본 주소

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceIpGroup
규칙의 원본 ipgroup

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFqdn
이 규칙에 따라 필터링 된 도메인 이름 목록을 지정 합니다.
별표 문자 ' '는 *목록에 있는 FQDN의 첫 문자로만 허용 됩니다. 별표를 사용 하는 경우 임의 개수의 문자와 일치 합니다. (예: '* msn.com '는 msn.com와 모든 하위 도메인)

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### PSAzureFirewallApplicationRule에 대 한.

## 상속자

## 관련 링크

[새로운 AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[새로운 AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)

[Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md)
