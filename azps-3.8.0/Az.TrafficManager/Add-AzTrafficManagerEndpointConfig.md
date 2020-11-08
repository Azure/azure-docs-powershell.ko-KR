---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041652"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
로컬 트래픽 관리자 프로필 개체에 끝점을 추가 합니다.

## 구문과

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Add-AzTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 끝점을 추가 합니다.
New-AzTrafficManagerProfile 또는 Get-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.

이 cmdlet은 로컬 프로필 개체에서 작동 합니다.
Set-AzTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.
끝점을 만들고 단일 작업으로 변경 내용을 커밋하려면 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.

## 예제의

### 예제 1: 프로필에 끝점 추가
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

첫 번째 명령은 **AzTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.
명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.

두 번째 명령은 contoso 이라는 이름의 끝점을 $TrafficManagerProfile에 저장 된 프로필에 추가 합니다.
명령에 끝점에 대 한 구성 데이터가 포함 됩니다.
이 명령은 로컬 개체만 변경 합니다.

마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Azure의 Traffic Manager 프로필을 업데이트 합니다.

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

### -EndpointName
이 cmdlet이 추가 하는 Traffic Manager 끝점의 이름을 지정 합니다.

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
' 지역 ' 트래픽 라우팅 방법을 사용할 때이 끝점에 매핑되는 영역의 목록입니다. 허용 되는 [값의 전체 목록은](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Traffic Manager 설명서를 참조 하세요.

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
부모 프로필에서 중첩 된 끝점을 사용할 수 있는 것으로 간주 하기 위해 하위 프로필에서 사용할 수 있어야 하는 끝점의 최소 수입니다.
' NestedEndpoints ' 형식의 끝점에만 적용 됩니다.

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

### -TrafficManagerProfile
로컬 **TrafficManagerProfile** 개체를 지정 합니다.
이 cmdlet은이 로컬 개체를 수정 합니다.
**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.

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

### -Type
이 cmdlet이 Azure Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.
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

### TrafficManager. TrafficManagerProfile/.

## 출력

### TrafficManager. TrafficManagerProfile/.

## 상속자

## 관련 링크

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[새로운 AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[제거-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


