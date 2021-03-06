---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987210"
---
# Set-AzTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필을 업데이트합니다.

## 구문

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 업데이트합니다.
이 cmdlet은 로컬 프로필 개체에서 프로필의 설정을 업데이트합니다.
*TrafficManagerProfile* 매개 변수를 사용하거나 파이프라인을 사용하여 프로필 개체를 지정할 수 있습니다.

cmdlet을 사용하여 프로필을 나타내는 로컬 개체를 Get-AzTrafficManagerProfile 수 있습니다.
개체를 로컬로 수정한 다음 **Set-AzTrafficManagerProfile을** 사용하여 변경 내용을 커밋합니다.

## 예제

### 예제 1: 프로필 업데이트
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

첫 번째 명령은 Get-AzTrafficManagerProfile cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.
명령은 프로필을 로컬로 $TrafficManagerProfile 변수에 저장합니다.

두 번째 명령은 로컬로 프로필을 변경합니다.
이 명령은 프로필을 사용하지 않도록 설정합니다.

세 번째 명령은 ContosoProfile이라는 Traffic Manager 프로필을 업데이트하여 로컬 값과 $TrafficManagerProfile.

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

### -TrafficManagerProfile
로컬 **TrafficManagerProfile** 개체를 지정합니다.
이 cmdlet은 Traffic Manager를 업데이트하여 이 로컬 개체와 일치합니다.

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

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


