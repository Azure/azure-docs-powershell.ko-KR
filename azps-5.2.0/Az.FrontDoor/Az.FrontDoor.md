---
Module Name: Az.FrontDoor
Module Guid: 91832aaa-dc11-4583-8239-adb7df531604
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
ms.openlocfilehash: 5039a5684dfc24a05f2d79e49397b8d064bc6a3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344906"
---
# Az.FrontDoor 모듈
## 설명
이 섹션의 항목에서는 Azure Resource Manager(ARM) 프레임워크의 Azure Front Door Service에 대한 Azure PowerShell cmdlet을 문서화합니다. cmdlet은 Microsoft.Azure.Commands.FrontDoor 네임스페이스에 있습니다.

## Az.FrontDoor Cmdlet
### [Disable-AzFrontDoorCustomDomainHttps](Disable-AzFrontDoorCustomDomainHttps.md)
사용자 지정 도메인에 대해 HTTPS를 사용하지 않도록 설정

### [Enable-AzFrontDoorCustomDomainHttps](Enable-AzFrontDoorCustomDomainHttps.md)
Front Door 관리 인증서를 사용하여 사용자 지정 도메인에 HTTPS를 사용하도록 설정하거나 Azure Key Vault에서 자체 인증서를 사용할 수 있습니다.

### [Get-AzFrontDoor](Get-AzFrontDoor.md)
Front Door 부하 균형 조정기

### [Get-AzFrontDoorFrontendEndpoint](Get-AzFrontDoorFrontendEndpoint.md)
프런트 도어 프런트 엔드 엔드포인트를 얻습니다.

### [Get-AzFrontDoorRulesEngine](Get-AzFrontDoorRulesEngine.md)
규칙 엔진 구성을 얻습니다.

### [Get-AzFrontDoorWafManagedRuleSetDefinition](Get-AzFrontDoorWafManagedRuleSetDefinition.md)
WAF 관리 규칙 집합 정의를 얻습니다.

### [Get-AzFrontDoorWafPolicy](Get-AzFrontDoorWafPolicy.md)
WAF 정책 얻기

### [New-AzFrontDoor](New-AzFrontDoor.md)
새 Azure Front Door 부하 균형 조정기 만들기

### [New-AzFrontDoorBackendObject](New-AzFrontDoorBackendObject.md)
PSBackend 개체 만들기

### [New-AzFrontDoorBackendPoolObject](New-AzFrontDoorBackendPoolObject.md)
Front Door 만들기를 위한 PSBackendPool 개체 만들기

### [New-AzFrontDoorBackendPoolsSettingObject](New-AzFrontDoorBackendPoolsSettingObject.md)
Front Door를 만들기 위한 PSBackendPoolsSetting 개체를 만듭니다.

### [New-AzFrontDoorFrontendEndpointObject](New-AzFrontDoorFrontendEndpointObject.md)
Front Door 만들기를 위한 PSFrontendEndpoint 개체 만들기

### [New-AzFrontDoorHeaderActionObject](New-AzFrontDoorHeaderActionObject.md)
PSHeaderAction 개체를 만듭니다.

### [New-AzFrontDoorHealthProbeSettingObject](New-AzFrontDoorHealthProbeSettingObject.md)
Front Door 만들기를 위한 PSHealthProbeSetting 개체 만들기

### [New-AzFrontDoorLoadBalancingSettingObject](New-AzFrontDoorLoadBalancingSettingObject.md)
Front Door 만들기를 위한 PSLoadBalancingSetting 개체 만들기

### [New-AzFrontDoorRoutingRuleObject](New-AzFrontDoorRoutingRuleObject.md)
Front Door 만들기를 위한 PSRoutingRuleObject 만들기

### [New-AzFrontDoorRulesEngine](New-AzFrontDoorRulesEngine.md)
지정된 Front Door에 대한 새 규칙 엔진 구성을 작성합니다. 

### [New-AzFrontDoorRulesEngineActionObject](New-AzFrontDoorRulesEngineActionObject.md)
규칙 엔진 규칙을 만들기 위한 PSRulesEngineAction 개체를 만듭니다.

### [New-AzFrontDoorRulesEngineMatchConditionObject](New-AzFrontDoorRulesEngineMatchConditionObject.md)
규칙 엔진 규칙을 만들기 위한 PSRulesEngineMatchCondition 개체를 만듭니다.

### [New-AzFrontDoorRulesEngineRuleObject](New-AzFrontDoorRulesEngineRuleObject.md)
규칙 엔진 생성을 위한 PSRulesEngineRule 개체를 만듭니다.

### [New-AzFrontDoorWafCustomRuleObject](New-AzFrontDoorWafCustomRuleObject.md)
WAF 정책 만들기를 위한 CustomRule 개체 만들기

### [New-AzFrontDoorWafManagedRuleExclusionObject](New-AzFrontDoorWafManagedRuleExclusionObject.md)
WAF 관리 규칙 집합, 그룹 또는 규칙에 대한 관리되는 규칙 제외 개체를 만듭니다.

### [New-AzFrontDoorWafManagedRuleObject](New-AzFrontDoorWafManagedRuleObject.md)
WAF 정책 만들기를 위한 ManagedRule 개체 만들기

### [New-AzFrontDoorWafManagedRuleOverrideObject](New-AzFrontDoorWafManagedRuleOverrideObject.md)
관리되는 규칙 개체 만들기

### [New-AzFrontDoorWafMatchConditionObject](New-AzFrontDoorWafMatchConditionObject.md)
WAF 정책 만들기를 위한 MatchCondition 개체 만들기

### [New-AzFrontDoorWafPolicy](New-AzFrontDoorWafPolicy.md)
WAF 정책 만들기

### [New-AzFrontDoorWafRuleGroupOverrideObject](New-AzFrontDoorWafRuleGroupOverrideObject.md)
WAF 정책 만들기에 대한 RuleGroupOverride 개체 만들기

### [Remove-AzFrontDoor](Remove-AzFrontDoor.md)
Front Door 부하 균형 조정기 제거

### [Remove-AzFrontDoorContent](Remove-AzFrontDoorContent.md)
Front Door에서 콘텐츠 제거

### [Remove-AzFrontDoorRulesEngine](Remove-AzFrontDoorRulesEngine.md)
Front Door에서 규칙 엔진 제거

### [Remove-AzFrontDoorWafPolicy](Remove-AzFrontDoorWafPolicy.md)
WAF 정책 제거

### [Set-AzFrontDoor](Set-AzFrontDoor.md)
Front Door 부하 균형 조정기 업데이트

### [Set-AzFrontDoorRulesEngine](Set-AzFrontDoorRulesEngine.md)
규칙 엔진을 업데이트합니다.

### [Update-AzFrontDoorWafPolicy](Update-AzFrontDoorWafPolicy.md)
WAF 정책 업데이트

