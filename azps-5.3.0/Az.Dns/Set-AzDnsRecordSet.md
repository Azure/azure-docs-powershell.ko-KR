---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489836"
---
# Set-AzDnsRecordSet

## SYNOPSIS
DNS 레코드 집합을 업데이트합니다.

## 구문

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzDnsRecordSet** cmdlet은 로컬 **RecordSet** 개체에서 Azure DNS 서비스의 레코드 집합을 업데이트합니다.
**RecordSet** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달할 수 있습니다.
*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 변경된 레코드 집합은 업데이트되지 않습니다.
이렇게 하면 동시 변경에 대한 보호를 제공합니다.
동시 변경 내용에 관계없이 레코드 집합을 업데이트하는 *덮어* 사용 매개 변수를 사용하여 이 동작을 표시하지 않습니다.

## 예제

### 예제 1: 레코드 집합 업데이트
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

첫 번째 명령은 Get-AzDnsRecordSet cmdlet을 사용하여 지정된 레코드 집합을 구한 다음, $RecordSet 변수에 저장합니다.
두 번째 및 세 번째 명령은 레코드 집합에 두 개의 A 레코드를 추가하는 오프 라인 작업입니다.
마지막 명령은 **Set-AzDnsRecordSet** cmdlet을 사용하여 업데이트를 커밋합니다.

### 예제 2: SOA 레코드 업데이트
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

첫 번째 명령은 **Get-AzDnsRecordset** cmdlet을 사용하여 지정된 레코드 집합을 구한 다음, $RecordSet 변수에 저장합니다.
두 번째 명령은 지정된 SOA 레코드를 $RecordSet.
마지막 명령은 **Set-AzDnsRecordSet** cmdlet을 사용하여 업데이트가 $RecordSet.

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

### -Overwrite
동시 변경 내용에 관계없이 레코드 집합을 업데이트하는지 나타냅니다.
로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 변경된 레코드 집합은 업데이트되지 않습니다.
이렇게 하면 동시 변경에 대한 보호를 제공합니다.
이 동작을 표시하지 않는  경우 덮어 사용 매개 변수를 사용하면 동시 변경 내용에 관계없이 레코드 집합이 업데이트됩니다.

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
업데이트할 **RecordSet을** 지정합니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## 출력

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## 참고 사항
*확인* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.
*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.
*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다. 

## 관련 링크

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
