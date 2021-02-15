---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189521"
---
# Set-AzFirewall

## SYNOPSIS
수정된 방화벽을 저장합니다.

## 구문

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzFirewall** cmdlet은 Azure Firewall을 업데이트합니다.

## 예제

### 1: 방화벽 애플리케이션 규칙 컬렉션의 업데이트 우선 순위
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

이 예제에서는 Azure Firewall의 기존 규칙 컬렉션의 우선 순위를 업데이트합니다.
리소스 그룹 "rg"의 Azure Firewall "AzureFirewall"에 "ruleCollectionName"이라는 애플리케이션 규칙 컬렉션이 포함되어 있는 경우 위의 명령은 해당 규칙 컬렉션의 우선 순위를 변경하고 이후에 Azure Firewall을 업데이트합니다. Set-AzFirewall 경우 로컬 $azFw 개체에서 수행된 모든 작업은 서버에 반영되지 않습니다.

### 2: Azure Firewall 만들기 및 나중에 애플리케이션 규칙 컬렉션 설정
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

이 예제에서는 애플리케이션 규칙 컬렉션 없이 방화벽이 먼저 만들어집니다. 그런 다음 애플리케이션 규칙 및 애플리케이션 규칙 컬렉션이 생성되면 클라우드의 실제 구성에 영향을 주지 않고 메모리에서 방화벽 개체가 수정됩니다. 변경 내용을 클라우드에 반영하려면 Set-AzFirewall 호출해야 합니다.

### 3: Azure Firewall의 위협 Intel 작업 모드 업데이트
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

이 예제에서는 리소스 그룹 "rg"에서 Azure Firewall "AzureFirewall"의 Threat Intel 작업 모드를 업데이트합니다.
Set-AzFirewall 경우 로컬 $azFw 개체에서 수행된 모든 작업은 서버에 반영되지 않습니다.

### 4: 방화벽 할당을 할당해제 및 할당
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
이 예제에서는 방화벽을 검색하고, 방화벽의 재배치 및 저장합니다. Deallocate 명령은 실행 중인 서비스를 제거하지만 방화벽의 구성은 보존합니다. 변경 내용을 클라우드에 반영하려면 Set-AzFirewall 호출해야 합니다.
사용자가 서비스를 다시 시작하려는 경우 방화벽에서 Allocate 메서드를 호출해야 합니다.
새 VNet 및 공용 IP는 방화벽과 동일한 리소스 그룹에 있어야 합니다. 다시, 클라우드에 변경 내용을 반영하려면 Set-AzFirewall 합니다.

### 5: 강제 터널링 시나리오에 대한 관리 공용 IP 주소로 할당
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
이 예제에서는 강제 터널링 시나리오에 대한 관리 공용 IP 주소 및 서브넷을 통해 방화벽을 할당합니다. VNet은 "AzureFirewallManagementSubnet"이라는 서브넷을 포함해야 합니다.

### 6: Azure Firewall에 공용 IP 주소 추가
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

이 예제에서는 방화벽에 연결된 공용 IP 주소 "azFwPublicIp1"입니다.

### 7: Azure Firewall에서 공용 IP 주소 제거
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

이 예제에서는 방화벽에서 "azFwPublicIp1" 공용 IP 주소가 연결됩니다.

### 8: Azure Firewall에서 관리 공용 IP 주소 변경
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

이 예제에서는 방화벽의 관리 공용 IP 주소가 "AzFwMgmtPublicIp2"로 변경됩니다.

### 9: Azure Firewall에 DNS 구성 추가
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

이 예제에서는 DNS 프록시 및 DNS 서버 구성이 방화벽에 연결됩니다.

### 10: 방화벽 애플리케이션 규칙 컬렉션 내에서 기존 규칙의 대상 업데이트
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

이 예제에서는 Azure Firewall의 규칙 컬렉션 내에서 기존 규칙의 대상을 업데이트합니다. 이렇게 하면 IP 주소가 동적으로 변경될 때 규칙을 자동으로 업데이트할 수 있습니다.

### 11: Azure Firewall에서 활성 FTP 허용
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

이 예제에서는 방화벽에서 활성 FTP가 허용됩니다.

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

### -AzureFirewall
The AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## 출력

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## 참고 사항

## 관련 링크

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
