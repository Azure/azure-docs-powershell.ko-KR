---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214670"
---
# Enable-AzTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필을 사용 하도록 설정 합니다.

## 구문과

### 필드인
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 오브젝트가
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
AzTrafficManagerProfile cmdlet을 **사용** 하면 Azure Traffic Manager 프로필을 사용할 수 있습니다.
파이프라인 또는 매개 변수 값을 사용 하 여 프로필 개체를 지정할 수 있습니다.
또는 *Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 프로필을 지정할 수도 있습니다.

## 예제의

### 예제 1: 이름으로 지정 된 프로필 사용
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 사용 하도록 설정 합니다.

### 예제 2: 파이프라인을 사용 하 여 프로필 설정
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.
그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzTrafficManagerProfile** cmdlet에 전달 합니다.
해당 cmdlet은 해당 프로필을 사용 하도록 설정 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
이 cmdlet이 사용할 수 있는 Traffic Manager 프로필의 이름을 지정 합니다.

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
리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 사용 하도록 설정 합니다.

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

### -TrafficManagerProfile
사용할 **TrafficManagerProfile** 개체를 지정 합니다.
**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManager. TrafficManagerProfile/.

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[Disable-AzTrafficManagerProfile](./Disable-AzTrafficManagerProfile.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[새로운 AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[제거-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


