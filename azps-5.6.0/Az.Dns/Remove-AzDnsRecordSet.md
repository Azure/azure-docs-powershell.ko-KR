---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984774"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
레코드 집합을 삭제합니다.

## 구문

### 필드
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 혼합
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzDnsRecordSet** cmdlet은 지정된 영역의 지정된 레코드 집합을 삭제합니다.
영역 정수에서 자동으로 생성된 SOA 또는 NS(이름 서버) 레코드를 삭제할 수 없습니다.
파이프라인 연산자를 사용하여 또는 매개 변수로 **RecordSet** 개체를 이 cmdlet에 전달할 수 있습니다.
**RecordSet** 개체를 사용하지 않고 이름으로 설정된 레코드를 식별하고 형식을 지정하려면 파이프라인 연산자 또는 매개 변수로 이 cmdlet에 **DnsZone** 개체로 구역을 전달하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.
확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.
**RecordSet** 개체를 사용하여 레코드 집합을 지정할 때 로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 레코드 집합이 변경된 경우 레코드 집합이 삭제되지 않습니다.
이 기능은 동시 변경에 대한 보호를 제공합니다.
덮어 덮어  사용 매개 변수를 사용하여 이 기능을 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 레코드 집합을 삭제합니다.

## 예제

### 예제 1: 레코드 집합 제거
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

첫 번째 명령은 지정된 레코드 집합을 얻은 다음, 해당 레코드 집합을 $RecordSet 변수에 저장합니다. 두 번째 명령은 레코드 집합을 $RecordSet.

### 예제 2: 레코드 집합을 제거하고 모든 확인을 표시하지 않습니다.
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

첫 번째 명령은 지정된 레코드 집합을 얻습니다.
두 번째 명령은 레코드 집합이 그동안 변경된 경우에도 삭제됩니다.
확인 프롬프트가 억제됩니다.

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
제거할 **RecordSet의** 이름을 지정합니다.
이름으로 레코드 집합을 지정할 때 영역 매개 변수 또는  *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 DNS 영역이 지정되어야 합니다.
또는 *RecordSet* 매개 변수를 사용하여 **전달되는 RecordSet** 개체를 사용하여 레코드 집합을 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -덮어 덮어 덮어 덮어 덮어
**RecordSet** 개체를 사용하여 레코드 집합을 지정할 때 로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 레코드 집합이 변경된 경우 레코드 집합이 삭제되지 않습니다.
이 기능은 동시 변경에 대한 보호를 제공합니다.
이는 덮어 덮어 사용 매개 변수를 사용하여 억제될 수 있습니다. 이는 동시 변경 내용에 관계없이 레코드 집합을 삭제합니다. 

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
제거할 **RecordSet 개체를** 지정합니다.
또는 이름 및 영역 매개 변수를  사용하여 레코드 집합을 지정하거나 이름 *,* *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용할 수 있습니다. 

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
DNS 레코드 유형을 지정합니다.
유효한 값은:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- 영역이 삭제되면 TXT SOA 레코드가 자동으로 삭제됩니다.
SOA 레코드를 수동으로 삭제할 수 없습니다.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
삭제할 **RecordSet을** 포함하는 DNS 영역이 포함된 리소스 그룹을 지정합니다.
이 매개 변수는 이름 및 *ZoneName* 매개  변수를 사용하여 레코드 집합 및 DNS 영역이 지정된 경우만 적용할 수 있습니다.
또는 *RecordSet* 매개 변수 또는 이름 및 영역 매개 변수를 사용하여 레코드 집합을 *지정할* *수* 있습니다.

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
삭제할 **RecordSet이** 포함된 DNS 영역이 지정됩니다.
이 매개 변수는 이름 매개 변수를 사용하여 레코드 집합을 지정할 *때만 적용할 수* 있습니다.
또는 *RecordSet* 매개 변수 또는 이름 *,* *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 레코드 집합을 지정할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
삭제할 **RecordSet이** 포함된 영역의 이름을 지정합니다.
이름 및 *ResourceGroupName 매개 변수도 지정해야* 합니다. 
또는 *RecordSet* 매개 변수 또는 이름 및 영역 매개 변수를 사용하여 레코드 집합을 *지정할* *수* 있습니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## 출력

### System.Boolean

## 참고 사항
확인 매개  변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 중간 또는 더 낮은지 확인하라는 메시지를 묻는 메시지를 표시합니다.
확인 또는 *확인:$True* 지정하는 경우 이 cmdlet은 실행하기 전에 확인을 묻는 메시지를 표시합니다. 
*Confirm:$False* 지정하면 cmdlet에서 확인을 묻는 메시지가 표시되지 않습니다.

## 관련 링크

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
