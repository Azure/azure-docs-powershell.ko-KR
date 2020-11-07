---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876772"
---
# Get-AzDnsZone

## SYNOPSIS
DNS 영역을 가져옵니다.

## 구문과

### 기본값 (기본값)
```
Get-AzDnsZone [<CommonParameters>]
```

### 리소스
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## 설명은
**AzDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 가져옵니다.
*Name* 매개 변수를 지정 하면 단일 **DnsZone** 개체가 반환 됩니다.
*Name* 매개 변수를 지정 하지 않으면 지정 된 리소스 그룹의 모든 영역이 포함 된 배열이 반환 됩니다.
**DnsZone** 개체를 사용 하 여 영역을 업데이트할 수 있습니다 (예: **레코드 집합** 개체를 추가할 수 있음).

## 예제의

### 예제 1: 영역 가져오기
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

이 예제에서는 지정 된 리소스 그룹에서 myzone.com 이라는 DNS 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.

### 예제 2: 리소스 그룹의 모든 영역 가져오기
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

이 예제에서는 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.

### 예제 3: 구독에 있는 모든 영역 가져오기
```
PS C:\> $Zones = Get-AzDnsZone
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 사용자가 파이프를 입력할 수 있도록 허용 하지 않습니다.

## 출력

### DnsZone에 대 한 명령
이 cmdlet은 DNS 영역을 나타내는 개체를 반환 합니다.
영역 이름을 지정 하지 않으면 영역 개체의 배열이 반환 됩니다.

## 상속자

## 관련 링크

[새로운 AzDnsZone](./New-AzDnsZone.md)

[제거-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
