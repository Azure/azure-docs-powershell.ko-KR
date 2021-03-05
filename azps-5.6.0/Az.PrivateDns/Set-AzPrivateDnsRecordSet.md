---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 68e55ae6a0c563ecc72e74fc127360ddb35f73f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986687"
---
# Set-AzPrivateDnsRecordSet

## SYNOPSIS
개인 DNS 영역의 레코드 집합을 업데이트/설정합니다.

## 구문

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Set-AzPrivateDnsRecordSet cmdlet은 로컬 RecordSet 개체에서 Azure Private DNS 서비스에서 레코드 집합을 업데이트합니다. RecordSet 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달할 수 있습니다. 확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다. 로컬 RecordSet 개체를 검색한 후 Azure Private DNS에서 레코드 집합이 변경된 경우 레코드 집합이 업데이트되지 않습니다. 이 기능은 동시 변경에 대한 보호를 제공합니다. 동시 변경 내용에 관계없이 레코드 집합을 업데이트하는 덮어 덮어 사용 매개 변수를 사용하여 이 동작을 억제할 수 있습니다.

## 예제

### 예제 1: 레코드 집합 업데이트
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

첫 번째 명령은 Get-AzPrivateDnsRecordSet cmdlet을 사용하여 지정된 레코드 집합을 구한 다음 해당 $RecordSet 저장합니다. 두 번째 및 세 번째 명령은 레코드 집합에 두 개의 A 레코드를 추가하는 오프라인 작업입니다. 최종 명령은 Set-AzPrivateDnsRecordSet cmdlet을 사용하여 업데이트를 커밋합니다.

### 예제 2: SOA 레코드 업데이트
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

첫 번째 명령은 Get-AzPrivateDnsRecordSet cmdlet을 사용하여 지정된 레코드 집합을 구한 다음 해당 $RecordSet 저장합니다. 두 번째 명령은 지정된 SOA 레코드를 $RecordSet. 최종 명령은 Set-AzPrivateDnsRecordSet cmdlet을 사용하여 $RecordSet.

## 매개 변수

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

### -덮어 덮어 덮어 덮어 덮어
낙관적 동시성 검사를 위해 RecordSet 매개 변수의 ETag 필드를 사용하지 않습니다.

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
레코드를 추가할 레코드 집합입니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
