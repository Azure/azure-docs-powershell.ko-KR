---
title: PowerShellGet으로 Azure PowerShell 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: f7a1658cdcafd1e8d6cba51ead26f9ddaa8c4c56
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407390"
---
# <a name="install-azure-powershell"></a>Azure Powershell 설치

이 문서에서는 [PowerShellGet](/powershell/scripting/gallery/installing-psget)을 사용하여 Azure PowerShell 모듈을 설치하는 방법에 대해 설명합니다. 이러한 지침은 Windows, macOS 및 Linux 플랫폼에서 작동합니다.

Azure PowerShell은 Azure [Cloud Shell](/azure/cloud-shell/overview)에서도 사용할 수 있으며, 이제 [Docker 이미지](azureps-in-docker.md)에도 미리 설치되어 있습니다.

## <a name="requirements"></a>요구 사항

> [!NOTE]
> 모든 플랫폼에서 Azure PowerShell과 함께 사용할 것을 권장하는 PowerShell 버전은 PowerShell 7.x 이상입니다.

Azure PowerShell은 모든 플랫폼에서 PowerShell 6.2.4 이상과 함께 작동합니다. Windows에서는 PowerShell 5.1에서도 지원됩니다. 사용하는 운영 체제에 제공되는 [최신 버전의 PowerShell](/powershell/scripting/install/installing-powershell)을 설치합니다. PowerShell 6.2.4 이상에서 실행하는 경우 Azure PowerShell과 관련된 추가 요구 사항이 없습니다.

PowerShell 버전을 확인하려면 다음 명령을 실행합니다.

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

Windows의 PowerShell 5.1에서 Azure PowerShell을 사용하려면 다음을 수행합니다.

