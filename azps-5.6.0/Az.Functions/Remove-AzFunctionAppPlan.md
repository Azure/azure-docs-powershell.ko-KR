---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994233"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
함수 앱 계획을 삭제합니다.

## 구문

### ByName(기본값)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
함수 앱 계획을 삭제합니다.

## 예제

### 예제 1: 이름에 따라 함수 앱 계획을 다운로드하고 삭제합니다.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

이 명령은 함수 앱 계획을 이름으로 얻게 하여 삭제합니다.

### 예제 2: 함수 앱 계획을 이름으로 삭제합니다.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

이 명령은 함수 앱 계획을 이름으로 삭제합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Force
확인을 요청하지 않고 cmdlet을 강제로 함수 앱 계획을 제거합니다.

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

### -InputObject
생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

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

### -Name
함수 앱의 이름입니다.

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

### -PassThru
명령이 성공하면 true를 반환합니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## 출력

### System.Boolean

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: 리소스 위치입니다.
  - `[Kind <String>]`: 리소스의 종류입니다.
  - `[Tag <IResourceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.
  - `[Capacity <Int32?>]`: 리소스에 할당된 현재 인스턴스 수입니다.
  - `[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제안이 만료되는 시간입니다.
  - `[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.
  - `[HyperV <Boolean?>]`: 컨테이너 Hyper-V 서비스 계획이 있는 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.
  - `[IsSpot <Boolean?>]`: <code>true</code> 이 App Service 계획은 스팟 인스턴스를 소유합니다.
  - `[IsXenon <Boolean?>]`: 사용되지 않습니다. 컨테이너 Hyper-V 서비스 계획이 있는 경우 그렇지 <code>true</code> <code>false</code> 않은 경우.
  - `[MaximumElasticWorkerCount <Int32?>]`: 이 ElasticScaleEnabled App Service 계획에 대해 허용되는 총 작업자의 최대 수
  - `[PerSiteScaling <Boolean?>]`: 이 App Service 계획에 할당된 앱을 독립적으로 <code>true</code> 확장할 수 있는 경우.         이 App Service 계획에 할당된 앱이 계획의 모든 인스턴스로 <code>false</code> 확장됩니다.
  - `[Reserved <Boolean?>]`: Linux 앱 서비스 계획인 경우 <code>true</code> 그렇지 <code>false</code> 않은 경우.
  - `[SkuCapability <ICapability[]>]`: SKU의 기능(예: Traffic Manager)을 사용하도록 설정되어 있나요?
    - `[Name <String>]`: SKU 기능의 이름입니다.
    - `[Reason <String>]`: SKU 기능의 이유입니다.
    - `[Value <String>]`: SKU 기능의 값입니다.
  - `[SkuCapacityDefault <Int32?>]`: 이 App Service 계획 SKU의 기본 작업자 수입니다.
  - `[SkuCapacityMaximum <Int32?>]`: 이 App Service 계획 SKU의 최대 작업자 수입니다.
  - `[SkuCapacityMinimum <Int32?>]`: 이 App Service 계획 SKU에 대한 최소 작업자 수입니다.
  - `[SkuCapacityScaleType <String>]`: App Service 계획에 사용할 수 있는 확장 구성입니다.
  - `[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.
  - `[SkuLocation <String[]>]`: SKU의 위치입니다.
  - `[SkuName <String>]`: 리소스 SKU의 이름입니다.
  - `[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.
  - `[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.
  - `[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료되는 시간입니다. 스폿 서버 팜인 경우만 유효합니다.
  - `[TargetWorkerCount <Int32?>]`: 작업자 수를 조정합니다.
  - `[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID 크기를 조정합니다.
  - `[WorkerTierName <String>]`: App Service 계획에 할당된 대상 작업자 계층입니다.

## 관련 링크

