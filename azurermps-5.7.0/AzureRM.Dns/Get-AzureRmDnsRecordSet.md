---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532848"
---
# Get-AzureRmDnsRecordSet

## SYNOPSIS
DNS 레코드 집합을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 필드인
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 오브젝트가
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 이름 및 형식으로 DNS (Domain Name System) 레코드 집합을 가져옵니다.

*Name* 또는 *RecordType* 매개 변수를 지정 하지 않으면이 cmdlet은 영역에 지정 된 형식의 모든 레코드 집합을 반환 합니다.
*Name* 매개 변수를 제외한 *RecordType* 매개 변수를 지정 하면이 cmdlet은 지정 된 레코드 형식의 모든 레코드 집합을 반환 합니다.

파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역과 리소스 그룹을 지정할 수 있습니다.

## 예제의

### 예제 1: 지정 된 이름 및 형식으로 레코드 집합 가져오기
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

이 명령은 지정 된 리소스 그룹 및 영역에서 www 라는 레코드 종류의 레코드 집합을 가져온 다음이를 $RecordSet 변수에 저장 합니다.
*Name* 및 *RecordType* 매개 변수는 지정 되어 있으므로 하나의 **레코드 집합** 개체만 반환 됩니다.

### 예제 2: 지정 된 형식의 레코드 집합 가져오기
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

이 명령은 MyResourceGroup 이라는 리소스 그룹에 있는 myzone.com 이라는 영역에 있는 레코드 종류 A의 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.

### 예제 3: 영역의 모든 레코드 집합 가져오기
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 영역에 있는 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.

### 예제 4: DnsZone 개체를 사용 하 여 영역의 모든 레코드 집합 가져오기
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

이 예제는 위의 예제 3과 동일 합니다.
이번에는 zone 개체를 사용 하 여 영역이 지정 됩니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
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
- 라는

*RecordType* 매개 변수를 지정 하지 않으면 *Name* 매개 변수도 생략 해야 합니다. 그런 다음이 cmdlet은 모든 이름과 형식의 영역에 있는 모든 레코드 집합을 반환 합니다.

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

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
이 cmdlet이 가져오는 레코드 집합을 포함 하는 DNS 영역을 지정 합니다.
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

### -ZoneName
가져올 레코드 집합을 포함 하는 DNS 영역의 이름을 지정 합니다.
*ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹도 지정 해야 합니다.

또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### DnsZone에 대 한 명령
**DnsZone** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.
**DnsZone** 개체는 **레코드 집합** 개체를 찾을 영역을 나타냅니다.

## 출력

### Microsoft Azure. DnsRecordSet
이 cmdlet은 검색 된 레코드 집합을 나타내는 하나 이상의 개체를 반환 합니다.
*Name* 및 *RecordType* 매개 변수를 지정한 경우 **레코드 집합** 을 하나만 반환 하 고, 그렇지 않으면 여러 **레코드 집합** 개체가 배열로 반환 됩니다.

## 상속자

## 관련 링크

[새로운 AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[제거-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


