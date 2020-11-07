---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883018"
---
# Add-AzureRmRouteFilterRuleConfig

## SYNOPSIS
경로 필터에 경로 필터 규칙을 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Add-AzureRmRouteFilterRuleConfig cmdlet은 Azure 경로 필터에 경로 필터 규칙을 추가 합니다.

## 예제의

### --------------------------예제 1: 경로 필터에 경로 필터 규칙 추가--------------------------
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

첫 번째 명령은 Get-AzureRmRouteFilter cmdlet을 사용 하 여 routefilter01 이라는 경로 필터를 가져옵니다.
명령이 $RouteFilter 변수에 필터를 저장 합니다.

## 변수

### -Access
경로 필터 규칙의 액세스를 지정 하 고, 유효한 값은 거부 또는 허용입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommunityList
경로 필터가 필터링 할 커뮤니티 값 목록

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Force
리소스를 overrite 할 때 확인 메시지 표시 안 함

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
경로 필터에 추가할 경로 필터 규칙의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RouteFilter
이 cmdlet이 경로 필터 규칙을 추가 하는 경로 필터를 지정 합니다.

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RouteFilterRuleType
경로 필터 규칙 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 커뮤니티

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSRouteFilter
' RouteFilter ' 매개 변수는 파이프라인에서 ' PSRouteFilter ' 형식의 값을 허용 합니다.

## 출력

### PSRouteFilter에 대 한.

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹

## 관련 링크

[Get-AzureRmRouteFilterRuleConfig](./Get-AzureRmRouteFilterRuleConfig.md)

[Get-AzureRmRouteFilter](./Get-AzureRmRouteFilter.md)







[Set-AzureRmRouteFilter](./Set-AzureRmRouteFilter.md)

