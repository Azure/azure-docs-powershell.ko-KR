---
title: Azure 컨텍스트 및 로그인 자격 증명
description: 여러 PowerShell 세션에 걸쳐 Azure 자격 증명 및 다른 정보를 재사용하는 방법에 대해 알아보세요.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: c79d1d634d5b76b2c6ab6b6ab309c2d49f9f7678
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363303"
---
# <a name="azure-powershell-context-objects"></a>Azure PowerShell 컨텍스트 개체

Azure PowerShell은 _Azure PowerShell 컨텍스트 개체_(Azure 컨텍스트)를 사용하여 구독 및 인증 정보를 보관합니다. 둘 이상의 구독이 있는 경우 Azure 컨텍스트를 사용하여 Azure PowerShell cmdlet을 실행할 구독을 선택할 수 있습니다. Azure 컨텍스트는 여러 PowerShell 세션에서 로그인 정보를 저장하고 백그라운드 작업을 실행하는 데도 사용됩니다.

이 문서에서는 구독 또는 계정 관리가 아닌 Azure 컨텍스트 관리에 대해 설명합니다. 사용자, 구독, 테넌트 또는 기타 계정 정보를 관리하려면 [Azure Active Directory](/azure/active-directory) 설명서를 참조하세요. 백그라운드 또는 병렬 작업을 실행하기 위한 컨텍스트 사용에 대한 자세한 내용은 Azure 컨텍스트에 익숙해진 후 [PowerShell 작업 에서 Azure PowerShell cmdlet 사용](using-psjobs.md)을 참조하세요.

## <a name="overview-of-azure-context-objects"></a>Azure 컨텍스트 개체 개요

Azure 컨텍스트는 명령을 실행할 활성 구독과 Azure Cloud에 연결하는 데 필요한 인증 정보를 나타내는 PowerShell 개체입니다. Azure 컨텍스트를 사용하면 구독을 전환할 때마다 Azure PowerShell에서 계정을 다시 인증할 필요가 없습니다. 컨텍스트는 다음과 같이 구성됩니다.

