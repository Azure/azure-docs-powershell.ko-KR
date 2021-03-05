---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009675"
---
# Get-AzCostManagementExportExecutionHistory

## SYNOPSIS
정의된 범위 및 내보내기 이름에 대한 내보내기의 실행 기록을 얻습니다.

## 구문

### Get(기본값)
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 설명
정의된 범위 및 내보내기 이름에 대한 내보내기의 실행 기록을 얻습니다.

## 예제

### 예제 1: AzCostManagementExportExecutionHistory를 얻습니다.
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

ExportName 및 Scope에 의해 AzCostManagementExportExecutionHistory를 얻습니다.

### 예제 2: InputObject로 AzCostManagementExportExecutionHistory를 얻습니다.
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

InputObject로 AzCostManagementExportExecutionHistory를 얻습니다.

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

### -ExportName
이름 내보내기.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
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

### -Scope
이 매개 변수는 '구독', 'ResourceGroup' 및 'Service 제공'의 다양한 관점에서 비용 관리 범위를 정의합니다.

```yaml
Type: System.String
Parameter Sets: Get
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

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution

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

