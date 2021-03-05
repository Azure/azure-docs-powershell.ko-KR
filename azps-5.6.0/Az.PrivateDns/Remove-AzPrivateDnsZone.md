---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: 8c8e7059a6c23c928180b8d6fab3cfdbbfd9ed5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970411"
---
# Remove-AzPrivateDnsZone

## SYNOPSIS
리소스 그룹에서 개인 DNS 영역이 제거됩니다.

## 구문

### 필드(기본값)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzPrivateDnsZone cmdlet은** 지정된 리소스 그룹에서 DNS(개인 도메인 이름 시스템) 영역이 영구적으로 삭제됩니다.
영역 내에 포함된 모든 레코드 집합도 삭제됩니다.
PrivateZone 매개 변수를 사용하여  **PrivateDnsZone** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. 
확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.
PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정하는 경우 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 직접 작업만 변경으로 수, 영역 내의 레코드 집합의 작업은 변경되지 않습니다). 
그러면 동시 영역 변경에 대한 보호가 제공됩니다.
이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. 

## 예제

### 예제 1: 개인 영역 제거
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

이 명령은 MyResourceGroup이라는 리소스 myzone.com 그룹에서 이라는 영역이 제거됩니다.

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
이 cmdlet이 제거한 개인 DNS 영역의 이름을 지정합니다.
*ResourceGroupName 매개 변수도 지정해야* 합니다.
또는 영역 매개 변수를 사용하여 DNS 지역을 *지정할 수* 있습니다.

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
PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정하는 경우 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 직접 작업만 변경으로 수, 영역 내의 레코드 집합의 작업은 변경되지 않습니다). 
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
작업의 결과(부울)를 전달하는 데 사용됩니다.

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

### -PrivateZone
삭제할 개인 영역 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
제거할 영역이 포함된 리소스 그룹의 이름을 지정합니다.
*ZoneName 매개 변수도 지정해야* 합니다.
또는 파이프라인 또는 영역 매개 변수를 통해 전달되는 **PrivateDnsZone** 개체를 사용하여 DNS 영역을 *지정할 수* 있습니다.

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
개인 DNS 영역 ResourceID.

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

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

### System.String

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
