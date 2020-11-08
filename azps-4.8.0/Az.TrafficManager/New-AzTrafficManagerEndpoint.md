---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056036"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Traffic Manager 프로필에서 끝점을 만듭니다.

## 구문과

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에서 끝점을 만듭니다.

이 cmdlet은 각 새 끝점을 Traffic Manager 서비스에 커밋합니다.
로컬 Traffic Manager 프로필 개체에 여러 끝점을 추가 하 고 한 번의 작업으로 변경 내용을 커밋하려면 Add-AzTrafficManagerEndpointConfig cmdlet을 사용 합니다.

## 예제의

### 예제 1: 프로필에 대 한 외부 끝점 만들기
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

이 명령은 ResourceGroup11 이라는 리소스 그룹의 ContosoProfile 이라는 프로필에 contoso 라는 외부 끝점을 만듭니다.

### 예제 2: 프로필에 대 한 Azure 끝점 만들기
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

이 명령은 리소스 그룹 ResourceGroup11의 ContosoProfile 라는 프로필에 contoso 라는 Azure 끝점을 만듭니다.
Azure endpoint는 Azure 리소스 관리자 ID가 *TargetResourceId* 의 URI 경로로 지정 된 Azure 웹 앱을 가리킵니다.
웹 앱 리소스가 위치를 제공 하기 때문에 명령이 *Endpointlocation* 매개 변수를 지정 하지 않습니다.

## 변수

### -CustomHeader
검색 요청에 대 한 사용자 지정 헤더 이름 및 값 쌍의 목록입니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EndpointLocation
성능 트래픽 라우팅 메서드에 사용할 끝점의 위치를 지정 합니다.
이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 형식의 끝점에만 적용할 수 있습니다.
성능 트래픽 라우팅 메서드를 사용 하는 경우이 매개 변수를 지정 해야 합니다.

Azure 지역 이름을 지정 합니다.
Azure 지역 전체 목록은 Azure 지역 http://azure.microsoft.com/regions/ (()을 참조 하세요 http://azure.microsoft.com/regions/) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointStatus
끝점의 상태를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 수 
- 비활성화 

상태를 사용 하는 경우 끝점은 끝점 상태를 조사 하 고 트래픽 라우팅 메서드에 포함 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoMapping
' 지역 ' 트래픽 라우팅 방법을 사용할 때이 끝점에 매핑되는 영역의 목록입니다. 허용 되는 값의 전체 목록은 Traffic Manager 설명서를 참조 하세요.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Azure 지역 이름을 지정 합니다.
Azure 지역 전체 목록은 Azure 지역 http://azure.microsoft.com/regions/ (()을 참조 하세요 http://azure.microsoft.com/regions/) .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 만드는 Traffic Manager 끝점의 이름을 지정 합니다.

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

### -우선 순위
트래픽 관리자가 끝점에 할당 하는 우선 순위를 지정 합니다.
이 매개 변수는 트래픽 관리자 프로필이 우선 순위의 트래픽 라우팅 메서드를 사용 하 여 구성 된 경우에만 사용 됩니다.
유효한 값은 1부터 1000 까지의 정수입니다.
값이 낮을수록 높은 우선 순위를 나타냅니다.

우선 순위를 지정 하는 경우 프로필의 모든 끝점에 대 한 우선 순위를 지정 해야 하며, 두 종점이 같은 우선 순위 값을 공유할 수 없습니다.
우선 순위를 지정 하지 않으면 트래픽 관리자가 끝점에 기본 우선 순위 값 (1)부터 끝점을 나열 하는 순서 대로 해당 프로필에 대 한 기본값을 지정 합니다.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -/Profile
이 cmdlet이 끝점을 추가 하는 Traffic Manager 프로필의 이름을 지정 합니다.
프로필을 얻으려면 New-AzTrafficManagerProfile 또는 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.

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

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 그룹에 트래픽 관리자 끝점을 만듭니다.

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

### -SubnetMapping
' Subnet ' 트래픽 라우팅 방법을 사용할 때이 끝점에 매핑된 주소 범위 또는 서브넷 목록입니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -대상
끝점의 정규화 된 DNS 이름을 지정 합니다.
트래픽 관리자는 트래픽을이 끝점으로 이동할 때 DNS 응답에이 값을 반환 합니다.
이 매개 변수는 ExternalEndpoints 끝점 형식에만 지정 합니다.
다른 끝점 형식의 경우 대신 *TargetResourceId* 매개 변수를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceId
대상의 리소스 ID를 지정 합니다.
AzureEndpoints 및 NestedEndpoints endpoint 형식에 대해서만이 매개 변수를 지정 합니다.
ExternalEndpoints 끝점 형식의 경우 *Target* 매개 변수를 대신 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -중량
트래픽 관리자가 끝점에 할당 하는 가중치를 지정 합니다.
유효한 값은 1부터 1000 까지의 정수입니다.
기본값은 1입니다.
이 매개 변수는 트래픽 관리자 프로필이 가중치가 있는 트래픽 라우팅 방법으로 구성 된 경우에만 사용 됩니다.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### TrafficManager. TrafficManagerEndpoint/.

## 상속자

## 관련 링크

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[새로운 AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[제거-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


