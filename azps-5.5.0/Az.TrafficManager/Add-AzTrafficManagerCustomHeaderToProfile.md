---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207533"
---
# Add-AzTrafficManagerCustomHeaderToProfile

## SYNOPSIS
로컬 Traffic Manager 프로필 개체에 사용자 지정 헤더 정보를 추가합니다.

## 구문

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Add-AzTrafficManagerCustomHeaderToProfile** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 사용자 지정 헤더 정보를 추가합니다.
New-AzTrafficManagerProfile cmdlet을 사용하여 프로필을 Get-AzTrafficManagerProfile 있습니다.

이 cmdlet은 로컬 프로필 개체에서 작동됩니다.
Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager에 대한 프로필에 변경 내용을 커밋합니다.

## 예제

### 예제 1: 프로필에 사용자 지정 헤더 정보 추가
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.
이 명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.
두 번째 명령은 사용자 지정 헤더 정보를 사용자 지정 헤더에 저장된 프로필에 $TrafficManagerProfile.
마지막 명령은 Traffic Manager의 프로필을 업데이트하여 트래픽 관리자의 로컬 값과 $TrafficManagerProfile.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
추가할 사용자 지정 헤더 정보의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
로컬 **TrafficManagerProfile** 개체를 지정합니다.
이 cmdlet은 이 로컬 개체를 수정합니다.
**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Value
추가할 사용자 지정 헤더 정보의 값을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## 출력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## 참고 사항

## 관련 링크

[Remove-AzTrafficManagerCustomHeaderFromProfile](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)
