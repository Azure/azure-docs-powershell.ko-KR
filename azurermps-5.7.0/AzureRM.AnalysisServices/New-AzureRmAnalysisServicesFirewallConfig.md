---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703292"
---
# New-AzureRmAnalysisServicesFirewallConfig

## SYNOPSIS
새 Analysis Services 방화벽 구성을 만듭니다. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## 설명은
New-AzureRmAnalysisServicesFirewallConfig에서 새 방화벽 구성 개체를 만듭니다.

## 예제의

### 예제 1
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

Power bi 서비스를 사용 하지 않고 방화벽 규칙 구성을 만듭니다.

## 변수

### -EnablePowerBIService
PowerBI 서비스 사용 여부를 나타내는 플래그

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRules
방화벽 규칙 목록

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

## 출력

### AnalysisServices. AzureAnalysisServicesFirewallConfig/.

## 관련 링크

[새로운 AzureRmAnalysisServicesFirewallConfig](./New-AzureRmAnalysisServicesFirewallConfig.md)
