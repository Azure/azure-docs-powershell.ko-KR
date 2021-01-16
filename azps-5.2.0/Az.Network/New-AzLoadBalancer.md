---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354326"
---
# New-AzLoadBalancer

## SYNOPSIS
부하 균형 조정을 만듭니다.

## 구문

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzLoadBalancer** cmdlet은 Azure Load Balancer를 만듭니다.

## 예제

### 예제 1: 부하 균형 조정기 만들기
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

부하 균형 조정을 배포하려면 먼저 여러 개체를 만들어야 합니다. 처음 7개의 명령은 해당 개체를 만드는 방법을 보여 주며,
8번 명령은 MyResourceGroup이라는 리소스 그룹에 MyLoadBalancer라는 부하 분산을 만듭니다.
9번째 명령과 마지막 명령은 새 부하가 성공적으로 만들어지기 위해 새 부하 균형을 맞출 수 있도록 합니다.
이 예제에서는 부하 균형 조정을 만드는 방법만 보여줍니다. 또한 다른 가상 머신에 Add-AzNetworkInterfaceIpConfig cmdlet을 사용하여 구성해야 합니다.

### 예제 2: 전역 부하 균형 조정기 만들기
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

전역 부하 균형 조정을 배포하려면 먼저 여러 개체를 만들어야 합니다. 처음 5개의 명령은 해당 개체를 만드는 방법을 보여 주며,
여섯 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyLoadBalancer라는 부하 분산을 만듭니다.
일곱 번째 명령과 마지막 명령은 새 부하가 성공적으로 생성되도록 합니다.
이 예제에서는 전역 부하 균형 조정을 만드는 방법만 보여줍니다. 또한 백 엔드 주소 풀에 지역 부하 New-AzLoadBalancerBackendAddressConfig ipconfig ID를 할당하려면 New-AzLoadBalancerBackendAddressConfig cmdlet을 사용하여 구성해야 합니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet 실행

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

### -BackendAddressPool
부하 균형 조정과 연결하기 위해 백end 주소 풀을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Force
이 cmdlet이 동일한 이름의 부하 균형 조정이 이미 있는 경우에도 부하 균형 조정을 만듭니다.

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

### -FrontendIpConfiguration
부하 균형 조정과 연결하기 위해 프런트 엔드 IP 주소 목록을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InboundNatPool
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InboundNatRule
부하 균형 조정과 연결하기 위해 인바운드 NAT(네트워크 주소 변환) 규칙 목록을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancingRule
부하 분산과 연결하기 위해 부하 분산 규칙 목록을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
부하 균형 조정기를 만들 지역을 지정합니다.

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

### -Name
이렇게 만드는 부하 균형 조정의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutboundRule
아웃바운드 규칙.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Probe
부하 균형 조정과 연결하기 위해 프로브 목록을 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
부하 균형 조정기를 만들 리소스 그룹의 이름을 지정합니다.

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

### -Sku
부하 균형 조정기 SKU 이름입니다.

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

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
부하 균형 조정기 SKU 계층입니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]

### Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]

### Microsoft.Azure.Commands.Network.Models.PSProbe[]

### Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]

### Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]

### Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]

## 출력

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## 참고 사항

## 관련 링크

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Remove-AzLoadBalancer](./Remove-AzLoadBalancer.md)

[Set-AzLoadBalancer](./Set-AzLoadBalancer.md)
