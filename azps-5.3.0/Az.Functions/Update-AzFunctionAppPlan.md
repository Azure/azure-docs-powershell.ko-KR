---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492972"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
함수 앱 서비스 계획을 업데이트합니다.

## 구문

### ByName(기본값)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
함수 앱 서비스 계획을 업데이트합니다.

## 예제

### 예제 1: 최대 작업자 20명으로 App Service 계획을 EP2 sku로 업데이트합니다.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

이 명령은 최대 20개 작업자를 사용하여 App Service 계획을 EP2 sku로 업데이트합니다.

## PARAMETERS

### -AsJob
명령을 작업으로 실행합니다.

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

### -InputObject
생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
App Service 계획에 대한 최대 작업자 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
App Service 계획에 대한 최소 작업자 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
App Service 계획의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
명령을 비동기적으로 실행합니다.

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
리소스가 속한 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
계획 SKU입니다.
유효한 입력은 EP1, EP2, EP3입니다.

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

### -SubscriptionId
Azure 구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
리소스 태그.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <IAppServicePlan> 
  - `Location <String>`: 리소스 위치입니다.
  - `[Kind <String>]`: 리소스의 종류입니다.
  - `[Tag <IResourceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[Capacity <Int32?>]`: 리소스에 할당된 현재 인스턴스 수입니다.
  - `[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제안이 만료되는 시간입니다.
  - `[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.
  - `[HyperV <Boolean?>]`: Hyper-V 컨테이너 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.
  - `[IsSpot <Boolean?>]`: 이 <code>true</code> App Service 계획은 스폿 인스턴스를 소유합니다.
  - `[IsXenon <Boolean?>]`: 사용되지 않습니다. Hyper-V 컨테이너 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.
  - `[MaximumElasticWorkerCount <Int32?>]`: 이 ElasticScaleEnabled App Service 계획에 허용되는 최대 총 작업자 수
  - `[PerSiteScaling <Boolean?>]`: 이 App Service 계획에 <code>true</code> 할당된 앱은 독립적으로 확장할 수 있습니다.         이 App Service 계획에 할당된 앱은 계획의 모든 <code>false</code> 인스턴스로 확장됩니다.
  - `[Reserved <Boolean?>]`: Linux 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.
  - `[SkuCapability <ICapability[]>]`: SKU의 기능(예: Traffic Manager를 사용하도록 설정되어 있나요?
    - `[Name <String>]`: SKU 기능의 이름입니다.
    - `[Reason <String>]`: SKU 기능의 이유입니다.
    - `[Value <String>]`: SKU 기능의 값입니다.
  - `[SkuCapacityDefault <Int32?>]`: 이 App Service 계획 SKU에 대한 기본 작업자 수입니다.
  - `[SkuCapacityMaximum <Int32?>]`: 이 App Service 계획 SKU에 대한 최대 작업자 수입니다.
  - `[SkuCapacityMinimum <Int32?>]`: 이 App Service 계획 SKU에 대한 최소 작업자 수입니다.
  - `[SkuCapacityScaleType <String>]`: App Service 계획에 사용 가능한 크기 조정 구성입니다.
  - `[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.
  - `[SkuLocation <String[]>]`: SKU의 위치입니다.
  - `[SkuName <String>]`: 리소스 SKU의 이름입니다.
  - `[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.
  - `[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.
  - `[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료되는 시간입니다. 스폿 서버 팜인 경우만 유효합니다.
  - `[TargetWorkerCount <Int32?>]`: 작업자 수를 조정합니다.
  - `[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID 크기 조정
  - `[WorkerTierName <String>]`: App Service 계획에 할당된 대상 작업 계층입니다.

## 관련 링크

