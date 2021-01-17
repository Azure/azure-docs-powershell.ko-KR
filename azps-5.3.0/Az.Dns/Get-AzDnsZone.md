---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489859"
---
# Get-AzDnsZone

## SYNOPSIS
DNS 영역이 있습니다.

## 구문

### 기본값(기본값)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzDnsZone** cmdlet은 지정된 리소스 그룹에서 DNS(도메인 이름 시스템) 지역을 얻습니다.
Name 매개 *변수를 지정하면* 단일 **DnsZone** 개체가 반환됩니다.
Name 매개 변수를 *지정하지* 않으면 지정된 리소스 그룹의 모든 영역이 포함된 배열이 반환됩니다.
**DnsZone** 개체를 사용하여 영역 업데이트를 할 수 있습니다. 예를 들어 **RecordSet** 개체를 추가할 수 있습니다.

## 예제

### 예제 1: 영역 얻기
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

이 예제에서는 지정된 리소스 그룹에서 myzone.com DNS 영역의 이름을 지정한 다음, $Zone 변수에 저장합니다.

### 예제 2: 리소스 그룹의 모든 영역 얻기
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

이 예제에서는 지정된 리소스 그룹에 있는 모든 DNS 영역과 해당 DNS $Zones 저장합니다.

### 예제 3: 구독의 모든 영역 얻기
```
PS C:\> $Zones = Get-AzDnsZone
```

이 예제에서는 현재 Azure 구독의 모든 DNS 영역과 해당 DNS $Zones 저장합니다.

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

### -Name
얻을 DNS 영역의 이름을 지정합니다.
Name 매개 변수에 대한  값을 지정하지 않으면 이 cmdlet은 지정된 리소스 그룹의 모든 DNS 영역이 표시됩니다.
*ResourceGroupName* 매개 변수도 생략하면 이 cmdlet은 현재 Azure 구독의 모든 DNS 영역을 얻습니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
얻을 DNS 영역이 포함된 리소스 그룹의 이름을 지정합니다.
*ResourceGroupName을* 지정하지 않으면 이름 매개 변수도 *생략해야* 합니다.
이 경우 이 cmdlet은 현재 Azure 구독의 모든 DNS 영역을 얻습니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Dns.DnsZone

## 참고 사항

## 관련 링크

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
