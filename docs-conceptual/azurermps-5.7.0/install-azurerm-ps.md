---
title: PowerShellGet으로 Azure PowerShell을 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 17e625dacfadff07b0498ac173b7b2c312172f87
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387771"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>PowerShellGet으로 Azure PowerShell을 설치

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

이 아티클에서는 PowerShellGet을 사용하여 Windows용 PowerShell 5.x용 Azure PowerShell 모듈을 설치하는 단계를 설명합니다. PowerShellGet 및 모듈 관리는 Azure PowerShell을 설치하는 더 좋은 방법이지만 대신 웹 플랫폼 설치 관리자 또는 MSI 패키지로 설치하려는 경우 [다른 설치 방법](other-install.md)을 참조합니다.

Azure 클래식 배포 모델은 본 버전의 Azure PowerShell에서 지원되지 않습니다. 클래식 배포에 대한 지원은 [Azure PowerShell Service Management 모듈 설치](/powershell/azure/servicemanagement/install-azure-ps) 지침을 참조합니다.

> [!IMPORTANT]
> MacOS 또는 Linux 용 AzureRM 모듈은 지원되지 않습니다. 이러한 플랫폼에서 Azure PowerShell cmdlet을 사용하려면 [Az 모듈을 설치](/powershell/azure/install-az-ps)합니다.

## <a name="requirements"></a>요구 사항

Azure PowerShell을 설치하려면, PowerShellGet 버전 1.1.2.0 이상이 필요합니다. 귀하의 시스템에서 가능한지 확인하려면 다음 명령을 실행합니다:

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

다음과 비슷하게 표시됩니다.

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

PowerShellGet 설치를 업데이트하려면 다음 명령을 실행합니다:

```powershell-interactive
Install-Module PowerShellGet -Force
```

PowerShellGet이 설치되지 않은 경우, 귀하의 시스템을 위해 아래 표의 지침을 따릅니다.

|시나리오|설치 지침|
|---|---|
|윈도우 10<br/>Windows Server 2016|OS에 포함된 WMF(Windows Management Framework) 5.0으로 빌드됩니다.|
|PowerShell 5로 업그레이드| <ol><li>[최신 버전의 WMF 설치](https://www.microsoft.com/download/details.aspx?id=54616)</li><li>다음 명령 실행:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|PowerShell 3 또는 PowerShell 4이 설치된 Windows|<ol><il>[PackageManagement 모듈 가져오기](https://go.microsoft.com/fwlink/?LinkID=746217)</il><li>다음 명령 실행:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> PowerShellGet을 사용하려면 스크립트를 실행할 수 있게 하는 실행 정책이 필요합니다. PowerShell의 실행 정책에 대한 자세한 내용은 [실행 정책 정보](/powershell/module/microsoft.powershell.core/about/about_execution_policies)(영문)를 참조하세요.
>
> [!IMPORTANT]
> 이 문서에서 설명된 모듈인 AzureRM에서는 .NET Framework를 사용합니다. 이렇게 하면 .NET Core를 사용하는 PowerShell 6.0과 호환되지 않습니다. PowerShell 6.0을 사용하는 경우, [macOS 및 Linux에 대한 설치 지침](install-azurermps-maclinux.md)을 따릅니다.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell 모듈 설치

PowerShell 갤러리에서 모듈을 설치하려면 상승된 권한이 필요합니다. Azure PowerShell을 설치하려면 승격된 세션에서 다음 명령을 실행합니다.

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> NuGet 2.8.5.201 이전 버전을 사용하는 경우 최신 버전의 NuGet을 다운로드하여 설치하라는 메시지가 표시됩니다.

기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다. PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.

`AzureRM` 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다. 설치하면 사용 가능한 모든 Azure Resource Manager 모듈이 다운로드되고 cmdlet을 사용할 수 있게 됩니다.

## <a name="sign-in"></a>로그인

Azure PowerShell을 사용하여 작업을 시작 하려면 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet을 사용하여 현재 PowerShell 세션에 `AzureRM`을 로드한 후 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다. `AzureRM` 모듈을 자동으로 가져오려면 PowerShell 프로필을 설정해야 하며, 프로필 설정은 [프로필 정보](/powershell/module/microsoft.powershell.core/about/about_profiles)에서 알아볼 수 있습니다.
Azure 로그인을 세션 간에 유지하는 방법을 알아보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조합니다.

## <a name="update-the-azure-powershell-module"></a>Azure PowerShell 모듈 업데이트

[Update-Module](/powershell/module/powershellget/update-module)을 실행하여 Azure PowerShell 설치를 업데이트할 수 있습니다. 이 명령은 이전 버전을 제거하지 __않습니다__.

```powershell-interactive
Update-Module -Name AzureRM
```

Azure PowerShell의 이전 버전을 시스템에서 제거하려면, [Azure PowerShell 모듈 제거](uninstall-azurerm-ps.md)를 참조합니다.

## <a name="use-multiple-versions-of-azure-powershell"></a>여러 버전의 Azure PowerShell 사용

여러 버전의 Azure PowerShell을 설치하는 것은 가능합니다. 온-프레미스 Azure Stack 리소스로 작업하거나 PowerShell 5.0으로 업데이트할 수 없는 이전 버전의 Windows를 실행하거나 Azure 클래식 배포 모델을 사용하는 경우 둘 이상의 버전이 필요할 수 있습니다. 이전 버전을 설치하려면 `-RequiredVersion` 인수를 설치 시 제공합니다.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Azure PowerShell 모듈 로드 시, 기본으로 최신 버전이 로드됩니다. 다른 버전을 로드하려면 `-RequiredVersion` 인수를 제공합니다.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>피드백 제공

Azure Powershell 사용 중 버그 발생 시, [ GitHub에서 문제 제출](https://github.com/Azure/azure-powershell/issues)을 해 주십시오.
명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet을 사용해 보세요.

## <a name="next-steps"></a>다음 단계

Azure PowerShell 사용을 시작하려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하여 모듈 및 모듈의 기능에 대해 자세히 알아보세요.
