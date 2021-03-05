---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996814"
---
# Get-AzCostManagementExport

## SYNOPSIS
내보내기 이름으로 정의된 범위에 대한 내보내기 를 얻습니다.

## 구문

### 목록(기본값)
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### 가져오기
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명
내보내기 이름으로 정의된 범위에 대한 내보내기 를 얻습니다.

## 예제

### 예제 1: 범위에 의해 모든 AzCostManagementExports를 얻습니다.
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

범위에 의해 모든 AzCostManagementExports를 얻습니다.

### 예제 2: 이름 및 범위로 AzCostManagementExport를 얻다
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

이름 및 범위로 AzCostManagementExport를 얻다

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

### -확장
내보내기 내에서 속성을 확장하는 데 사용할 수 있습니다.
현재 'runHistory'만 지원하며 내보내기의 마지막 10개 실행에 대한 정보를 반환합니다.

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

### -InputObject
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
이름 내보내기.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


INPUTOBJECT <ICostManagementIdentity> : ID 매개 변수
  - `[AlertId <String>]`: 경고 ID
  - `[ExportName <String>]`: 이름 내보내기.
  - `[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}' 또는 차원/쿼리 작업과 함께 사용되는 통합 계정에 대해 '{externalBillingAccountId}'일 수 있습니다.
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다. 여기에는 연결된 계정에 대한 'externalSubscriptions', 통합 계정에 대한 'externalBillingAccounts'가 포함됩니다.
  - `[Id <String>]`: 리소스 ID 경로
  - `[Scope <String>]`: 보기 작업과 연결된 범위입니다. 여기에는 구독 범위에 대한 'subscriptions/{subscriptionId}', ResourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}', 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위의 'providers/Microsoft.Billing/billingAccountId}/billingProfiles/{billingProfileId}' BillingProfile scope, 'providers/Microsoft.BillingAccountId}/InvoiceSections/{InvoiceSections/{InvoiceSectionId}'.Management/managementGroups/{managementGroupId}' for Management Group 범위, 'providers/Microsoft.CostManagement/externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptionName}'
  - `[ViewName <String>]`: 이름 보기

## 관련 링크

