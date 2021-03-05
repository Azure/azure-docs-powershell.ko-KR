---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984830"
---
# Get-AzDnsRecordSet

## SYNOPSIS
DNS 레코드 집합을 얻습니다.

## 구문

### 필드
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 개체
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzDnsRecordSet** cmdlet은 지정된 이름과 형식이 지정된 영역의 DNS(도메인 이름 시스템) 레코드 집합을 얻습니다.
Name 또는 *RecordType* 매개 변수를 지정하지 않으면 이 cmdlet은 영역의 지정된 형식의 모든 레코드 집합을 반환합니다. 
*RecordType* 매개 변수를 지정하지만 *이름* 매개 변수가 아닌 경우 이 cmdlet은 지정된 레코드 형식의 모든 레코드 집합을 반환합니다.
파이프라인 연산자를 사용하여 **DnsZone** 개체를 이 cmdlet에 전달하거나 **DnsZone** 개체를 영역  매개 변수로 전달하거나 또는 이름으로 영역 및 리소스 그룹을 지정할 수 있습니다.

## 예제

### 예제 1: 지정된 이름 및 형식이 있는 레코드 집합을 얻게 됩니다.
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

이 명령은 지정된 리소스 그룹 및 영역의 www라는 레코드 형식 A의 레코드 집합을 얻은 다음, $RecordSet 변수에 저장합니다.
Name *및* *RecordType* 매개 변수가 지정되어 있기 때문에 **RecordSet** 개체 하나만 반환됩니다.

### 예제 2: 지정된 형식의 레코드 집합을 얻게 됩니다.
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

이 명령은 MyResourceGroup이라는 리소스 그룹에 있는 myzone.com 영역의 레코드 형식 A의 모든 레코드 집합의 배열을 $RecordSets 변수에 저장합니다.

### 예제 3: 영역의 모든 레코드 집합을 얻습니다.
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

이 명령은 MyResourceGroup이라는 리소스 그룹에 있는 myzone.com 영역의 모든 레코드 집합의 배열을 구한 다음, 해당 레코드 집합을 $RecordSets 변수에 저장합니다.

### 예제 4: DnsZone 개체를 사용하여 영역의 모든 레코드 집합을 얻습니다.
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

이 예제는 위의 예제 3과 같습니다.
이번에는 영역 개체를 사용하여 영역이 지정됩니다.

## 매개 변수

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

### -Name
얻을 **RecordSet의 이름을** 지정합니다.
이름 매개 변수를  지정하지 않으면 지정된 형식의 모든 레코드 집합이 반환됩니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
이 cmdlet에서 얻을 DNS 레코드 유형을 지정합니다.
유효한 값은: 
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT *RecordType* 매개 변수를 지정하지 않으면 이름 매개 변수도 *생략해야* 합니다. 그런 다음 이 cmdlet은 영역의 모든 레코드 집합(모든 이름 및 형식)을 반환합니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
DNS 영역이 포함된 리소스 그룹을 지정합니다.
ZoneName 매개 변수를 사용하여 영역 이름을 *지정해야* 합니다.
또는 영역 매개 변수를 사용하여 **DnsZone** 개체에 전달하여 영역 및 리소스 그룹을 *지정할 수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
이 cmdlet이 얻을 레코드 집합을 포함하는 DNS 영역이 지정됩니다.
또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지역을 지정할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
얻을 레코드 집합이 포함된 DNS 영역의 이름을 지정합니다.
*ResourceGroupName* 매개 변수를 사용하여 영역이 포함된 리소스 그룹도 지정해야 합니다.
또는 영역 매개 변수를 사용하여 DNS 영역 개체에 전달하여 영역 및 리소스 그룹을 *지정할 수* 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
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

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## 출력

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## 참고 사항

## 관련 링크

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


