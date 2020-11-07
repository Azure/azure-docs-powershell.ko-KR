---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 0ccbabbb863b99aefd19b8f8a53257ac8c46faaa
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93883270"
---
# New-AzResource

## SYNOPSIS
리소스를 만듭니다.

## 구문과

### ByResourceId (기본값)
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BySubscriptionLevel
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTenantLevel
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzResource** cmdlet은 리소스 그룹에 웹 사이트, Azure sql 데이터베이스 서버 또는 Azure sql 데이터베이스 등의 azure 리소스를 만듭니다.

## 예제의

### 예제 1: 리소스 만들기
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.

### 예제 2: splatting를 사용 하 여 리소스 만들기
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.

## 변수

### -ApiVersion
사용할 리소스 공급자 API의 버전을 지정 합니다. 버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.

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

### -AsJob
백그라운드에서 cmdlet 실행

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -ExtensionResourceName
리소스에 대 한 확장 리소스의 이름을 지정 합니다. 예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionResourceType
확장 리소스의 리소스 종류를 지정 합니다.
예를 들어 확장 리소스가 데이터베이스인 경우 다음 형식을 지정 합니다. `Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -IsFullObject
*속성* 매개 변수에서 지정 하는 개체가 전체 개체 임을 나타냅니다.

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

### -종류
자원의 자원 종류를 지정 합니다.

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

### -위치
리소스의 위치를 지정 합니다.
중앙 미국 또는 동남 아시아 등의 데이터 센터 위치를 지정 합니다.
해당 형식의 리소스를 지 원하는 위치에 리소스를 배치할 수 있습니다. 리소스 그룹에는 다른 위치의 리소스가 포함 될 수 있습니다. 각 리소스 형식을 지 원하는 위치를 확인 하려면 Get-AzLocation cmdlet을 사용 합니다.

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

### -ODataQuery
OData (Open Data Protocol) 스타일 필터를 지정 합니다. 이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.

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

### -계획
자원 계획 속성을 나타내는 해시 테이블입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.

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

### -속성
리소스에 대 한 리소스 속성을 지정 합니다. 이 매개 변수를 사용 하 여 리소스 형식에 해당 하는 속성 값을 지정 합니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 리소스를 만드는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
구독을 포함 하 여 정규화 된 리소스 ID를 다음 예제와 같이 지정 합니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context.resourcename
리소스의 이름을 지정 합니다. 예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
리소스의 종류를 지정 합니다.
예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
Sku 속성을 나타내는 해시 테이블입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantLevel
이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System.webserver. 컬렉션 테이블

### System. 문자열

## 출력

### System.webserver. 자동. PSObject

## 상속자

## 관련 링크

[Get-AzResource](./Get-AzResource.md)

[이동-AzResource](./Move-AzResource.md)

[제거-AzResource](./Remove-AzResource.md)

[Set-AzResource](./Set-AzResource.md)
