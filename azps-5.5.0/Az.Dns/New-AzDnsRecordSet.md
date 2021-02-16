---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209616"
---
# New-AzDnsRecordSet

## SYNOPSIS
DNS 레코드 집합을 만듭니다.

## 구문

### 필드(기본값)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzDnsRecordSet** cmdlet은 지정된 이름 및 지정된 영역의 형식을 사용하여 새 DNS(도메인 이름 시스템) 레코드 집합을 만듭니다.
**RecordSet** 개체는 이름과 형식이 같은 DNS 레코드 집합입니다.
이름은 영역과 상대적인 것이고, 정식 이름이 아닌 것을 참고합니다.
*DnsRecords 매개* 변수는 레코드 집합의 레코드를 지정합니다.
이 매개 변수는 New-AzDnsRecordConfig를 사용하여 생성된 DNS 레코드의 배열을 사용합니다.
파이프라인 연산자를 사용하여 **DnsZone** 개체를 이 cmdlet에 전달하거나 **DnsZone** 개체를 영역  매개 변수로 전달하거나 이름으로 영역 지정을 지정할 수 있습니다.
*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
일치하는 **RecordSet이** 이미 있는 경우(동일한 이름 및 레코드 형식) *덮어써서* 매개 변수를 지정해야 합니다. 그렇지 않으면 cmdlet에서 새 **RecordSet을 만들지 않습니다.**

## 예제

### 예제 1: A 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.
단일 DNS 레코드를 포함 합니다.

### 예제 2: AAAA 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 AAAA 형식의 TTL(1시간)(3600초)입니다.
단일 DNS 레코드를 포함 합니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 3: CNAME 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 예제에서는 영역 이름에 www라는 **RecordSet을** myzone.com.
레코드 집합은 CNAME 형식이고 TTL은 1시간(3600초)입니다.
단일 DNS 레코드를 포함 합니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 4: MX 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 MX 형식이고 TTL은 1시간(3600초)입니다.
단일 DNS 레코드를 포함 합니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.

### 예제 5: NS 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역 집합에 ns1이라는 **RecordSet을** myzone.com.
레코드 집합은 NS 형식으로, TTL은 1시간(3600초)입니다.
단일 DNS 레코드를 포함 합니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 6: PTR 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

이 명령은 **4라는 RecordSet을** 3.2.1.in-addr.arpa입니다.
레코드 집합은 PTR 형식으로, TTL은 1시간(3600초)입니다.
단일 DNS 레코드를 포함 합니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 7: SRV 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 _sip._tcp라는 **RecordSet을** myzone.com.
레코드 집합은 SRV 형식으로, TTL은 1시간(3600초)입니다.
IP 주소 2001.2.3.4를 포인터로 하는 단일 DNS 레코드가 포함되어 있습니다.
서비스(sip) 및 프로토콜(tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정됩니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 8: TXT 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역 이름의 **RecordSet** 텍스트를 myzone.com.
레코드 집합은 TXT 형식으로, TTL은 1시간(3600초)입니다.
단일 DNS 레코드를 포함 합니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 9: 영역 apex에서 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역의 루트 또는 루트에 **RecordSet을** myzone.com.
이를 위해 레코드 집합 이름은 "@"(따옴표 포함)로 지정됩니다.
영역의 apex에는 CNAME 레코드를 만들 수 없습니다.
DNS 표준의 제약 조건입니다. Azure DNS의 제한 사항이 아닌 경우
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 10: 와일드카드 레코드 집합 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역 집합에 *라는 **RecordSet을** myzone.com.
와일드카드 레코드 집합입니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 11: 빈 레코드 집합 만들기
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

이 명령은 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.
빈 레코드 집합으로, 나중에 레코드를 추가할 수 있는 자리 홀더 역할을 합니다.

### 예제 12: 레코드 집합 만들기 및 모든 확인 표시 안
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

이 명령은 **RecordSet을 만듭니다.**
*덮어덮어* 사용 매개 변수를 사용하면 이 레코드 집합이 이름과 형식이 같은 기존 레코드 집합을 덮어 덮어습니다(해당 레코드 집합의 기존 레코드가 손실).
값과 함께 *Confirm* $False 확인 프롬프트를 표시하지 않습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -DnsRecords
레코드 집합에 포함할 DNS 레코드의 배열을 지정합니다.
New-AzDnsRecordConfig cmdlet을 사용하여 DNS 레코드 개체를 만들 수 있습니다.
자세한 내용은 예제를 참조하세요.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadata
RecordSet과 연결되는 메타데이터 배열을 지정합니다.
메타데이터는 해시 테이블로 표현되는 이름-값 쌍(예: @{"dept"="shopping";")을 사용하여 지정됩니다. env"="production"}.

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

### -Name
만들 **RecordSet의 이름을** 지정합니다.

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

### -Overwrite
이 cmdlet이 이미 있는 경우 지정된 **RecordSet을** 덮어써야 것을 나타냅니다.

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

### -RecordType
만들 DNS 레코드의 유형을 지정합니다.
유효한 값은
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- 영역이 만들어지면 TXT SOA 레코드가 자동으로 만들어지며 수동으로 만들 수 없습니다.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
DNS 영역이 포함된 리소스 그룹을 지정합니다.
영역 이름을 지정하려면 *ZoneName* 매개 변수도 지정해야 합니다.
또는 영역 매개 변수를 사용하여 DNS 영역 개체를 전달하여 영역 및 리소스 그룹을 지정할 *수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
별칭 대상 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
DNS RecordSet에 대한 TTL(Time to Live)을 지정합니다.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
RecordSet을 만들 DnsZone을 **지정합니다.**
또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지역을 지정할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
RecordSet을 만들 영역의 이름을 **지정합니다.**
*ResourceGroupName* 매개 변수를 사용하여 영역이 포함된 리소스 그룹도 지정해야 합니다.
또는 영역 매개 변수를 사용하여 DNS 영역 개체를 전달하여 영역 및 리소스 그룹을 지정할 *수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## 출력

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## 참고 사항
*Confirm* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.
*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.
*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.

## 관련 링크

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
