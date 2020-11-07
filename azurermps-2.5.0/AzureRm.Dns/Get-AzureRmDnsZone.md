---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882254"
---
# Get-AzureRmDnsZone

## SYNOPSIS
DNS 영역을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 기본값 (기본값)
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### 리소스
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## 설명은
**AzureRmDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 가져옵니다.
*Name* 매개 변수를 지정 하면 단일 **DnsZone** 개체가 반환 됩니다.
*Name* 매개 변수를 지정 하지 않으면 지정 된 리소스 그룹의 모든 영역이 포함 된 배열이 반환 됩니다.
**DnsZone** 개체를 사용 하 여 영역을 업데이트할 수 있습니다 (예: **레코드 집합** 개체를 추가할 수 있음).

## 예제의

### 예제 1: 영역 가져오기
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

이 예제에서는 지정 된 리소스 그룹에서 myzone.com 이라는 DNS 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.

### 예제 2: 리소스 그룹의 모든 영역 가져오기
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

이 예제에서는 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.

### 예제 3: 구독에 있는 모든 영역 가져오기
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

이 예제에서는 현재 Azure 구독에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.

## 변수

### -이름
가져올 DNS 영역의 이름을 지정 합니다.

*Name* 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져옵니다.
*ResourceGroupName* 매개 변수를 생략 해도이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가져올 DNS 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.

*ResourceGroupName* 를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다.
이 경우이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 사용자가 파이프를 입력할 수 있도록 허용 하지 않습니다.

## 출력

### DnsZone에 대 한 명령
이 cmdlet은 DNS 영역을 나타내는 개체를 반환 합니다.
영역 이름을 지정 하지 않으면 영역 개체의 배열이 반환 됩니다.

## 상속자

## 관련 링크

[새로운 AzureRmDnsZone](./New-AzureRmDnsZone.md)

[제거-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
