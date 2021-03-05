---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 2dd00c21a0badaca90419615df179299dc2d4240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003424"
---
# Set-AzLoadBalancerProbeConfig

## SYNOPSIS
부하 저울에 대한 프로브 구성을 업데이트합니다.

## 구문

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzLoadBalancerProbeConfig** cmdlet은 부하 분산기에 대한 프로브 구성을 업데이트합니다.

## 예제

### 예제 1: 부하 저울에서 프로브 구성 수정
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

첫 번째 명령은 MyLoadBalancer라는 loadbalancer를 구한 다음, $slb 변수에 저장합니다.
두 번째 명령은 파이프라인 연산자를 사용하여 부하 분산 $slb Add-AzLoadBalancerProbeConfig에 전달하여 새 프로브 구성을 추가합니다.
세 번째 명령은 부하 분산을 **Set-AzLoadBalancerProbeConfig로 전달하여** 새 구성을 설정합니다.
현재 cmdlet에서 요구하기 때문에 이전 명령에 지정된 동일한 매개 변수 중 몇 가지를 지정해야 합니다.

## 매개 변수

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

### -IntervalInSeconds
부하 균형 서비스의 각 인스턴스에 대한 프로브 사이의 간격을 초로 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancer
부하 균형 조정기를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 부하 저울에 대한 프로브 구성을 업데이트합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
이 cmdlet에서 설정하는 프로브 구성의 이름을 지정합니다.

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

### -Port
부하가 조정된 서비스에 연결해야 하는 프로브의 포트를 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProbeCount
인스턴스에 대해 인스턴스당 연속 오류 수를 지정하여 부적당으로 간주합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protocol
프로비전에 사용할 프로토콜을 지정합니다.
이 매개 변수에 대해 허용되는 값은 Tcp 또는 Http입니다.

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

### -RequestPath
상태 확인을 위해 프로브할 부하 균형 서비스의 경로를 지정합니다.

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

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

### System.String

### System.Int32

## 출력

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## 참고 사항

## 관련 링크

[Add-AzLoadBalancerProbeConfig](./Add-AzLoadBalancerProbeConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Get-AzLoadBalancerProbeConfig](./Get-AzLoadBalancerProbeConfig.md)

[New-AzLoadBalancerProbeConfig](./New-AzLoadBalancerProbeConfig.md)

[Remove-AzLoadBalancerProbeConfig](./Remove-AzLoadBalancerProbeConfig.md)


