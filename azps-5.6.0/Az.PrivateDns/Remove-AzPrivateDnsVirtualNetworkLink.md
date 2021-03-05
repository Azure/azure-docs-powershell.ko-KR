---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965552"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## SYNOPSIS
리소스 그룹에서 가상 네트워크 링크를 제거합니다.

## 구문

### 필드(기본값)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹에서 DNS(개인 도메인 이름 시스템) 링크를 영구적으로 삭제합니다.
링크 매개 변수를 사용하여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름  *영역* 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. 
확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.
**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 링크를 지정할 때(파이프라인 또는  링크 매개 변수를 통해 전달) 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure Private DNS에서 변경된 경우 링크가 삭제되지 않습니다. 그러면 동시 영역 변경에 대한 보호가 제공됩니다. 이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. 

## 예제

### 예제 1: 링크 제거
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

이 명령은 MyResourceGroup이라는 리소스 myzone.com 영역과 연결된 mylink라는 링크를 제거합니다.

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

### -Name
삭제할 링크의 이름을 지정합니다.
*ResourceGroupName* 및 *ZoneName 매개 변수도 지정해야* 합니다.
또는 링크 매개 변수를 사용하여 링크를 지정할 *수* 있습니다.

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

### -덮어 덮어 덮어 덮어 덮어
**PSPrivateDnsVirtualNetworkLink** 개체(파이프라인 또는 링크 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 영역이 변경된 경우 해당 영역은 삭제되지 않습니다.
그러면 동시 영역 변경에 대한 보호가 제공됩니다.
이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. 

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
작업 삭제 가상 네트워크 링크의 결과(부울)를 파이프라인 아래로 전달하는 데 사용됩니다.

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
제거할 링크가 포함된 리소스 그룹의 이름을 지정합니다.
*ZoneName* 및 Name 매개 변수도 *지정해야* 합니다.
또는 파이프라인 또는 링크 매개 변수를 통해 전달된 **PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 DNS 지역을 지정할 *수* 있습니다.

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
링크의 ARM 리소스 ID를 지정합니다.

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
링크가 연결된 개인 DNS 영역의 이름을 지정합니다.
*ResourceGroupName 및 Name* 매개 변수도 *지정해야* 합니다.
또는 링크 매개 변수를 사용하여 링크를 지정할 *수* 있습니다.

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

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink

### System.String

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
