---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034467"
---
# Set-AzPrivateDnsRecordSet

## SYNOPSIS
개인 DNS 영역에서 레코드 집합을 업데이트/설정 합니다.

## 구문과

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Set-AzPrivateDnsRecordSet cmdlet은 로컬 RecordSet 개체에서 Azure 개인 DNS 서비스에 집합 된 레코드를 업데이트 합니다. 레코드 집합 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용할 수 있습니다. 확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다. 로컬 RecordSet 개체를 검색 한 후 Azure 비공개 DNS에서 레코드 집합이 변경 되는 경우 해당 레코드가 업데이트 되지 않습니다. 이는 동시 변경에 대 한 보호를 제공 합니다. 동시 변경 내용에 관계 없이 레코드 집합을 업데이트 하는 Overwrite 매개 변수를 사용 하 여이 동작을 억제할 수 있습니다.

## 예제의

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

첫 번째 명령은 Get-AzPrivateDnsRecordSet cmdlet을 사용 하 여 지정 된 레코드 집합을 얻은 다음 $RecordSet 변수에 저장 합니다. 두 번째 및 세 번째 명령은 레코드 집합에 두 개의 레코드를 추가 하는 오프 라인 작업입니다. 마지막 명령은 Set-AzPrivateDnsRecordSet cmdlet을 사용 하 여 업데이트를 커밋합니다.

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

첫 번째 명령은 Get-AzPrivateDnsRecordSet cmdlet을 사용 하 여 지정 된 레코드 집합을 얻은 다음 $RecordSet 변수에 저장 합니다. 두 번째 명령은 $RecordSet에서 지정 된 SOA 레코드를 업데이트 합니다. 마지막 명령은 Set-AzPrivateDnsRecordSet cmdlet을 사용 하 여 $RecordSet에서 업데이트를 전파 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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
낙관적 동시성 검사에 레코드 집합 매개 변수의 ETag 필드를 사용 하지 마세요.

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
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PrivateDns. PSPrivateDnsRecordSet/.

## 출력

### PrivateDns. PSPrivateDnsRecordSet/.

## 상속자

## 관련 링크
