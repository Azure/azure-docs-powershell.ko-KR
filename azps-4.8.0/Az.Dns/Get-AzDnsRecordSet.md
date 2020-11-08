---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056368"
---
# Get-AzDnsRecordSet

## SYNOPSIS
DNS 레코드 집합을 가져옵니다.

## 구문과

### 필드인
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 오브젝트가
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 이름 및 형식으로 DNS (Domain Name System) 레코드 집합을 가져옵니다.
*Name* 또는 *RecordType* 매개 변수를 지정 하지 않으면이 cmdlet은 영역에 지정 된 형식의 모든 레코드 집합을 반환 합니다.
*Name* 매개 변수를 제외한 *RecordType* 매개 변수를 지정 하면이 cmdlet은 지정 된 레코드 형식의 모든 레코드 집합을 반환 합니다.
파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역과 리소스 그룹을 지정할 수 있습니다.

## 예제의

### 예제 1: 지정 된 이름 및 형식으로 레코드 집합 가져오기
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

이 명령은 지정 된 리소스 그룹 및 영역에서 www 라는 레코드 종류의 레코드 집합을 가져온 다음이를 $RecordSet 변수에 저장 합니다.
*Name* 및 *RecordType* 매개 변수는 지정 되어 있으므로 하나의 **레코드 집합** 개체만 반환 됩니다.

### 예제 2: 지정 된 형식의 레코드 집합 가져오기
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

이 명령은 MyResourceGroup 이라는 리소스 그룹에 있는 myzone.com 이라는 영역에 있는 레코드 종류 A의 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.

### 예제 3: 영역의 모든 레코드 집합 가져오기
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 영역에 있는 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.

### 예제 4: DnsZone 개체를 사용 하 여 영역의 모든 레코드 집합 가져오기
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

이 예제는 위의 예제 3과 동일 합니다.
이번에는 zone 개체를 사용 하 여 영역이 지정 됩니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -이름
가져올 **레코드 집합** 의 이름을 지정 합니다.
*Name* 매개 변수를 지정 하지 않으면 지정 된 형식의 모든 레코드 집합이 반환 됩니다.

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
이 cmdlet이 가져오는 DNS 레코드의 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 
- 에서
- AAAA
- CNAME
- 멕시코
- NS
- PTR 레코드로
- SOA
- SRV
- TXT *RecordType* 매개 변수를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다. 그런 다음이 cmdlet은 모든 이름과 형식의 영역에 있는 모든 레코드 집합을 반환 합니다.

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
DNS 영역이 포함 된 리소스 그룹을 지정 합니다.
*ZoneName* 매개 변수를 사용 하 여 영역 이름도 지정 해야 합니다.
또는 *zone* 매개 변수를 사용 하 여 **DnsZone** 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.

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
이 cmdlet이 가져오는 레코드 집합을 포함 하는 DNS 영역을 지정 합니다.
또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.

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
가져올 레코드 집합을 포함 하는 DNS 영역의 이름을 지정 합니다.
*ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹도 지정 해야 합니다.
또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### DnsZone에 대 한 명령

### 시스템 Null 허용 ' 1 [[RecordType, Microsoft azure. 관리. Dns, 버전 = 3.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]

## 출력

### Microsoft Azure. DnsRecordSet

## 상속자

## 관련 링크

[새로운 AzDnsRecordSet](./New-AzDnsRecordSet.md)

[제거-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


