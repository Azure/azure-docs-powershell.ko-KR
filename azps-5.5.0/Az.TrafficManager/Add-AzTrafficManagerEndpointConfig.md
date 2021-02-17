---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207517"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
로컬 Traffic Manager 프로필 개체에 엔드포인트를 추가합니다.

## 구문

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 엔드포인트를 추가합니다.
New-AzTrafficManagerProfile cmdlet을 사용하여 프로필을 Get-AzTrafficManagerProfile 있습니다.

이 cmdlet은 로컬 프로필 개체에서 작동됩니다.
Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager에 대한 프로필에 변경 내용을 커밋합니다.
엔드포인트를 만들고 단일 작업에서 변경을 커밋하기 위해 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.

## 예제

### 예제 1: 프로필에 엔드포인트 추가
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.
이 명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.

두 번째 명령은 contoso라는 엔드포인트를 $TrafficManagerProfile.
이 명령은 엔드포인트에 대한 구성 데이터를 포함합니다.
이 명령은 로컬 개체만 변경합니다.

마지막 명령은 Azure의 Traffic Manager 프로필을 업데이트하여 Azure의 로컬 값과 $TrafficManagerProfile.

## PARAMETERS

### -CustomHeader
프로브 요청에 대한 사용자 지정 헤더 이름 및 값 쌍 목록입니다.

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

### -EndpointLocation
성능 트래픽 라우팅 메서드에 사용할 엔드포인트의 위치를 지정합니다.
이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 유형의 엔드포인트에만 적용할 수 있습니다.
성능 트래픽 라우팅 메서드를 사용할 때 이 매개 변수를 지정해야 합니다.

Azure 지역 이름을 지정합니다.
Azure 지역 전체 목록은 Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) 지역(.

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
이 cmdlet이 추가하는 Traffic Manager 엔드포인트의 이름을 지정합니다.

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
엔드포인트의 상태를 지정합니다.
유효한 값은 

- 사용 
- 사용 안 

상태가 사용되면 엔드포인트가 엔드포인트 상태에 대해 프로브되어 트래픽 라우팅 메서드에 포함됩니다.

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
'지리적' 트래픽 라우팅 방법을 사용하는 경우 이 엔드포인트에 매핑된 지역 목록입니다. 허용되는 값의 전체 목록은 Traffic Manager [설명서를 참조하세요.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)

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
부모 프로필의 중첩 엔드포인트를 사용할 수 있는 것으로 간주하려면 자식 프로필에서 사용할 수 있어야 하는 최소 엔드포인트 수입니다.
'NestedEndpoints' 형식의 엔드포인트에만 적용할 수 있습니다.

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

### -Priority
Traffic Manager가 엔드포인트에 할당하는 우선 순위를 지정합니다.
이 매개 변수는 Traffic Manager 프로필이 우선 순위 트래픽 라우팅 메서드로 구성된 경우만 사용됩니다.
유효한 값은 1에서 1000까지의 정수입니다.
낮은 값은 높은 우선 순위를 나타냅니다.

우선 순위를 지정하는 경우 프로필의 모든 엔드포인트에 우선 순위를 지정해야 합니다. 두 엔드포인트가 동일한 우선 순위 값을 공유할 수 없습니다.
우선 순위를 지정하지 않으면 Traffic Manager는 엔드포인트에 기본 우선 순위 값을 할당합니다( 1부터 시작하여 프로필이 엔드포인트를 나열하는 순서대로).

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
'서브넷' 트래픽 라우팅 방법을 사용할 때 이 엔드포인트에 매핑된 주소 범위 또는 서브넷 목록입니다.

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

### -Target
엔드포인트의 정식 DNS 이름을 지정합니다.
Traffic Manager는 트래픽을 이 엔드포인트로 지시할 때 DNS 응답에서 이 값을 반환합니다.
ExternalEndpoints 엔드포인트 형식에만 이 매개 변수를 지정합니다.
다른 엔드포인트 형식의 경우 *TargetResourceId* 매개 변수를 대신 지정합니다.

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
대상의 리소스 ID를 지정합니다.
AzureEndpoints 및 NestedEndpoints 엔드포인트 유형에만 이 매개 변수를 지정합니다.
ExternalEndpoints 엔드포인트 형식의 경우 대상 매개 *변수를 대신* 지정합니다.

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
로컬 **TrafficManagerProfile** 개체를 지정합니다.
이 cmdlet은 이 로컬 개체를 수정합니다.
**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.

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
이 cmdlet이 Azure Traffic Manager 프로필에 추가하는 엔드포인트의 유형을 지정합니다.
유효한 값은 

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

### -Weight
Traffic Manager가 엔드포인트에 할당하는 가중치를 지정합니다.
유효한 값은 1에서 1000까지의 정수입니다.
기본값은 1(1)입니다.
이 매개 변수는 Traffic Manager 프로필이 가중 트래픽 라우팅 방법으로 구성된 경우만 사용됩니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## 출력

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## 참고 사항

## 관련 링크

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


