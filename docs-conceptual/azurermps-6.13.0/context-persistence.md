---
title: PowerShell 세션간에 사용자 자격 증명 유지
description: 여러 PowerShell 세션에 걸쳐 Azure 자격 증명 및 다른 정보를 재사용하는 방법에 대해 알아보세요.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 1e5c89a43886343bfc0a1affb5133a7cb6af0bcc
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65854157"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>PowerShell 세션간에 사용자 자격 증명 유지

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell은 **Azure Context Autosave**라고 하는 기능을 제공하며, 이는 다음과 같은 기능을 제공합니다.

- 새 PowerShell 세션에서 다시 사용하기 위한 로그인 정보 보존.
- 오랫동안 수행되는 cmdlet을 실행하기 위한 더 쉬운 백그라운드 작업 사용.
- 별도 로그인 없이 계정, 구독 및 환경 간 전환.
- 동일한 PowerShell 세션에서 다른 자격 증명 및 구독을 동시에 사용하여 작업 실행.

## <a name="azure-contexts-defined"></a>정의된 Azure 컨텍스트

*Azure 컨텍스트*는 Azure PowerShell cmdlet의 대상을 정의하는 정보 집합입니다. 컨텍스트는 5개의 부분으로 구성됩니다.

- *계정* - Azure와의 통신을 인증하는 데 사용되는 사용자 이름 또는 서비스 주체
- *구독* - 동작하는 리소스를 포함하는 Azure 구독.
- *테넌트* - 구독을 포함하는 Azure Active Directory 테넌트. 테넌트는 ServicePrincipal 인증에서 더 중요합니다.
- *환경* - 목표가 되는 특정 Azure Cloud(보통 Azure 전역 클라우드).
  그러나 환경 설정을 사용하여 대상 국가, 정부 및 온-프레미스(Azure Stack) 클라우드도 대상으로 지정할 수 있습니다.
- *자격 증명* - Azure에서 사용자 ID를 확인하고 Azure의 리소스에 액세스하기 위한 사용자의 권한 부여를 확인하는 데 사용되는 정보

이전 릴리스에서는 새 PowerShell 세션을 열 때마다 Azure 컨텍스트를 만들어야 했습니다. Azure PowerShell v4.4.0부터는 새 PowerShell 세션을 열 때마다 Azure 컨텍스트를 자동으로 저장할 수 있습니다.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>다음 로그인을 위해 컨텍스트를 자동으로 저장

버전 6.3.0 이상에서 Azure PowerShell은 세션 간에 자동으로 컨텍스트 정보를 유지합니다. PowerShell이 사용자의 컨텍스트 및 자격 증명을 기억하지 않도록 설정하려면 `Disable-AzureRmContextAutoSave`를 사용합니다. PowerShell 세션을 열 때마다 Azure에 로그인해야 합니다.

Azure PowerShell이 PowerShell 세션을 닫은 후 사용자의 컨텍스트를 기억하도록 하려면 `Enable-AzureRmContextAutosave`를 사용합니다. 컨텍스트 및 자격 증명 정보는 사용자 디렉터리의 숨겨진 특수 폴더(`%AppData%\Roaming\Windows Azure PowerShell`)에 자동으로 저장됩니다.
새로운 PowerShell 세션마다 마지막 세션에 사용된 컨텍스트가 대상으로 지정됩니다.

Azure 컨텍스트를 관리할 수 있는 cmdlet을 사용하면 세분화된 제어가 가능합니다. 변경 내용을 현재 PowerShell 세션(`Process` 범위)에만 적용하거나 또는 모든 PowerShell 세션(`CurrentUser` 범위)에 적용하려는 경우가 있습니다. 이러한 옵션은 [컨텍스트 범위 사용](#using-context-scopes)에서 자세히 설명합니다.

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Azure PowerShell cmdlet을 백그라운드 작업으로 실행

**Azure 컨텍스트 자동 저장** 기능을 사용하면 PowerShell 백그라운드 작업으로 컨텍스트를 공유할 수 있습니다. PowerShell을 사용하면 장기 실행 작업을 작업이 완료될 때까지 기다리지 않고 백그라운드 작업으로 시작하고 모니터링할 수 있습니다. 두 가지 방법을 통해 백그라운드 작업으로 자격 증명을 공유할 수 있습니다.

- 컨텍스트를 인수로 전달

  대부분 AzureRM cmdlet을 사용하면 cmdlet에 컨텍스트를 매개 변수로 전달할 수 있습니다. 다음 예제와 같이 백그라운드 작업으로 컨텍스트를 전달할 수 있습니다.

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- 자동 저장이 활성화된 기본 컨텍스트 사용

  **컨텍스트 자동 저장**을 사용하도록 설정한 경우 백그라운드 작업은 자동으로 기본 저장된 기본 컨텍스트를 사용합니다.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

백그라운드 작업의 결과를 알아야 하는 경우 `Get-Job`을 사용하여 작업 상태를 확인하고 `Wait-Job`을 사용하여 작업이 완료될 때까지 대기합니다. 백그라운드 작업의 출력을 캡처하거나 표시하려면 `Receive-Job`을 사용합니다. 자세한 내용은 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)를 참조하세요.

## <a name="creating-selecting-renaming-and-removing-contexts"></a>컨텍스트 생성, 선택, 이름 바꾸기 및 제거

