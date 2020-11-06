---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9db3efc71b751f291c5bb8636246ed6927200c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527584"
---
# Set-AzureRmDnsRecordSet

## SYNOPSIS
DNS 레코드 집합을 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmDnsRecordSet** cmdlet은 로컬 **RecordSet** 개체에서 Azure DNS 서비스의 레코드 집합을 업데이트 합니다.

**레코드 집합** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용할 수 있습니다.

*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.

로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 된 경우에는 해당 레코드가 업데이트 되지 않습니다.
이는 동시 변경에 대 한 보호를 제공 합니다.
동시 변경 내용에 관계 없이 레코드 집합을 업데이트 하는 *Overwrite* 매개 변수를 사용 하 여이 동작을 억제할 수 있습니다.

## 예제의

### 예제 1: 레코드 집합 업데이트
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

첫 번째 명령은 Get-AzureRmDnsRecordSet cmdlet을 사용 하 여 지정 된 레코드 집합을 얻은 다음 $RecordSet 변수에 저장 합니다.

두 번째 및 세 번째 명령은 레코드 집합에 두 개의 레코드를 추가 하는 오프 라인 작업입니다.

마지막 명령은 **Set-AzureRmDnsRecordSet** cmdlet을 사용 하 여 업데이트를 커밋합니다.

### 예제 2: SOA 레코드 업데이트
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

첫 번째 명령은 **AzureRmDnsRecordset** cmdlet을 사용 하 여 지정 된 레코드 집합을 얻은 다음 $RecordSet 변수에 저장 합니다.

두 번째 명령은 $RecordSet에서 지정 된 SOA 레코드를 업데이트 합니다.

마지막 명령은 **Set-AzureRmDnsRecordSet** cmdlet을 사용 하 여 $RecordSet에서 업데이트를 전파 합니다.

## 변수

### -Overwrite
동시 변경 내용에 관계 없이 레코드 집합을 업데이트 하는 것을 나타냅니다.

로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 된 경우 업데이트 되지 않습니다.
이는 동시 변경에 대 한 보호를 제공 합니다.
이 동작을 생략 하려면 *Overwrite* 매개 변수를 사용 하 여 동시 변경 내용에 관계 없이 레코드 집합을 업데이트 합니다.

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

### -레코드 집합
업데이트할 **레코드 집합** 을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft Azure. DnsRecordSet
이 cmdlet에 **RecordSet** 개체를 전달할 수 있습니다.

## 출력

### Microsoft Azure. DnsRecordSet
이 cmdlet은 업데이트 된 **레코드 집합** 개체를 나타내는 개체를 반환 합니다.

## 상속자
*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.

*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.
*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다. 

## 관련 링크

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[새로운 AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[제거-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)
