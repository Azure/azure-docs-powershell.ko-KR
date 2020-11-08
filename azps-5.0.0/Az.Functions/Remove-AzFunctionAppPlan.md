---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215417"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
함수 앱 계획을 삭제 합니다.

## 구문과

### ByName (기본값)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은
함수 앱 계획을 삭제 합니다.

## 예제의

### 예제 1: 이름으로 함수 앱 계획을 가져와 삭제 합니다.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

이 명령은 함수 앱 계획을 이름별로 가져와 삭제 합니다.

### 예제 2: 이름을 기준으로 함수 앱 계획을 삭제 합니다.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

이 명령은 함수 앱 계획을 이름으로 삭제 합니다.

## 변수

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

### -Force
확인 메시지 없이 cmdlet에서 함수 앱 계획을 제거 하도록 강제 합니다.

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
생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

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

### -이름
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
명령이 성공 하면 true를 반환 합니다.

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

### Api20190801. i p. PowerShell. IAppServicePlan

## 출력

### 시스템 부울

## 상속자

별칭과

복합 매개 변수 속성

아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: 리소스 위치입니다.
  - `[Kind <String>]`: 리소스 종류입니다.
  - `[Tag <IResourceTags>]`: 리소스 태그.
    - `[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[Capacity <Int32?>]`: 리소스에 할당 된 현재 인스턴스 수입니다.
  - `[FreeOfferExpirationTime <DateTime?>]`: 서버 팜 무료 제공이 만료 되는 시간입니다.
  - `[HostingEnvironmentProfileId <String>]`: 앱 서비스 환경의 리소스 ID입니다.
  - `[HyperV <Boolean?>]`: Hyper-v 컨테이너 app service 계획 <code>true</code> 인 경우에는 <code>false</code> 그렇지 않습니다.
  - `[IsSpot <Boolean?>]`: <code>true</code> 이 앱 서비스 계획에서 스폿 인스턴스를 소유 하는 경우
  - `[IsXenon <Boolean?>]`: 사용 하지 않음: Hyper-v 컨테이너 app service 계획 <code>true</code> 인 경우 <code>false</code>
  - `[MaximumElasticWorkerCount <Int32?>]`:이 ElasticScaleEnabled App Service 계획에 허용 되는 최대 총 작업자 수
  - `[PerSiteScaling <Boolean?>]`: <code>true</code> 이 앱 서비스 계획에 할당 된 앱을 독립적으로 확장할 수 있습니다.         <code>false</code>이 앱 서비스 계획에 할당 된 앱이 계획의 모든 인스턴스에 맞게 조정 됩니다.
  - `[Reserved <Boolean?>]`: Linux app service 계획 <code>true</code> 인 경우에는 <code>false</code> 그렇지 않습니다.
  - `[SkuCapability <ICapability[]>]`: SKU의 기능 (예:)은 traffic manager를 사용할 수 있나요?
    - `[Name <String>]`: SKU 기능의 이름입니다.
    - `[Reason <String>]`: SKU 기능에 대 한 설명입니다.
    - `[Value <String>]`: SKU 기능의 값입니다.
  - `[SkuCapacityDefault <Int32?>]`:이 App Service 계획 SKU에 대 한 기본 작업자 수입니다.
  - `[SkuCapacityMaximum <Int32?>]`:이 App Service 계획 SKU에 대 한 최대 작업자 수입니다.
  - `[SkuCapacityMinimum <Int32?>]`:이 App Service 계획 SKU의 최소 작업자 수입니다.
  - `[SkuCapacityScaleType <String>]`: 앱 서비스 계획에 사용할 수 있는 배율 구성입니다.
  - `[SkuFamily <String>]`: 리소스 SKU의 패밀리 코드입니다.
  - `[SkuLocation <String[]>]`: SKU의 위치입니다.
  - `[SkuName <String>]`: 리소스 SKU의 이름입니다.
  - `[SkuSize <String>]`: 리소스 SKU의 크기 지정자입니다.
  - `[SkuTier <String>]`: 리소스 SKU의 서비스 계층입니다.
  - `[SpotExpirationTime <DateTime?>]`: 서버 팜이 만료 되는 시간입니다. 스폿 서버 팜과만 유효 합니다.
  - `[TargetWorkerCount <Int32?>]`: 작업자 수의 크기를 조정 합니다.
  - `[TargetWorkerSizeId <Int32?>]`: 작업자 크기 ID를 조정 합니다.
  - `[WorkerTierName <String>]`: 앱 서비스 계획에 할당 된 대상 작업자 계층입니다.

## 관련 링크