1. [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다.
   Windows 10 버전 1607 이상을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.
2. [.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.
3. 최신 버전의 PowerShellGet이 있는지 확인합니다. `Install-Module -Name PowerShellGet -Force`을 실행합니다.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell 모듈 설치

> [!WARNING]
> Windows에서 PowerShell 5.1용 AzureRM과 Az 모듈을 동시에 설치할 수 없습니다. 시스템에서 AzureRM을 사용할 수 있도록 유지해야 하는 경우 PowerShell 6.2.4 이상용 Az 모듈을 설치합니다.

기본 설치 방법은 PowerShellGet cmdlet을 사용하는 것입니다. 현재 사용자에 대해서만 Az 모듈을 설치합니다. 이는 추천되는 설치 방법입니다. 이 방법은 Windows, macOS 및 Linux 플랫폼에서 동일하게 작동합니다. PowerShell 세션에서 다음 명령을 실행합니다.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다. PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.

시스템의 모든 사용자에 대해 모듈을 설치하려면 관리자 권한이 필요합니다. Windows에서 **관리자 권한으로 실행** 을 사용하여 PowerShell 세션을 시작하거나 macOS 또는 Linux에서 `sudo` 명령을 사용합니다.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Az 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다. 이 모듈을 설치하면 갤러리의 모든 사용 가능한 Az PowerShell 모듈이 다운로드되고, cmdlet을 사용할 수 있게 됩니다.

## <a name="install-offline"></a>오프라인 설치

일부 환경에서는 PowerShell 갤러리에 연결할 수 없습니다. 이러한 경우에도 다음 방법 중 하나를 사용하여 오프라인으로 설치할 수 있습니다.

* 모듈을 네트워크의 다른 위치에 다운로드하여 이 모듈을 네트워크의 설치 원본으로 사용합니다.
  이 방법을 사용하면 단일 서버 또는 파일 공유에서 PowerShell 모듈을 캐시하여 PowerShellGet을 사용하여 연결이 끊긴 시스템에 배포할 수 있습니다. [로컬 PowerShellGet 리포지토리로 작업](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)을 통해 로컬 리포지토리를 설정하고 연결이 끊어진 시스템에 설치하는 방법을 알아봅니다.
* 네트워크에 연결된 컴퓨터에 [Azure PowerShell MSI](install-az-ps-msi.md)를 다운로드한 다음, PowerShell 갤러리에 액세스하지 않고 설치 관리자를 시스템에 복사합니다. MSI 설치 관리자는 Windows의 PowerShell 5.1에서만 작동합니다.
* [Save-Module](/powershell/module/PowershellGet/Save-Module)을 사용하여 모듈을 파일 공유에 저장하거나 다른 소스에 저장하고 다른 컴퓨터에 수동으로 복사합니다.

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>문제 해결

Azure PowerShell 모듈을 설치할 때 나타나는 몇 가지 일반적인 문제는 다음과 같습니다. 여기에 나열되지 않은 문제가 발생하면 [GitHub에서 문제를 제출](https://github.com/azure/azure-powershell/issues)하세요.

### <a name="proxy-blocks-connection"></a>프록시 연결 차단

`Install-Module`에서 PowerShell 갤러리에 연결할 수 없다는 오류가 발생하면 프록시를 지원하고 있을 수 있습니다. 운영 체제와 네트워크 환경에 따라 시스템 수준 프록시 구성에 대한 요구 사항이 다릅니다. 프록시 설정 및 환경에 맞게 구성하는 방법에 대해서는 시스템 관리자에게 문의하세요.

PowerShell 자체는 이 프록시를 자동으로 사용하도록 구성되지 않을 수 있습니다. PowerShell 5.1 이상에서는 다음 명령을 사용하여 프록시를 사용하도록 PowerShell 세션을 구성합니다.

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

운영 체제 자격 증명이 올바르게 구성되면 이 구성에서 프록시를 통해 PowerShell 요청을 라우팅합니다. 이 설정이 세션 간에 유지되도록 하려면 명령을 [PowerShell 프로필](/powershell/module/microsoft.powershell.core/about/about_profiles)에 추가합니다.

패키지를 설치하려면 프록시에서 다음 주소에 대한 HTTPS 연결을 허용해야 합니다.

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>로그인

Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> 모듈 자동 로딩을 비활성화한 경우 `Import-Module -Name Az`을 사용하여 모듈을 수동으로 가져옵니다.
> 모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.

모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다. PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.

## <a name="update-the-azure-powershell-module"></a>Azure PowerShell 모듈 업데이트

PowerShell 모듈을 업데이트하려면 모듈을 설치하는 데 사용한 것과 동일한 방법을 사용해야 합니다. 예를 들어 처음에 `Install-Module`을 사용한 경우 [Update-Module](/powershell/module/powershellget/update-module)을 사용하여 최신 버전을 가져와야 합니다. 처음에 MSI 패키지를 사용한 경우 새 MSI 패키지를 다운로드하여 설치해야 합니다.

PowerShellGet cmdlet은 MSI 패키지에서 설치된 모듈을 업데이트할 수 없습니다. MSI 패키지는 PowerShellGet을 사용하여 설치한 모듈을 업데이트하지 않습니다. PowershellGet을 사용하여 업데이트하는 데 문제가 있는 경우 **업데이트** 하는 대신 **다시 설치** 해야 합니다. 다시 설치는 설치와 동일한 방식으로 수행되지만 `-Force` 매개 변수를 추가해야 합니다.

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

MSI 기반 설치와 달리 PowerShellGet을 사용하여 설치하거나 업데이트해도 시스템에 있을 수 있는 이전 버전은 제거되지 않습니다. 시스템에서 이전 버전의 Azure PowerShell을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조하세요. MSI 기반 설치에 대한 자세한 내용은 [MSI를 사용하여 Azure PowerShell 설치](install-az-ps-msi.md)를 참조하세요.

## <a name="use-multiple-versions-of-azure-powershell"></a>여러 버전의 Azure PowerShell 사용

Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다. 여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.

모듈 버전이 두 개 이상인 경우 모듈 자동 로드 및 `Import-Module`이 기본적으로 최신 버전을 로드합니다.

`-RequiredVersion` 매개 변수를 사용하여 특정 버전의 `Az` 모듈을 설치하거나 로드할 수 있습니다.

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a>PowerShellGet에서 여러 리포지토리 사용

시스템의 PowerShellGet에 리포지토리를 추가하고 그 중 2개 이상에서 Az 모듈을 찾을 수 있는 경우 **Repository** 매개 변수가 필요합니다.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a>피드백 제공

버그가 Azure PowerShell에 있으면 [GitHub에서 문제를 제기](https://github.com/Azure/azure-powershell/issues)하세요. 명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.

## <a name="next-steps"></a>다음 단계

Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요. Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.
