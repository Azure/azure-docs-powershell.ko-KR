---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987266"
---
# Remove-AzTrafficManagerEndpointConfig

## SYNOPSIS
로컬 Traffic Manager 프로필 개체에서 엔드포인트를 제거합니다.

## 구문

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Remove-AzTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 엔드포인트를 제거합니다.
cmdlet을 사용하여 프로필을 Get-AzTrafficManagerProfile 수 있습니다.

이 cmdlet은 로컬 프로필 개체에서 작동합니다.
Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager 프로필에 변경 내용을 커밋합니다.
엔드포인트를 제거하고 단일 작업에서 변경 내용을 커밋하려면 Remove-AzTrafficManagerEndpoint cmdlet을 사용 합니다.

## 예제

### 예제 1: 엔드포인트 제거
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.
명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.

두 번째 명령은 에 저장된 프로필에서 contoso라는 Azure 엔드포인트를 $TrafficManagerProfile.
이 명령은 로컬 개체만 변경합니다.

최종 명령은 ContosoProfile이라는 Traffic Manager 프로필을 업데이트하여 로컬 값과 $TrafficManagerProfile.

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

### -EndpointName
이 cmdlet이 제거하는 Traffic Manager 엔드포인트의 이름을 지정합니다.

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
**TrafficManagerProfile** 개체를 얻은 경우 Get-AzTrafficManagerProfile cmdlet을 사용합니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## 출력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## 참고 사항

## 관련 링크

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


