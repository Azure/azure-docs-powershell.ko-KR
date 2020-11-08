---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214600"
---
# New-AzCustomProvider

## SYNOPSIS
사용자 지정 리소스 공급자를 만들거나 업데이트 합니다.

## 구문과

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은
사용자 지정 리소스 공급자를 만들거나 업데이트 합니다.

## 예제의

### 예제 1: 사용자 지정 공급자 만들기
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

사용자 지정 리소스 공급자 만들기

### 예제 2: 연결을 사용 하 여 사용자 지정 공급자 만들기
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

사용자 지정 공급자 연결에 대 한 경로를 사용 하 여 사용자 지정 공급자를 만듭니다.

## 변수

### -작업
사용자 지정 리소스 공급자가 구현 하는 작업 목록입니다.
생성 하려면 작업 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
작업으로 명령 실행

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
리소스 위치

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

### -이름
리소스 공급자의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
비동기적으로 명령 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

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

### -ResourceType
사용자 지정 리소스 공급자가 구현 하는 리소스 종류 목록입니다.
생성 하려면 RESOURCETYPE 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 구독 ID입니다.
GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
리소스 태그

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -유효성 검사
사용자 지정 리소스 공급자의 요청에 대해 실행할 유효성 검사 목록입니다.
생성 하려면 유효성 검사 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

## 출력

### Api20180901Preview. ICustomRpManifest에 대 한 Microsoft.

## 상속자

별칭과

복합 매개 변수 속성

아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.


ACTION <ICustomRpActionRouteDefinition [] >: 사용자 지정 리소스 공급자가 구현 하는 작업 목록입니다.
  - `Endpoint <String>`: 사용자 지정 리소스 공급자가 요청을 프록시 하는 경로 정의 끝점 URI입니다. 이는 플랫 URI (예: ' https://testendpoint/ ') 형식 이거나 경로를 통해 라우팅하도록 지정할 수 있습니다 (예: ' https://testendpoint/{requestPath} ').
  - `Name <String>`: 경로 정의의 이름입니다. ARM 확장의 이름이 됩니다 (예: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ').
  - `[RoutingType <ActionRouting?>]`: 작업 요청에 대해 지원 되는 라우팅 유형입니다.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: 사용자 지정 리소스 공급자가 구현 하는 리소스 종류 목록입니다.
  - `Endpoint <String>`: 사용자 지정 리소스 공급자가 요청을 프록시 하는 경로 정의 끝점 URI입니다. 이는 플랫 URI (예: ' https://testendpoint/ ') 형식 이거나 경로를 통해 라우팅하도록 지정할 수 있습니다 (예: ' https://testendpoint/{requestPath} ').
  - `Name <String>`: 경로 정의의 이름입니다. ARM 확장의 이름이 됩니다 (예: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ').
  - `[RoutingType <ResourceTypeRouting?>]`: 리소스 요청에 대해 지원 되는 라우팅 유형입니다.

유효성 검사 <ICustomRpValidations [] >: 사용자 지정 리소스 공급자의 요청에 대해 실행할 유효성 검사 목록입니다.
  - `Specification <String>`: 유효성 검사 사양에 대 한 링크입니다. Raw.githubusercontent.com에서 사양을 호스트 해야 합니다.
  - `[ValidationType <ValidationType?>]`: 일치 하는 요청에 대해 실행할 유효성 검사의 유형입니다.

## 관련 링크

