---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: cd0e2f2913a950e677b1f7294076351556b81c80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005867"
---
# Remove-AzPrivateDnsRecordConfig

## SYNOPSIS
로컬 레코드 집합 개체에서 개인 DNS 레코드를 제거합니다.

## 구문

### A(기본값)
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AAAA
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PTR
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TXT
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CNAME
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Remove-AzPrivateDnsRecordConfig cmdlet은 레코드 집합에서 DNS(개인 도메인 이름 시스템) 레코드를 제거합니다. RecordSet 개체는 오프라인 개체로 변경되어 Microsoft Azure Private DNS 서비스에 대한 변경을 유지하기 위해 Set-AzPrivateDnsRecordSet cmdlet을 실행한 후에까지 개인 DNS 응답을 변경하지 않습니다. 레코드를 제거하려면 해당 레코드 형식의 모든 필드가 정확히 일치해야 합니다. SOA 레코드를 추가하거나 제거할 수 없습니다. SOA 레코드는 개인 DNS 영역이 만들어지면 자동으로 생성되고 개인 DNS 영역이 삭제될 때 자동으로 삭제됩니다. RecordSet 개체를 매개 변수로 또는 파이프라인 연산자를 사용하여 이 cmdlet에 전달할 수 있습니다.

## 예제

### 예제 1: 레코드 집합에서 A 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 A 레코드를 제거합니다. 레코드 집합의 유일한 레코드인 경우 결과는 빈 레코드 집합입니다. 레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.

### 예제 2: 레코드 집합에서 AAAA 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 AAAA 레코드를 제거합니다. 레코드 집합의 유일한 레코드인 경우 결과는 빈 레코드 집합입니다. 레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.

### 예제 3: 레코드 집합에서 CNAME 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 CNAME 레코드를 제거합니다. CNAME 레코드 집합에 최대 하나의 레코드가 포함될 수 있기 때문에 결과는 빈 레코드 집합입니다.

### 예제 4: 레코드 집합에서 MX 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 MX 레코드를 제거합니다. 레코드 이름 "@"은 영역 정수에 있는 레코드 집합을 나타냅니다. 레코드 집합의 유일한 레코드인 경우 결과는 빈 레코드 집합입니다. 레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.

### 예제 5: 레코드 집합에서 PTR 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 PTR 레코드를 제거합니다. 레코드 집합의 유일한 레코드인 경우 결과는 빈 레코드 집합입니다. 레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.

### 예제 6: 레코드 집합에서 SRV 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 SRV 레코드를 제거합니다. 레코드 집합의 유일한 레코드인 경우 결과는 빈 레코드 집합입니다. 레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.

### 예제 7: 레코드 집합에서 TXT 레코드 제거
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

이 예제에서는 기존 레코드 집합에서 TXT 레코드를 제거합니다. 레코드 집합의 유일한 레코드인 경우 결과는 빈 레코드 집합입니다. 레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.

## 매개 변수

### -Cname
제거할 CNAME 레코드의 정형 이름입니다.
영역의 이름과 상대적이면 안 됩니다.
종료점이 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
제거할 MX 레코드의 메일 교환 호스트입니다.
영역의 이름과 상대적이면 안 됩니다.
종료점이 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv4Address
제거할 A 레코드의 IPv4 주소입니다.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipv6Address
제거할 AAAA 레코드의 IPv6 주소입니다.

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Port
제거할 SRV 레코드의 포트 번호입니다.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -기본 설정
제거할 MX 레코드의 기본 설정 값입니다.

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
제거할 SRV 레코드의 우선 순위 값입니다.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ptrdname
제거할 PTR 레코드의 대상 호스트입니다.
영역의 이름과 상대적이면 안 됩니다.
종료점이 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
레코드를 제거할 레코드 집합입니다.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Target
제거할 SRV 레코드의 대상 호스트입니다.
영역의 이름과 상대적이면 안 됩니다.
종료점이 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
제거할 TXT 레코드의 텍스트 값입니다.

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
제거할 SRV 레코드의 가중치 값입니다.

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet

## 출력

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet

## 참고 사항

## 관련 링크
