---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b0e8642feb208c9ed7ab0a91a31ebe7bd0f7cf8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882250"
---
# Remove-AzureRmDnsRecordConfig

## SYNOPSIS
로컬 레코드 집합 개체에서 DNS 레코드를 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 에서
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### AAAA
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### NS
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### 멕시코
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### PTR 레코드로
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### 라는
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### SRV
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### CNAME
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## 설명은
**AzureRmDnsRecordConfig** cmdlet은 레코드 집합에서 DNS (Domain Name System) 레코드를 제거 합니다.
**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzureRmDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.

레코드를 제거 하려면 해당 레코드 종류에 대 한 모든 필드가 정확히 일치 해야 합니다.
SOA 레코드를 추가 하거나 제거할 수 없습니다.
SOA 레코드는 dns 영역이 생성 될 때 자동으로 만들어지고 DNS 영역이 삭제 되 면 자동으로 삭제 됩니다.

이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.

## 예제의

### 예제 1: 레코드 집합에서 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 A 레코드를 제거 합니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

### 예제 2: 레코드 집합에서 AAAA 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 AAAA 레코드를 제거 합니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

### 예제 3: 레코드 집합에서 CNAME 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 CNAME 레코드를 제거 합니다.
CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로 결과는 빈 레코드 집합입니다.

### 예제 4: 레코드 집합에서 MX 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 MX 레코드를 제거 합니다.
레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

### 예제 5: 레코드 집합에서 NS 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 NS 레코드를 제거 합니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

### 예제 6: 레코드 집합에서 PTR 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 PTR 레코드를 제거 합니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

### 예제 7: 레코드 집합에서 SRV 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 SRV 레코드를 제거 합니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

### 예제 8: 레코드 집합에서 TXT 레코드 제거
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

이 예제에서는 기존 레코드 집합에서 TXT 레코드를 제거 합니다.
레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.
레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.

## 변수

### -Cname
CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exchange
메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
A 레코드에 대 한 IPv4 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
NS (이름 서버) 레코드에 대 한 이름 서버를 지정 합니다.

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -포트
서비스 (SRV) 레코드의 포트를 지정 합니다.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -기본 설정
MX 레코드에 대 한 기본 설정을 지정 합니다.

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -우선 순위
SRV 레코드에 대 한 우선 순위를 지정 합니다.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
포인터 (PTR) 레코드의 대상 도메인 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -레코드 집합
제거할 레코드가 포함 된 **레코드 집합** 개체를 지정 합니다.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -대상
SRV 레코드의 대상을 지정 합니다.

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -값
TXT 레코드에 대 한 값을 지정 합니다.

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -중량
SRV 레코드의 가중치를 지정 합니다.

```yaml
Type: UInt16
Parameter Sets: SRV
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

### Microsoft Azure. DnsRecordSet
이 cmdlet에 **Dnsrecordset** 개체를 파이프 할 수 있습니다.
이는 레코드 집합의 오프 라인 표현이 며, Set-AzureRmDnsRecordSet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.

## 출력

### Microsoft Azure. DnsRecordSet
이 cmdlet은 수정 된 **레코드 집합** 개체를 반환 합니다.

## 상속자

## 관련 링크

[추가-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
