---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883094"
---
# Remove-AzureRmDnsZone

## SYNOPSIS
리소스 그룹에서 DNS 영역을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 필드인
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 오브젝트가
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureRmDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 영구적으로 삭제 합니다.
영역에 포함 된 모든 레코드 집합도 삭제 됩니다.

*Name* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **DnsZone** 개체를 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.

확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.

**DnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우에는 로컬 **DnsZone** 개체가 검색 된 이후 해당 영역이 Azure DNS에서 변경 되지 않습니다 (DNS 영역 리소스에서 직접 작업을 변경 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행 하지 않음).
이는 동시 영역 변경에 대 한 보호를 제공 합니다.
이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.

## 예제의

### 예제 1: 영역 제거
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

이 명령은 MyResourceGroup 이라는 리소스 그룹에서 myzone.com 이라는 영역을 제거 합니다.

## 변수

### -Force
이 매개 변수는이 cmdlet에 대해 더 이상 사용 되지 않습니다.
이후 릴리스에서 제거 될 것입니다.

이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어 하려면 *Confirm* 매개 변수를 사용 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 제거 하는 DNS 영역의 이름을 지정 합니다.
또한 *ResourceGroupName* 매개 변수를 지정 해야 합니다.

또는 *zone* 매개 변수를 사용 하 여 DNS 영역을 지정할 수도 있습니다.

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
**DnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우에는 로컬 **DnsZone** 개체가 검색 된 이후 해당 영역이 Azure DNS에서 변경 되지 않습니다 (DNS 영역 리소스에서 직접 작업을 변경 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행 하지 않음).
이는 동시 영역 변경에 대 한 보호를 제공 합니다.

이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.

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

### -PassThru
passthru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
제거할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.
*ZoneName* 매개 변수도 지정 해야 합니다.

또는 파이프라인 또는 *zone* 매개 변수를 통해 전달 되는 **DnsZone** 개체를 사용 하 여 DNS 영역을 지정할 수도 있습니다.

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

### -Zone
삭제할 DNS 영역을 지정 합니다.
**DnsZone** 개체는 파이프라인을 통해 전달할 수도 있습니다.

또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 삭제할 DNS 영역을 지정할 수도 있습니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### DnsZone에 대 한 명령
**DnsZone** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.

## 출력

### 않아야
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자
DNS 영역 삭제 시 발생할 가능성이 높은 영향으로 인해,이 cmdlet은 $ConfirmPreference Windows PowerShell 변수에 없음이 아닌 값이 있는 경우 확인을 묻는 메시지를 표시 합니다.

*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.
*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다. 

## 관련 링크

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[새로운 AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
