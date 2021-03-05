---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 1864cc9d5975c9f959edb6be470e63a10cfa63f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987280"
---
# Remove-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager에서 엔드포인트를 제거합니다.

## 구문

### 필드
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 개체
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager에서 엔드포인트를 제거합니다.

이 cmdlet은 Traffic Manager 서비스에 대한 각 변경을 커밋합니다.
로컬 Traffic Manager 프로필 개체에서 여러 엔드포인트를 제거하고 단일 작업에서 변경 내용을 커밋하려면 Remove-AzTrafficManagerEndpointConfig cmdlet을 사용합니다.

파이프라인 연산자를 사용하여 **TrafficManagerEndpoint** 개체를 이 cmdlet에 전달하거나 **TrafficManagerEndpoint** 매개 변수를 사용하여 *TrafficManagerEndpoint* 개체를 지정할 수 있습니다.

또는 *ProfileName* 및 *ResourceGroupName*  매개  변수와 함께 이름 및 형식 매개 변수를 사용하여 엔드포인트 이름을 지정하고 입력할 수 있습니다.

## 예제

### 예제 1: 프로필에서 엔드포인트 제거
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

이 명령은 ResourceGroup11이라는 리소스 그룹의 ContosoProfile이라는 프로필에서 contoso라는 Azure 엔드포인트를 제거합니다.

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

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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

### -Name
이 cmdlet이 제거하는 Traffic Manager 엔드포인트의 이름을 지정합니다.

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

### -ProfileName
이 cmdlet에서 엔드포인트를 제거하는 Traffic Manager 프로필의 이름을 지정합니다.
프로필을 얻하려면 Get-AzTrafficManagerProfile cmdlet을 사용하세요.

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

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 그룹의 Traffic Manager 프로필에서 Traffic Manager 엔드포인트를 제거합니다.

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

### -TrafficManagerEndpoint
이 cmdlet이 제거하는 Traffic Manager 엔드포인트를 지정합니다.
**TrafficManagerEndpoint** 개체를 얻은 경우 Get-AzTrafficManagerEndpoint cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Type
이 cmdlet이 Traffic Manager 프로필에 추가하는 엔드포인트 유형을 지정합니다.
유효한 값은: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


