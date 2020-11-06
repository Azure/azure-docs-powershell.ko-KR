---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 50ad29e9c28b42b1459d66358b8c6c37e2e0f4ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531792"
---
# Get-AzureRmTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 프로필에 대 한 끝점을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 필드인
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 오브젝트가
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에 대 한 끝점을 가져옵니다.

이 개체를 로컬로 수정한 다음 Set-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.
*Name* 및 *Type* 매개 변수를 사용 하 여 끝점을 지정 합니다.
*/Profile* 및 *ResourceGroupName* 매개 변수를 사용 하거나 **TrafficManagerProfile** 개체를 지정 하 여 Traffic Manager 프로필을 지정할 수 있습니다.
또는 파이프라인을 사용 하 여 해당 값을 전달할 수도 있습니다.

## 예제의

### 예제 1: 끝점 가져오기
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.

## 변수

### -이름
이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.

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
이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 그룹의 Traffic Manager 끝점을 가져옵니다.

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
이 cmdlet이 가져오는 트래픽 관리자 끝점을 지정 합니다.

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
이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.
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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManagerEndpoint
' TrafficManagerEndpoint ' 매개 변수는 파이프라인에서 ' TrafficManagerEndpoint ' 형식의 값을 허용 합니다.

## 출력

### TrafficManager. TrafficManagerEndpoint/.

## 상속자

## 관련 링크

[Disable-AzureRmTrafficManagerEndpoint](./Disable-AzureRmTrafficManagerEndpoint.md)

[Enable-AzureRmTrafficManagerEndpoint](./Enable-AzureRmTrafficManagerEndpoint.md)

[새로운 AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[제거-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)