컨텍스트를 작성하려면 Azure에 로그인해야 합니다. `Connect-AzureRmAccount` cmdlet(또는 해당 별칭인 `Login-AzureRmAccount`)은 Azure PowerShell cmdlet에서 사용하는 기본 컨텍스트를 설정하고, 사용자는 이를 통해 자격 증명에서 허용하는 모든 테넌트 또는 구독에 액세스할 수 있습니다.

로그인한 후 새 컨텍스트를 추가하려면 `Set-AzureRmContext`(또는 해당 별칭인 `Select-AzureRmSubscription`)를 사용합니다.

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

앞의 예제는 현재 자격 증명을 사용하여 새 컨텍스트 대상인 ‘Contoso Subscription 1’을 추가합니다. 새 컨텍스트는 ‘Contoso1’이라고 합니다. 컨텍스트에 대한 이름을 제공하지 않은 경우 계정 ID 및 구독 ID를 사용하는 기본 이름이 사용됩니다.

기존 컨텍스트 이름을 바꾸려면 `Rename-AzureRmContext` cmdlet을 사용합니다. 다음은 그 예입니다. 

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

이 예제에서는 자동 이름 `[user1@contoso.org; 123456-7890-1234-564321]`을 사용하는 컨텍스트 이름을 간단한 이름인 ‘Contoso2’로 바꿉니다. 또한 컨텍스트를 관리하는 cmdlet에서 탭 완성 기능을 사용하면 컨텍스트를 빠르게 선택할 수 있습니다.

마지막으로, 컨텍스트를 제거하려면 `Remove-AzureRmContext` cmdlet을 사용합니다.  다음은 그 예입니다. 

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

‘Contoso2’로 명명된 컨텍스트를 잊었습니다. `Set-AzureRmContext`를 사용하여 나중에 다시 이 컨텍스트를 만들 수 있습니다.

## <a name="removing-credentials"></a>자격 증명 제거

`Disconnect-AzureRmAccount`(`Logout-AzureRmAccount`라고도 함)를 사용하여 사용자 또는 서비스 주체에 대한 모든 자격 증명 및 연결된 컨텍스트를 제거할 수 있습니다. `Disconnect-AzureRmAccount` cmdlet을 매개 변수 없이 실행하면 현재 컨텍스트에서 사용자 또는 서비스 주체에 연결된 모든 자격 증명 및 컨텍스트를 제거합니다. 사용자 이름, 서비스 주체 이름 또는 컨텍스트를 특정 보안 주체를 대상으로 전달할 수 있습니다.

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>컨텍스트 범위 사용

경우에 따라 다른 세션에 영향을 주지 않고 PowerShell 세션에서 컨텍스트를 선택, 변경 또는 제거할 수도 있습니다. 컨텍스트 cmdlet의 기본 동작을 변경하려면 `Scope` 매개 변수를 사용합니다. `Process` 범위는 현재 세션에만 적용되도록 기본 동작을 재정의합니다. 반대로 `CurrentUser` 범위는 현재 세션만이 아닌 모든 세션의 컨텍스트를 변경합니다.

예를 들어, 다른 창에 영향을 주지 않고 현재 PowerShell 세션의 기본 컨텍스트 또는 다음에 세션을 열 때 사용되는 컨텍스트를 변경하려면 다음을 사용합니다.

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>컨텍스트 자동 저장 설정이 기억되는 방식

컨텍스트 자동 저장 설정은 사용자 Azure PowerShell 디렉터리(`%AppData%\Roaming\Windows Azure PowerShell`)에 저장됩니다. 컴퓨터 계정 중 일부 유형은 이 디렉터리에 액세스하지 못할 수도 있습니다. 이러한 시나리오에서 환경 변수를 사용할 수 있습니다.

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

‘true’로 설정하면 컨텍스트가 자동으로 저장됩니다. ‘false’로 설정하면 컨텍스트가 저장되지 않습니다.

## <a name="changes-to-the-azurermprofile-module"></a>AzureRM.Profile 모듈에 대한 변경 내용

컨텍스트 관리를 위한 새 cmdlet

- [Enable-AzureRmContextAutosave][enable] - powershell 세션 간에 컨텍스트를 저장할 수 있습니다.
  변경 내용이 전역 컨텍스트를 변경합니다.
- [Disable-AzureRmContextAutosave][disable] - 컨텍스트 자동 저장을 해제합니다. 새로운 각 PowerShell 세션은 다시 로그인해야 합니다.
- [Select-AzureRmContext][select] - 기본값으로 컨텍스트를 선택합니다. 모든 cmdlet이 인증을 위해 이 컨텍스트에서 자격 증명을 사용합니다.
- [Disconnect-AzureRmAccount][remove-cred] - 계정과 관련된 자격 증명 및 컨텍스트를 모두 제거합니다.
- [Remove-AzureRmContext][remove-context] - 명명된 컨텍스트의 이름을 바꿉니다.
- [Rename-AzureRmContext][rename] - 기존 컨텍스트의 이름을 바꿉니다.

기존 프로필 cmdlet에 대한 변경 내용

- [Add-AzureRmAccount][login] - 프로세스 또는 현재 사용자로 로그인의 범위를 지정할 수 있습니다.
  인증 후 기본 컨텍스트의 이름을 지정할 수 있습니다.
- [Import-AzureRmContext][import] - 프로세스 또는 현재 사용자로 로그인의 범위를 지정할 수 있습니다.
- [Set-AzureRmContext][set-context] - 기존의 명명된 컨텍스트를 선택하고, 프로세스 또는 현재 사용자로 범위를 변경할 수 있습니다.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
