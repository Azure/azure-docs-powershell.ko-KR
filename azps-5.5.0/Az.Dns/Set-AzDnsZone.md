---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185988"
---
# Set-AzDnsZone

## SYNOPSIS
DNS 영역의 속성을 업데이트합니다.

## 구문

### 필드(기본값)
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FieldsObjects
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Set-AzDnsZone** cmdlet은 Azure DNS 서비스에서 지정된 DNS 영역이 업데이트됩니다.
이 cmdlet은 영역의 레코드 집합을 업데이트하지 않습니다.
**DnsZone** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.
*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
DNS 영역이 개체로 전달될 때(영역 개체 사용 또는 파이프라인을 통해) 로컬 DnsZone 개체를 검색한 후 Azure DNS에서 변경된 경우 업데이트되지 않습니다. 이렇게 하면 동시 변경에 대한 보호를 제공합니다. 동시 변경 내용에 관계없이 영역이 업데이트되는 *덮어* 사용 매개 변수를 사용하면 이 동작을 표시하지 않습니다.

## 예제

### 예제 1: DNS 영역 업데이트
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

첫 번째 명령은 지정된 리소스 myzone.com 그룹에서 이름이 지정된 영역으로 지정된 $Zone 저장합니다.
두 번째 명령은 다음에 대한 태그를 $Zone.
마지막 명령은 변경을 커밋합니다.

### 예제 2: 영역의 태그 업데이트
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

이 명령은 먼저 해당 myzone.com 없이 이름 있는 영역의 태그를 업데이트합니다.

### 예제 3: ID를 지정하여 개인 영역과 가상 네트워크 연결
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

이 명령은 ID를 myprivatezone.com 등록 네트워크로 가상 네트워크 myvnet과 개인 DNS 영역 서버를 연결합니다.

### 예제 4: 네트워크 개체를 지정하여 개인 영역과 가상 네트워크 연결
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

이 명령은 $vnet 변수로 표현되는 가상 네트워크 개체를 myprivatezone.com cmdlet에 전달하여 가상 네트워크 myvnet과 개인 DNS 영역 Set-AzDnsZone 연결합니다.

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
업데이트할 DNS 영역의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
DNS 영역이 개체로 전달될 때(영역 개체 사용 또는 파이프라인을 통해) 로컬 DnsZone 개체를 검색한 후 Azure DNS에서 변경된 경우 업데이트되지 않습니다. 이렇게 하면 동시 변경에 대한 보호를 제공합니다. 동시 변경 내용에 관계없이 영역이 업데이트되는 *덮어* 사용 매개 변수를 사용하면 이 동작을 표시하지 않습니다.

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

### -RegistrationVirtualNetwork
이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 사설 영역만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록할 가상 네트워크 신분의 목록으로, 사설 영역만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 사설 영역만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 신분의 목록으로, 사설 영역만 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
업데이트할 영역이 포함된 리소스 그룹의 이름을 지정합니다.
ZoneName 매개 변수도 지정해야 합니다.
또는 Zone 매개 변수 또는 파이프라인과 함께 DnsZone 개체를 사용하여 영역을 지정할 수 있습니다. 

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
업데이트할 DNS 영역이 지정됩니다.
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

### System.String

### System.Collections.Hashtable

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### Microsoft.Azure.Commands.Dns.DnsZone

## 출력

### Microsoft.Azure.Commands.Dns.DnsZone

## 참고 사항
*Confirm* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.
기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.
*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.
*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.

## 관련 링크

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
