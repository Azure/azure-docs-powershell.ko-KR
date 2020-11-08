---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213735"
---
# New-AzAppConfigurationStore

## SYNOPSIS
지정 된 매개 변수를 사용 하 여 구성 저장소를 만듭니다.

## 구문과

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## 설명은
지정 된 매개 변수를 사용 하 여 구성 저장소를 만듭니다.

## 예제의

### 예제 1: 앱 구성 저장소 만들기
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

이 명령은 앱 구성 저장소를 만듭니다.

### 예제 2: IdentityType이 "UserAssigned"으로 설정 된 앱 구성 만들기
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

이 명령은 앱 구성을 만들고 사용자가 할당 한 관리 되는 id를 할당 합니다.
`Update-AzAppConfigurationStore`Nk (cusomer 관리 되는 키)을 사용 하도록 설정 하려면 다음 단계에 대 한 예제를 참조 하세요.

### 예제 3: IdentityType이 "지정 된 SystemAssigned"으로 설정 된 앱 구성 만들기 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

이 명령은 앱 구성을 만들고 리소스와 연결 된 시스템 할당 관리 id를 사용 하도록 설정 합니다.
`Update-AzAppConfigurationStore`Nk (cusomer 관리 되는 키)을 사용 하도록 설정 하려면 다음 단계에 대 한 예제를 참조 하세요.

### 예제 4: IdentityType이 "SystemAssigned, UserAssigned 됨"으로 설정 된 앱 구성 만들기
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

시스템 할당 관리 id를 사용 하도록 설정 하 고 동시에 사용자에 게 할당 된 id를 제공할 수 있습니다.
`Update-AzAppConfigurationStore`Nk (cusomer 관리 되는 키)을 사용 하도록 설정 하려면 다음 단계에 대 한 예제를 참조 하세요.

## 변수

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

### -IdentityType
사용 되는 관리 되는 id의 유형입니다.
' SystemAssignedAndUserAssigned ' 형식에는 암시적으로 만들어진 id와 사용자 지정 id 집합이 모두 포함 됩니다.
' 없음 ' 형식은 id를 모두 제거 합니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
리소스의 위치입니다.
리소스를 만든 후에는 변경할 수 없습니다.

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
구성 저장소의 이름입니다.

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
컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.

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

### -Sku
구성 저장소의 SKU 이름입니다.

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

### -SubscriptionId
Microsoft Azure 구독 ID입니다.

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
리소스의 태그입니다.

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

### -UserAssignedIdentity
리소스와 연결 된 사용자 할당 id의 목록입니다.
사용자 할당 id 사전 키는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식의 리소스 id를 사용 합니다.

```yaml
Type: System.String[]
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

### Api20200601. IConfigurationStore에 대 한 Microsoft.

## 상속자

별칭과

## 관련 링크



[새로운 AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

