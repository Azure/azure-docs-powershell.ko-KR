---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522816"
---
# AzureRM 모듈
## 설명은
이 항목에서는 Azure Insights Cmdlet에 대 한 도움말 항목을 표시 합니다.

## AzureRM Cmdlet
### [추가-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
자동 크기 조정 설정을 만듭니다.

### [추가-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
로그 알림 규칙을 추가 하거나 바꿉니다.

### [추가-AzureRmLogProfile](Add-AzureRmLogProfile.md)
새 활동 로그 프로필을 만듭니다. 이 프로필을 사용 하 여 활동 로그를 Azure storage 계정에 보관 하거나 같은 구독의 Azure 이벤트 허브에 스트리밍할 수 있습니다. 

- **저장소 계정** -표준 저장소 계정 (premium 저장소 계정 (지원 되지 않음)이 지원 되지 않음). ARM 또는 클래식 형식이 될 수 있습니다. 저장소 계정에 기록 된 경우 활동 로그를 저장 하는 비용은 표준 저장소 요금으로 청구 됩니다. 구독 당 하나의 로그 프로필만 있을 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 저장소 계정만 사용할 수 있습니다. 

- **이벤트 허브** -구독 당 하나의 로그 프로필만 사용할 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 이벤트 허브가 있을 수 있습니다. 활동 로그가 이벤트 허브로 스트리밍되는 경우 표준 이벤트 허브 가격이 적용 됩니다. 

활동 로그에서 이벤트는 지역과 관련이 있거나 "전역" 일 수 있습니다. 전역 본질적으로 이러한 이벤트는 영역 agnostics 지역에 관계 없이 대부분의 이벤트가이 범주에 속합니다. 활동 로그 프로필이 포털에서 설정 된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "Global"이 암시적으로 추가 됩니다. Cmdlet을 사용 하는 경우에는 "전역"으로 위치를 명시적으로 다른 지역과 별도로 언급 해야 합니다. 

**참고** : **위치에 "Global"을 설정 하지 않으면 대부분의 활동 로그가 내보내지지 않습니다.** 

### [추가-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
메트릭 기반 알림 규칙을 추가 하거나 업데이트 합니다.

### [추가-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Webtest 경고 규칙을 추가 하거나 업데이트 합니다.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
활동 로그 알림을 비활성화 하 고 해당 태그를 설정 합니다.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
활동 로그 알림을 사용 하 고 해당 태그를 설정 합니다.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
작업 그룹을 가져옵니다.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
하나 이상의 활동 로그 알림 리소스를 가져옵니다.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
알림 기록을 가져옵니다.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
알림 규칙을 가져옵니다.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
자동 크기 조정 기록을 가져옵니다.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
자동 크기 조정 설정을 가져옵니다.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
기록 된 범주와 시간 grains를 가져옵니다.

### [Get-AzureRmLog](Get-AzureRmLog.md)
이벤트의 로그를 가져옵니다.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
로그 프로필을 가져옵니다.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
리소스의 메트릭 값을 가져옵니다.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
메트릭 정의를 가져옵니다.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
리소스에 대 한 사용 메트릭을 가져옵니다.

### [새로운 AzureRmActionGroup](New-AzureRmActionGroup.md)
메모리에 ActionGroup reference 개체를 만듭니다.

### [새로운 AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
새 작업 그룹 수신기를 만듭니다.

### [새로운 AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
메모리에 새 활동 로그 알림 조건 개체를 만듭니다.

### [새로운 AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
경고 규칙에 대 한 전자 메일 작업을 만듭니다.

### [새로운 AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
알림 규칙 webhook을 만듭니다.

### [새로운 AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
자동 크기 조정 전자 메일 알림을 만듭니다.

### [새로운 AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
자동 크기 조정 프로필을 만듭니다.

### [새로운 AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
자동 크기 조정 규칙을 만듭니다.

### [새로운 AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
자동 크기 조정 webhook을 만듭니다.

### [제거-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
작업 그룹을 제거 합니다.

### [제거-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
활동 로그 알림을 제거 합니다.

### [제거-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
알림 규칙을 제거 합니다.

### [제거-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
자동 크기 조정 설정을 제거 합니다.

### [제거-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
로그 프로필을 제거 합니다.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
새를 만들거나 기존 작업 그룹을 업데이트 합니다.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
기존 활동 로그 알림을 새로 만들거나 설정 합니다.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
리소스에 대 한 로그 및 메트릭 설정을 설정 합니다.

