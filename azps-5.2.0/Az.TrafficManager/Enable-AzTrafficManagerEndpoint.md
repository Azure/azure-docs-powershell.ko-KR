---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367158"
---
# Enable-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 프로필에서 엔드포인트를 사용할 수 있습니다.

## 구문

### 필드
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 개체
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Enable-AzTrafficManagerEndpoint** cmdlet을 사용하면 Azure Traffic Manager 프로필에서 엔드포인트를 사용할 수 있습니다.

파이프라인 연산자를 사용하여 **TrafficManagerEndpoint** 개체를 이 cmdlet에 전달하거나 **TrafficManagerEndpoint** 매개 변수를 사용하여 *TrafficManagerEndpoint* 개체를 지정할 수 있습니다.

또는 *ProfileName* 및 *ResourceGroupName*  매개 변수와 함께 이름 및 *형식* 매개 변수를 사용하여 엔드포인트 이름 및 형식을 지정할 수 있습니다.

## 예제

### 예제 1: 프로필에서 엔드포인트 사용
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

이 명령은 리소스 그룹 ResourceGroup11의 ContosoProfile 프로필에서 contoso라는 외부 엔드포인트를 사용할 수 있습니다.

### 예제 2: 파이프라인을 사용하여 엔드포인트 사용
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

이 명령은 ResourceGroup11의 ContosoProfile 프로필에서 Contoso라는 외부 엔드포인트를 얻습니다.
그런 다음 이 명령은 파이프라인 연산자를 사용하여 해당 엔드포인트를 **Enable-AzTrafficManagerEndpoint** cmdlet에 전달합니다.
이 cmdlet은 엔드포인트를 가능하게 합니다.

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
이 cmdlet에서 사용 가능하게 하는 Traffic Manager 엔드포인트의 이름을 지정합니다.

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
이 cmdlet에서 엔드포인트를 사용할 수 있는 Traffic Manager 프로필의 이름을 지정합니다.
프로필을 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용하세요.

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
이 cmdlet을 사용하면 이 매개 변수가 지정하는 그룹의 Traffic Manager 엔드포인트를 사용할 수 있습니다.

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
이 cmdlet에서 사용 가능하게 하는 Traffic Manager 엔드포인트를 지정합니다.
**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint cmdlet을 사용합니다.

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
Traffic Manager 프로필에서 이 cmdlet이 사용하지 않도록 설정하는 엔드포인트의 유형을 지정합니다.
유효한 값은 

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## 출력

### System.Boolean

## 참고 사항

## 관련 링크

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


