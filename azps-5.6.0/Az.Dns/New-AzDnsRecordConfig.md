---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: c85cc0b4ad60529cc57becb9ca864751d90a37c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984802"
---
# New-AzDnsRecordConfig

## SYNOPSIS
새 DNS 레코드 로컬 개체를 만듭니다.

## 구문

### A
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Aaaa
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Ns
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Mx
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Ptr
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Txt
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Srv
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Caa
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzDnsRecordConfig** cmdlet은 로컬 **DnsRecord 개체를 만듭니다.**
이러한 개체의 배열은 *dnsRecords* 매개 변수를 사용하여 New-AzDnsRecordSet cmdlet에 전달되어 레코드 집합에서 만들 레코드를 지정합니다.

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
레코드 집합은 A 형식의 TTL이 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.

### 예제 2: AAAA 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 AAAA 형식이고 TTL이 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 3: CNAME 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 CNAME 형식이며 TTL은 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 4: MX 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역 집합에 www라는 **RecordSet을** myzone.com.
레코드 집합은 MX 형식이고 TTL은 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 5: NS 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 해당 영역의 ns1이라는 **RecordSet을** myzone.com.
레코드 집합은 NS 형식이고 TTL은 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 6: PTR 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

이 명령은 **4라는 RecordSet을** 3.2.1.in-addr.arpa를 만듭니다.
레코드 집합은 PTR 형식으로, TTL은 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 7: SRV 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 _sip._tcp라는 **RecordSet을** myzone.com.
레코드 집합은 SRV 형식이고 TTL은 1시간(3600초)입니다.
IP 주소 2001.2.3.4를 지적하는 단일 DNS 레코드가 포함되어 있습니다.
서비스(sip) 및 프로토콜(tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정됩니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

### 예제 8: TXT 형식의 RecordSet 만들기
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

이 명령은 영역의 **레코드 집합이라는** myzone.com.
레코드 집합은 TXT 형식이며 TTL은 1시간(3600초)입니다.
단일 DNS 레코드가 포함되어 있습니다.
한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.

## 매개 변수

### -CaaFlags
추가할 CAA 레코드의 플래그입니다. 0에서 255 사이의 숫자가 되어야 합니다.

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
추가할 CAA 레코드의 태그 필드입니다.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
추가할 CAA 레코드의 값 필드입니다.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cname
CNAME(정형 이름) 레코드에 대한 도메인 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Exchange
MX(메일 교환) 레코드에 대한 메일 교환 서버 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
A 레코드에 대한 IPv4 주소를 지정합니다.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
AAAA 레코드에 대한 IPv6 주소를 지정합니다.

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
NS(이름 서버) 레코드의 이름 서버 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
SRV(서비스) 레코드에 대한 포트를 지정합니다.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -기본 설정
MX 레코드에 대한 기본 설정을 지정합니다.

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
SRV 레코드에 대한 우선 순위를 지정합니다.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
포인터 리소스(PTR) 레코드의 대상 도메인 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Target
SRV 레코드에 대한 대상을 지정합니다.

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
TXT 레코드의 값을 지정합니다.

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
SRV 레코드에 대한 가중치를 지정합니다.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### System.UInt16

### System.Byte

## 출력

### Microsoft.Azure.Commands.Dns.DnsRecordBase

## 참고 사항

## 관련 링크

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordConfig](./Remove-AzDnsRecordConfig.md)
