---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180609"
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

이 명령은 함수 앱 계획을 이름으로 다운로드하고 삭제합니다.

### 예제 2: 이름으로 함수 앱 계획을 삭제합니다.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

이 명령은 함수 앱 계획을 이름으로 삭제합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
확인을 요청하지 않고 cmdlet이 함수 앱 계획을 제거합니다.

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

### System.Boolean

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