* [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount)를 사용하여 Azure에 로그인하는 데 사용된 _계정_. Azure 컨텍스트는 계정 관점에서 사용자, 애플리케이션 ID 및 서비스 주체를 동일하게 처리합니다.
* _테넌트_와 연결된 Azure 리소스를 만들고 실행하기 위한 Microsoft와의 서비스 계약인 활성 _구독_. 테넌트는 종종 설명서에서 또는 Active Directory로 작업할 때 _조직_이라고도 합니다.
* Azure Cloud에 액세스하기 위해 저장된 인증 토큰인 _토큰 캐시_에 대한 참조입니다. 이 토큰이 저장되는 위치와 지속 기간은 [컨텍스트 자동 저장 설정](#save-azure-contexts-across-powershell-sessions)에 의해 결정됩니다.

이러한 용어에 대한 자세한 내용은 [Azure Active Directory 용어](/azure/active-directory/fundamentals/active-directory-whatis#terminology)를 참조하세요. Azure 컨텍스트에서 사용되는 인증 토큰은 영구 세션의 일부인 다른 저장된 토큰과 동일합니다. 

`Connect-AzAccount`에 로그인하면 기본 구독에 대해 하나 이상의 Azure 컨텍스트가 생성됩니다. `Connect-AzAccount`에 의해 반환된 개체는 PowerShell 세션의 나머지 부분에 사용되는 기본 Azure 컨텍스트입니다.

## <a name="get-azure-contexts"></a>Azure 컨텍스트 가져오기

사용 가능한 Azure 컨텍스트는 [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet을 사용하여 검색됩니다. `-ListAvailable`을 사용하여 사용 가능한 모든 컨텍스트를 나열합니다.

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

또는 이름별로 컨텍스트를 가져옵니다.

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

컨텍스트 이름은 연결된 구독의 이름과 다를 수 있습니다.

> [!IMPORTANT]
> 사용 가능한 Azure 컨텍스트가 항상 사용 가능한 구독은 __아닙니다__. Azure 컨텍스트는 로컬에 저장된 정보만 표시합니다. [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet을 사용하여 구독을 가져올 수 있습니다.

## <a name="create-a-new-azure-context-from-subscription-information"></a>구독 정보에서 새 Azure 컨텍스트 만들기

[Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet을 사용하여 새 Azure 컨텍스트를 만들고 활성 컨텍스트로 설정합니다.
새 Azure 컨텍스트를 만드는 가장 쉬운 방법은 기존 구독 정보를 사용하는 것입니다. 이 cmdlet은 `Get-AzSubscription`의 출력 개체를 파이프된 값으로 사용하고 새 Azure 컨텍스트를 구성하도록 디자인되었습니다.

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

또는 필요한 경우 구독 이름 또는 ID와 테넌트 ID를 지정합니다.

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

`-Name` 인수를 생략하면 구독의 이름과 ID는 `Subscription Name (subscription-id)` 형식의 컨텍스트 이름으로 사용됩니다.

## <a name="change-the-active-azure-context"></a>활성 Azure 컨텍스트 변경

`Set-AzContext` 및 [Select-AzContext](/powershell/module/az.accounts/set-azcontext)를 사용하여 활성 Azure 컨텍스트를 변경할 수 있습니다. [새 Azure 컨텍스트 만들기](#create-a-new-azure-context-from-subscription-information)에 설명된 대로 `Set-AzContext`는 구독에 대한 Azure 컨텍스트가 없는 경우 새로 하나 만든 다음, 해당 컨텍스트를 활성 컨텍스트로 사용하도록 전환합니다.

`Select-AzContext`는 기존 Azure 컨텍스트에만 사용하도록 되어 있으며 `Set-AzContext -Context`를 사용하는 것과 유사하게 작동하지만 파이프와 함께 사용하도록 디자인되었습니다.

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Azure PowerShell의 다른 많은 계정 및 컨텍스트 관리 명령과 마찬가지로 `Set-AzContext` 및 `Select-AzContext`는 컨텍스트 활성 시간을 제어할 수 있도록 `-Scope` 인수를 지원합니다. `-Scope`를 사용하면 기본값을 변경하지 않고 단일 세션의 활성 컨텍스트를 변경할 수 있습니다.

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

전체 PowerShell 세션에서 컨텍스트를 전환하지 않으려면 `-AzContext` 인수를 사용하여 지정된 컨텍스트에 대해 모든 Azure PowerShell 명령을 실행할 수 있습니다.

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

Azure PowerShell cmdlet을 사용한 컨텍스트의 다른 주요 용도는 백그라운드 명령을 실행하는 것입니다. Azure PowerShell을 사용하여 PowerShell 작업을 실행하는 방법에 대한 자세한 내용은 [PowerShell 작업에서 Azure PowerShell cmdlet 실행](using-psjobs.md)을 참조하세요.

## <a name="save-azure-contexts-across-powershell-sessions"></a>PowerShell 세션에서 Azure 컨텍스트 저장

기본적으로 Azure 컨텍스트는 PowerShell 세션 간에 사용하기 위해 저장됩니다. 다음과 같은 방법으로 이 동작을 변경합니다.

* `Connect-AzAccount`와 함께 `-Scope Process`를 사용하여 로그인

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  이 로그인의 일부로 반환된 Azure 컨텍스트는 현재 세션에 _대해서만_ 유효하며 Azure PowerShell 컨텍스트 자동 저장 설정에 관계없이 자동으로 저장되지 않습니다.
* [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet을 사용하여 AzurePowershell의 컨텍스트 자동 저장을 사용하지 않습니다.
  컨텍스트 자동 저장을 사용하지 않으면 저장된 토큰이 지워지지 __않습니다__. 저장된 Azure 컨텍스트 정보를 지우는 방법에 대해 알아보려면 [Azure 컨텍스트 및 자격 증명 제거](#remove-azure-contexts-and-stored-credentials)를 참조하세요.
* [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet을 사용하여 Azure 컨텍스트 자동 저장을 명시적으로 사용하도록 설정할 수 있습니다. 자동 저장을 사용하면 사용자의 모든 컨텍스트가 이후의 PowerShell 세션을 위해 로컬로 저장됩니다.
* 컨텍스트를 [Import-AzContext](/powershell/module/az.accounts/import-azcontext)와 함께 로드할 수 있는 향후 PowerShell 세션에서 사용할 [Save-AzContext](/powershell/module/az.accounts/save-azcontext)와 함께 컨텍스트를 수동으로 저장합니다.

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> 컨텍스트 자동 저장을 사용하지 않으면 저장된 모든 컨텍스트 정보는 지워지지 __않습니다__. 저장된 정보를 제거하려면 [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet을 사용합니다. 저장된 컨텍스트 제거에 대한 자세한 내용은 [컨텍스트 및 자격 증명 제거](#remove-azure-contexts-and-stored-credentials)를 참조하세요.

이러한 각각의 명령은 `-Scope` 매개 변수를 지원하며, 현재 실행중인 프로세스에만 적용되는 `Process` 값을 취합니다. 예를 들어, PowerShell 세션을 종료한 후 새로 만든 컨텍스트가 저장되지 않도록 하기 위해

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

컨텍스트 정보 및 토큰은 Windows의 `$env:USERPROFILE\.Azure` 디렉토리 및 다른 플랫폼의 `$HOME/.Azure`에 저장됩니다. 구독 ID 및 테넌트 ID와 같은 중요한 정보가 로그 또는 저장된 컨텍스트를 통해 저장된 정보에 계속 노출될 수 있습니다. 저장된 정보를 지우는 방법에 대해 알아보려면 [컨텍스트 및 자격 증명 제거](#remove-azure-contexts-and-stored-credentials) 섹션을 참조하세요.

## <a name="remove-azure-contexts-and-stored-credentials"></a>Azure 컨텍스트 및 저장된 자격 증명 제거

Azure 컨텍스트 및 로그인 자격 증명을 지우기 위해

* [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount)를 사용하여 계정에서 로그아웃합니다.
  계정 또는 컨텍스트별로 계정에서 로그아웃할 수 있습니다.

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  연결을 끊으면 항상 저장된 인증 토큰이 제거되고 연결이 끊어진 사용자 또는 컨텍스트와 관련된 저장된 컨텍스트가 지워집니다.
* [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext)를 사용합니다. 이 cmdlet은 항상 저장된 컨텍스트 및 인증 토큰을 제거하고 또한 사용자도 로그아웃합니다.
* [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext)를 사용하여 컨텍스트를 제거합니다.
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  활성 컨텍스트를 제거하면 Azure에서 연결이 끊어지며 `Connect-AzAccount`를 사용하여 다시 인증해야 합니다.

## <a name="see-also"></a>참고 항목

* [PowerShell 작업에서 Azure PowerShell cmdlet 실행](using-psjobs.md)
* [Azure Active Directory 용어](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Az.Accounts 참조](/powershell/module/az.accounts)
