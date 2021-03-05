---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987406"
---
# Add-AzTrafficManagerCustomHeaderToEndpoint

## SYNOPSIS
로컬 Traffic Manager 엔드포인트 개체에 사용자 지정 헤더 정보를 추가합니다.

## 구문

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet은 로컬 Azure Traffic Manager 엔드포인트 개체에 사용자 지정 헤더 정보를 추가합니다.
New-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 Get-AzTrafficManagerEndpoint 수 있습니다.

이 cmdlet은 로컬 엔드포인트 개체에서 작동합니다.
cmdlet을 사용하여 Traffic Manager의 엔드포인트에 Set-AzTrafficManagerEndpoint 커밋합니다.

## 예제

### 예제 1: 엔드포인트에 사용자 지정 헤더 정보 추가
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

첫 번째 명령은 **New-AzTrafficManagerEndpoint** cmdlet을 사용하여 Azure Traffic Manager 엔드포인트를 만듭니다.
명령은 로컬 엔드포인트를 $TrafficManagerEndpoint 저장합니다.
두 번째 명령은 사용자 지정 헤더 정보를 에 저장된 엔드포인트에 $TrafficManagerEndpoint.
마지막 명령은 Traffic Manager의 엔드포인트를 업데이트하여 로컬 값과 $TrafficManagerEndpoint.

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

### -TrafficManagerEndpoint
로컬 **TrafficManagerEndpoint 개체를 지정합니다.**
이 cmdlet은 이 로컬 개체를 수정합니다.
**TrafficManagerEndpoint** 개체를 얻은 경우 Get-AzTrafficManagerEndpoint cmdlet을 New-AzTrafficManagerEndpoint 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## 출력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## 참고 사항

## 관련 링크

[Remove-AzTrafficManagerCustomHeaderFromEndpoint](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
