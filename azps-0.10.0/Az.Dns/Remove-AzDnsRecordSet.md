---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: 10cd4936ad406be85f840b25c175d7900d66d679
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876765"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
레코드 집합을 삭제 합니다.

## 구문과

### 필드인
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 섞여
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 오브젝트가
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 레코드 집합을 삭제 합니다.
영역 apex에서 자동으로 만들어지는 SOA 또는 NS (이름 서버) 레코드는 삭제할 수 없습니다.

파이프라인 연산자 또는 매개 변수를 사용 하 여이 cmdlet에 **RecordSet** 개체를 전달할 수 있습니다.
**레코드 집합 개체를** 사용 하지 않고 이름 및 형식을 기준으로 하 여 변수를 확인 하려면 파이프라인 연산자 또는 매개 변수를 사용 하 여이 Cmdlet에 **DnsZone** 개체로 영역을 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정 해야 합니다.

확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.

**RecordSet** 개체를 사용 하 여 레코드 집합을 지정 하는 경우 로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 되 면 삭제 되지 않습니다.
이는 동시 변경에 대 한 보호를 제공 합니다.
동시 변경 내용에 관계 없이 레코드 집합을 삭제 하는 *Overwrite* 매개 변수를 사용 하 여이를 억제할 수 있습니다.

## 예제의

### 예제 1: 레코드 집합 제거
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

첫 번째 명령은 지정 된 레코드 집합을 가져온 다음 $RecordSet 변수에 저장 합니다. 두 번째 명령은 $RecordSet에 설정 된 레코드를 제거 합니다.

### 예제 2: 레코드 집합 제거 및 모든 확인 표시 안 함
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

첫 번째 명령은 지정 된 레코드 집합을 가져옵니다.

두 번째 명령은 레코드 집합을 삭제 했지만 그 동안에는 레코드가 변경 되지 않았습니다.
확인 메시지가 표시 되지 않습니다.

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
제거할 **레코드 집합** 의 이름을 지정 합니다.
이름으로 레코드 집합을 지정 하는 경우 *영역* 매개 변수 또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 DNS 영역을 지정 해야 합니다.

또는 레코드 집합 *은 레코드 집합 매개 변수* 를 사용 하 여 전달 되는 **레코드** 집합 개체를 사용 하 여 지정할 수 있습니다.

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
**RecordSet** 개체를 사용 하 여 레코드 집합을 지정 하는 경우 로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 되 면 삭제 되지 않습니다.
이는 동시 변경에 대 한 보호를 제공 합니다.
이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 레코드 집합을 삭제 합니다.

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

### -레코드 집합
제거할 **레코드 집합** 개체를 지정 합니다.

또는 *이름* , *영역* 매개 변수를 사용 하거나 *name* , *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 레코드 집합을 지정할 수 있습니다.

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
DNS 레코드의 유형을 지정 합니다.

유효한 값은 다음과 같습니다.

- 에서
- AAAA
- CNAME
- 멕시코
- NS
- PTR 레코드로
- SRV
- 라는

SOA 레코드는 영역이 삭제 될 때 자동으로 삭제 됩니다.
SOA 레코드는 수동으로 삭제할 수 없습니다.

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
삭제할 **레코드 집합** 을 포함 하는 DNS 영역이 포함 된 리소스 그룹을 지정 합니다.
이 매개 변수는 record set 및 DNS 영역이 *Name* 및 *ZoneName* 매개 변수를 사용 하 여 지정 된 경우에만 적용 됩니다.

또는 *RecordSet* 매개 변수 또는 *Name* 및 *Zone* 매개 변수를 사용 하 여 레코드 집합을 지정할 수도 있습니다.

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
삭제할 **레코드 집합** 을 포함 하는 DNS 영역을 지정 합니다.
이 매개 변수는 *Name* 매개 변수를 사용 하 여 레코드 집합을 지정 하는 경우에만 적용 됩니다.

또는 *RecordSet* 매개 변수 또는 *Name* , *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 레코드 집합을 지정할 수도 있습니다.

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
삭제할 **레코드 집합** 을 포함 하는 영역의 이름을 지정 합니다.
또한 *Name* 및 *ResourceGroupName* 매개 변수를 지정 해야 합니다.

또는 레코드 집합은 *레코드* 집합 매개 변수 또는 *Name* 및 *Zone* 매개 변수를 사용 하 여 지정할 수 있습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft Azure. DnsRecordSet
**RecordSet** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.

## 출력

### 않아야
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자
*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.

*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.
*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.

## 관련 링크

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[새로운 AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
