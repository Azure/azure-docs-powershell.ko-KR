---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533539"
---
# Set-AzureRmTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필을 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 업데이트 합니다.
이 cmdlet은 로컬 프로필 개체의 프로필 설정을 업데이트 합니다.
*TrafficManagerProfile* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 프로필 개체를 지정할 수 있습니다.

Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 나타내는 로컬 개체를 얻을 수 있습니다.
개체를 로컬로 수정한 다음 **Set-AzureRmTrafficManagerProfile** 를 사용 하 여 변경 내용을 커밋합니다.

## 예제의

### 예제 1: 프로필 업데이트
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

첫 번째 명령은 Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.
명령이 $TrafficManagerProfile 변수에 로컬로 프로필을 저장 합니다.

두 번째 명령은 해당 프로필을 로컬로 변경 합니다.
이 명령은 프로필을 사용 하지 않도록 설정 합니다.

세 번째 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 ContosoProfile 이라는 Traffic Manager 프로필을 업데이트 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
로컬 **TrafficManagerProfile** 개체를 지정 합니다.
이 cmdlet은이 로컬 개체와 일치 하도록 Traffic Manager를 업데이트 합니다.

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManagerProfile (Network.)
이 cmdlet은 **TrafficManagerProfile** 개체를 허용 합니다.

## 출력

### TrafficManagerProfile (Network.)
이 cmdlet은 **TrafficManagerProfile** 개체를 반환 합니다.

## 상속자

## 관련 링크

[추가-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[새로운 AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[제거-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[제거-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)


