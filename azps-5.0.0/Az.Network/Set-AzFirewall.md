---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226338"
---
# Set-AzFirewall

## SYNOPSIS
수정 된 방화벽을 저장 합니다.

## 구문과

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzFirewall** Cmdlet은 Azure 방화벽을 업데이트 합니다.

## 예제의

### 1: 방화벽 응용 프로그램 규칙 모음의 우선 순위 업데이트
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

이 예제에서는 Azure 방화벽의 기존 규칙 컬렉션에 대 한 우선 순위를 업데이트 합니다.
"Rg" 리소스 그룹의 Azure 방화벽 "AzureFirewall"에 "ruleCollectionName" 이라는 응용 프로그램 규칙 컬렉션이 포함 되어 있는 경우 위의 명령은 해당 규칙 모음의 우선 순위를 변경 하 고 나중에 Azure 방화벽을 업데이트 합니다. Set-AzFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.

### 2: Azure 방화벽을 만들고 나중에 응용 프로그램 규칙 컬렉션 설정
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

이 예제에서는 응용 프로그램 규칙 컬렉션 없이 방화벽을 먼저 만듭니다. 나중에 응용 프로그램 규칙과 응용 프로그램 규칙 컬렉션이 만들어지고, 방화벽 개체는 클라우드의 실제 구성에 영향을 주지 않고 메모리에서 수정 됩니다. 클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.

### 3: Azure 방화벽의 위협 업데이트 인텔 작동 모드
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

이 예제에서는 리소스 그룹 "rg"에서 Azure 방화벽 "AzureFirewall"의 위협 Intel 작업 모드를 업데이트 합니다.
Set-AzFirewall 명령이 없으면 로컬 $azFw 개체에서 수행 된 모든 작업이 서버에 반영 되지 않습니다.

### 4: 방화벽을 할당 취소 하 고 할당
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
이 예제에서는 방화벽을 검색 하 고 방화벽을 할당 해제 한 다음 저장 합니다. 할당 취소 명령은 실행 중인 서비스를 제거 하지만 방화벽 구성을 유지 합니다. 클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.
사용자가 서비스를 다시 시작 하려고 하면 방화벽에서 Allocate 메서드를 호출 해야 합니다.
새 VNet 및 공용 IP는 방화벽과 동일한 리소스 그룹에 있어야 합니다. 이번에도 클라우드에 변경 내용을 반영 하려면 Set-AzFirewall를 호출 해야 합니다.

### 5: 관리 공개 IP 주소를 사용 하 여 강제 터널링 시나리오에 할당
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
이 예제에서는 강제 터널링 시나리오를 위해 관리 공용 IP 주소와 서브넷을 사용 하 여 방화벽을 할당 합니다. VNet에는 "AzureFirewallManagementSubnet" 이라는 서브넷이 포함 되어야 합니다.

### 6: 공용 IP 주소를 Azure 방화벽에 추가
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

이 예제에서 공개 IP 주소 "azFwPublicIp1"는 방화벽에 연결 되어 있습니다.

### 7: Azure 방화벽에서 공용 IP 주소 제거
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

이 예제에서는 공개 IP 주소 "azFwPublicIp1"가 방화벽에서 분리 된 것으로 처리 됩니다.

### 8: Azure 방화벽에서 관리 공개 IP 주소 변경
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

이 예제에서는 방화벽의 관리 공용 IP 주소를 "AzFwMgmtPublicIp2"로 변경 합니다.

### 9: Azure 방화벽에 DNS 구성 추가
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

이 예제에서는 DNS 프록시와 DNS 서버 구성이 방화벽에 연결 되어 있습니다.

### 10: 방화벽 응용 프로그램 규칙 모음 내에서 기존 규칙의 대상 업데이트
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

이 예제에서는 Azure 방화벽의 규칙 컬렉션 내에서 기존 규칙의 대상을 업데이트 합니다. 이렇게 하면 IP 주소가 동적으로 변경 될 때 규칙을 자동으로 업데이트할 수 있습니다.

### 11: Azure 방화벽에서 액티브 FTP 허용
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

이 예제에서는 활성 FTP를 방화벽에서 사용할 수 있습니다.

## 변수

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
AzureFirewall

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. * PSAzureFirewall

## 출력

### Microsoft. * PSAzureFirewall

## 상속자

## 관련 링크

[Get-AzFirewall](./Get-AzFirewall.md)

[새로운 AzFirewall](./New-AzFirewall.md)

[제거-AzFirewall](./Remove-AzFirewall.md)
