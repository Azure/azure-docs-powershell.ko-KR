---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711337"
---
# Get-AzureRmFirewall

## SYNOPSIS
Azure 방화벽을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmFirewall** cmdlet은 리소스 그룹에 하나 이상의 방화벽을 가져옵니다.

## 예제의

### 1: 리소스 그룹의 모든 방화벽 검색
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

이 예제에서는 "rgName" 리소스 그룹의 모든 방화벽을 검색 합니다.

### 2: 이름으로 방화벽 검색
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

이 예제에서는 "azFw" 이라고 하는 "rgName" 리소스 그룹의 방화벽을 검색 합니다.

### 3: 방화벽을 검색 한 다음 응용 프로그램 규칙 컬렉션을 방화벽에 추가
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

이 예제에서는 방화벽을 검색 한 다음 메서드 AddApplicationRuleCollection를 호출 하 여 방화벽에 응용 프로그램 규칙 컬렉션을 추가 합니다.

### 4: 방화벽을 검색 한 다음 네트워크 규칙 컬렉션을 방화벽에 추가
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

이 예제에서는 방화벽을 검색 한 다음 메서드 AddNetworkRuleCollection를 호출 하 여 네트워크 규칙 컬렉션을 방화벽에 추가 합니다.

### 5: 방화벽을 검색 한 다음 방화벽에서 이름으로 응용 프로그램 규칙 컬렉션 검색
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 가져옵니다. 방화벽 개체의 GetApplicationRuleCollectionByName 메서드를 호출 합니다. 메서드 GetApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.

### 6: 방화벽을 검색 한 다음 방화벽에서 이름별로 네트워크 규칙 컬렉션 검색
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 가져옵니다. 방화벽 개체의 GetNetworkRuleCollectionByName 메서드를 호출 합니다. 메서드 GetNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.

### 7: 방화벽을 검색 한 다음 방화벽에서 이름으로 응용 프로그램 규칙 컬렉션 제거
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 제거 하 고 방화벽 개체의 RemoveApplicationRuleCollectionByName 메서드를 호출 합니다. 메서드 RemoveApplicationRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.

### 8: 방화벽을 검색 한 다음 방화벽에서 이름으로 네트워크 규칙 컬렉션 제거
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

이 예제에서는 방화벽을 검색 한 다음 이름으로 규칙 컬렉션을 제거 하 고 방화벽 개체의 RemoveNetworkRuleCollectionByName 메서드를 호출 합니다. 메서드 RemoveNetworkRuleCollectionByName의 규칙 컬렉션 이름은 대/소문자를 구분 합니다.

### 9: 방화벽을 검색 한 다음 방화벽을 할당 합니다.
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

이 예제에서는 방화벽을 검색 하 고 방화벽에 할당을 호출 하 여 방화벽과 연결 된 구성 (응용 프로그램 및 네트워크 규칙 컬렉션)을 사용 하 여 방화벽 서비스를 시작 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 가져오는 방화벽의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
방화벽이 속해 있는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. * PSAzureFirewall

## 상속자

## 관련 링크

[새로운 AzureRmFirewall](./New-AzureRmFirewall.md)

[제거-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
