---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 21e02077e7c2644c622a3f290a82fa26d7d6fc64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699771"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## SYNOPSIS
리소스 그룹에서 가상 네트워크 링크를 제거 합니다.

## 구문과

### 필드 (기본값)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 오브젝트가
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 리소스
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzPrivateDnsVirtualNetworkLink** cmdlet은 지정 된 리소스 그룹에서 DNS (사설 Domain Name System) 링크를 영구적으로 삭제 합니다.
*Link* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달 하거나 *이름* *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.
확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.
**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 링크를 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체를 검색 한 후에 해당 링크가 Azure Private DNS에서 변경 된 경우에는 삭제 되지 않습니다. 이는 동시 영역 변경에 대 한 보호를 제공 합니다. 이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.

## 예제의

### 예제 1: 링크 제거
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

이 명령은 Mylink 이라는 리소스 그룹에서 myzone.com 영역에 연결 된 mylink 링크를 제거 합니다.

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
제거할 가상 네트워크 링크 개체입니다.

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

### -이름
삭제할 링크의 이름을 지정 합니다.
또한 *ResourceGroupName* 및 *ZoneName* 매개 변수를 지정 해야 합니다.
또는 *link* 매개 변수를 사용 하 여 링크를 지정할 수도 있습니다.

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
**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 영역을 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체를 검색 한 후 Azure DNS에서 해당 영역이 변경 되 면 해당 영역은 삭제 되지 않습니다.
이는 동시 영역 변경에 대 한 보호를 제공 합니다.
이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.

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
작업의 결과를 전달 하는 데 사용 됩니다 (부울). 파이프라인의 가상 네트워크 링크 삭제

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

### -ResourceGroupName
제거할 링크가 포함 된 리소스 그룹의 이름을 지정 합니다.
*ZoneName* 및 *Name* 매개 변수도 지정 해야 합니다.
또는 파이프라인 또는 *링크* 매개 변수를 통해 전달 되는 **PSPrivateDnsVirtualNetworkLink** 개체를 사용 하 여 DNS 영역을 지정할 수도 있습니다.

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
링크의 ARM 리소스 ID를 지정 합니다.

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

### -ZoneName
링크가 연결 된 개인 DNS 영역의 이름을 지정 합니다.
또한 *ResourceGroupName* 및 *Name* 매개 변수를 지정 해야 합니다.
또는 *link* 매개 변수를 사용 하 여 링크를 지정할 수도 있습니다.

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

### 시스템 부울

## 상속자

## 관련 링크

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[새로운 AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
