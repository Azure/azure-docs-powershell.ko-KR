---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875951"
---
# Set-AzDnsZone

## SYNOPSIS
DNS 영역의 속성을 업데이트 합니다.

## 구문과

### 필드인
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 오브젝트가
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzDnsZone** Cmdlet은 Azure DNS 서비스에서 지정 된 DNS 영역을 업데이트 합니다.
이 cmdlet은 영역의 레코드 집합을 업데이트 하지 않습니다.

**DnsZone** 개체를 매개 변수 또는 파이프라인 연산자를 사용 하 여 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.

*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.

영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다. 이는 동시 변경에 대 한 보호를 제공 합니다. *덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.

## 예제의

### 예제 1: DNS 영역 업데이트
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

첫 번째 명령은 지정 된 리소스 그룹에서 myzone.com 이라는 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.

두 번째 명령은 $Zone에 대 한 태그를 업데이트 합니다.

마지막 명령은 변경 내용을 커밋합니다.

### 예제 2: 영역의 태그 업데이트
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

이 명령은 먼저 영역을 명시적으로 가져오지 않고 myzone.com 이라는 영역에 대 한 태그를 업데이트 합니다.

## 변수

### -이름
업데이트할 DNS 영역의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다. 이는 동시 변경에 대 한 보호를 제공 합니다. *덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
업데이트할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.
ZoneName 매개 변수도 지정 해야 합니다.

또는 *zone* 매개 변수 또는 파이프라인을 통해 DnsZone 개체를 사용 하 여 영역을 지정할 수도 있습니다.

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
업데이트할 DNS 영역을 지정 합니다.

또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
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

### DnsZone에 대 한 명령
DnsZone 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.

## 출력

### DnsZone에 대 한 명령
이 cmdlet은 새 Etag를 사용 하 여 업데이트 된 DNS 영역을 나타내는 DnsZone 개체를 반환 합니다.

## 상속자
*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.

*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.
*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.

## 관련 링크

[Get-AzDnsZone](./Get-AzDnsZone.md)

[새로운 AzDnsZone](./New-AzDnsZone.md)

[제거-AzDnsZone](./Remove-AzDnsZone.md)