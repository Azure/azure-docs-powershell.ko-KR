---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056038"
---
# Enable-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 프로필에서 끝점을 사용 하도록 설정 합니다.

## 구문과

### 필드인
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 오브젝트가
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
AzTrafficManagerEndpoint cmdlet을 **사용** 하면 Azure Traffic Manager 프로필에서 끝점을 사용할 수 있습니다.

파이프라인 연산자를 사용 하 여이 cmdlet에 **TrafficManagerEndpoint** 개체를 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 지정할 수 있습니다.

또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.

## 예제의

### 예제 1: 프로필에서 끝점 사용
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

이 명령을 사용 하 여 리소스 그룹 ResourceGroup11의 ContosoProfile 이라는 프로필에 contoso 라는 외부 끝점을 설정 합니다.

### 예제 2: 파이프라인을 사용 하 여 끝점 활성화
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

이 명령은 ResourceGroup11의 ContosoProfile 이라는 프로필에서 Contoso 라는 외부 끝점을 가져옵니다.
그런 다음 파이프라인 연산자를 사용 하 여 해당 끝점을 **Enable-AzTrafficManagerEndpoint** cmdlet에 전달 합니다.
해당 cmdlet은 해당 끝점을 사용할 수 있도록 합니다.

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
이 cmdlet이 사용할 수 있는 Traffic Manager 끝점의 이름을 지정 합니다.

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

### -/Profile
이 cmdlet이 끝점을 사용할 수 있도록 하는 Traffic Manager 프로필의 이름을 지정 합니다.
프로필을 얻으려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 끝점을 사용 하도록 설정 합니다.

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
이 cmdlet이 사용할 수 있는 트래픽 관리자 끝점을 지정 합니다.
**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint cmdlet을 사용 합니다.

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
이 cmdlet이 Traffic Manager 프로필에서 사용 하지 않도록 설정 하는 끝점 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManager. TrafficManagerEndpoint/.

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[새로운 AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[새로운 AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[제거-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


