---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872813"
---
# Set-AzPrivateDnsVirtualNetworkLink

## SYNOPSIS
개인 영역 및 리소스 그룹과 연결 된 가상 네트워크 링크를 업데이트/설정 합니다.

## 구문과

### 필드 (기본값)
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### 오브젝트가
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 리소스
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**Set-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정 된 리소스 그룹의 영역과 연결 된 링크를 업데이트 합니다.
*Link* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달 하거나 *이름* *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.
확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.
**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 영역을 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색 된 이후 Azure DNS에서 변경 된 링크가 업데이트 되지 않습니다. 이는 동시 링크 변경에 대 한 보호를 제공 합니다. 이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경에 관계 없이 링크를 업데이트 합니다.

## 예제의

### 예제 1: 링크 설정
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

이 명령은 Mylink 이라는 리소스 그룹의 myzone.com 이라는 영역에 연결 된 mylink 링크에 대해 IsRegistrationEnabled를 True로 설정 합니다.

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

### -InputObject
설정할 가상 네트워크 링크 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsRegistrationEnabled
가상 네트워크 링크에서 등록을 사용할 수 있는지 여부를 나타내는 부울입니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 제거 하는 링크의 이름을 지정 합니다.
또한 *ResourceGroupName* 및 *ZoneName* 매개 변수를 지정 해야 합니다.
또는 *링크* 매개 변수를 사용 하 여 개인 DNS 링크를 지정할 수도 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 링크를 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색 된 이후 Azure DNS에서 변경 된 링크가 삭제 되지 않습니다.
이는 동시 링크 변경에 대 한 보호를 제공 합니다.
이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며,이는 동시 변경에 관계 없이 링크를 삭제 하는 것입니다.

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

### -ResourceGroupName
제거할 링크가 포함 된 리소스 그룹의 이름을 지정 합니다.
*ZoneName* 및 *Name* 매개 변수도 지정 해야 합니다.
또는 파이프라인 또는 *링크* 매개 변수를 통해 전달 되는 **PSPrivateDnsVirtualNetworkLink** 개체를 사용 하 여 가상 네트워크 링크를 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
개인 DNS 영역 ResourceID

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
리소스 태그를 나타내는 해시 테이블입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneName
이 cmdlet이 제거 하는 DNS 영역의 이름을 지정 합니다.
또한 *Name* 및 *ResourceGroupName* 매개 변수를 지정 해야 합니다.
또는 *링크* 매개 변수를 사용 하 여 개인 DNS 링크를 지정할 수도 있습니다.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PrivateDns. PSPrivateDnsVirtualNetworkLink/.

### System. 문자열

## 출력

### PrivateDns. PSPrivateDnsVirtualNetworkLink/.

## 상속자

## 관련 링크

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[새로운 AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
