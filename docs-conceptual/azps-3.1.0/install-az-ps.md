---
title: PowerShellGet으로 Azure PowerShell 설치
description: PowerShellGet으로 Azure PowerShell을 설치 하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537356"
---
# <a name="install-the-azure-powershell-module"></a>Azure PowerShell 모듈 설치

이 문서에서는 PowerShellGet을 사용하여 Azure PowerShell 모듈을 설치하는 방법을 설명합니다. 이러한 지침은 Windows, macOS 및 Linux 플랫폼에서 작동합니다. Az 모듈에 대해 현재 다른 설치 방법은 지원되지 않습니다.

## <a name="requirements"></a>요구 사항

Azure PowerShell은 Windows의 PowerShell 5.1 이상 또는 모든 플랫폼의 PowerShell Core 6.x 이상에서 작동합니다. PowerShell이 있거나 macOS 또는 Linux에 있는지 확실하지 않은 경우 [최신 버전의 PowerShell Core를 설치](/powershell/scripting/install/installing-powershell#powershell-core)하세요.

PowerShell 버전을 확인하려면 다음 명령을 실행합니다.

```powershell-interactive
$PSVersionTable.PSVersion
```

Windows의 PowerShell 5.1에서 Azure PowerShell을 실행하려면 다음을 수행합니다.

1. 필요한 경우 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다. Windows 10을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.
2. [.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.

PowerShell Core를 사용하는 경우 Azure PowerShell에 대한 추가 요구 사항이 없습니다.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell 모듈 설치

> [!WARNING]
> Windows용 PowerShell 5.1에서 사용하기 위해 AzureRM 및 Az 모듈을 모두 동시에 __설치할 수는 없습니다__. 시스템에서 AzureRM을 사용할 수 있도록 유지해야 하는 경우 PowerShell Core 6.x 이상용 Az 모듈을 설치합니다. 이렇게 하려면 [PowerShell Core 6.x 이상을 설치](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows)한 다음, PowerShell Core 터미널에서 다음 지침을 따르세요.

권장 설치 방법은 활성 사용자에 대해서만 설치하는 것입니다.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

시스템의 모든 사용자에 대해 설치하려면 관리자 권한이 필요합니다. 관리자 권한 PowerShell 세션에서 관리자 권한으로 실행하거나 macOS 또는 Linux에서 `sudo` 명령을 사용하여 실행합니다.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다. PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

설치를 계속하려면 `Yes` 또는 `Yes to All`로 답변합니다.

Az 모듈은 Azure PowerShell cmdlet의 롤업 모듈입니다. 설치하면 사용 가능한 모든 Azure Resource Manager 모듈이 다운로드되고 cmdlet을 사용할 수 있게 됩니다.

## <a name="install-offline"></a>오프라인 설치

일부 환경에서는 PowerShell 갤러리에 연결할 수 없습니다. 이러한 경우에도 다음 방법 중 하나를 사용하여 오프라인으로 설치할 수 있습니다.

* 모듈을 다른 위치에 다운로드한 다음, 이 모듈을 네트워크의 설치 소스로 사용합니다. 다소 복잡해 보일 수도 있지만 이 프로세스를 사용하면 단일 서버 또는 파일 공유에서 PowerShell 모듈을 캐시하여 PowerShellGet으로 연결이 끊긴 시스템에 배포할 수 있습니다. [로컬 PowerShellGet 리포지토리로 작업](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)을 통해 로컬 리포지토리를 설정하고 연결이 끊어진 시스템에 설치하는 방법을 알아봅니다.
* 네트워크에 연결된 컴퓨터에 [Azure PowerShell MSI](install-az-ps-msi.md)를 다운로드한 다음, PowerShell 갤러리에 액세스하지 않고 설치 관리자를 시스템에 복사합니다. MSI 설치 관리자는 Windows의 PowerShell 5.1에서만 작동합니다.
* [Save-Module](/powershell/module/PowershellGet/Save-Module)을 사용하여 모듈을 파일 공유에 저장하거나 다른 소스에 저장하고 다른 컴퓨터에 수동으로 복사합니다.
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>문제 해결

Azure PowerShell 모듈을 설치할 때 나타나는 몇 가지 일반적인 문제는 다음과 같습니다. 여기에 나열되지 않은 문제가 발생하면 [GitHub에서 문제를 제출](https://github.com/azure/azure-powershell/issues)하세요.

### <a name="proxy-blocks-connection"></a>프록시 연결 차단

`Install-Module`에서 PowerShell 갤러리에 연결할 수 없다는 오류가 발생하면 프록시를 지원하고 있을 수 있습니다. 운영 체제마다 시스템 전체 프록시 구성에 대한 요구 사항이 다르며 여기서는 자세히 다루지 않습니다. 프록시 설정 및 OS에 맞게 구성하는 방법은 시스템 관리자에게 문의하세요.

PowerShell 자체는 이 프록시를 자동으로 사용하도록 구성되지 않을 수 있습니다. PowerShell 5.1 이상에서는 다음 명령을 사용하여 PowerShell 세션에 사용할 프록시를 구성합니다.

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

운영 체제 자격 증명이 올바르게 구성되어 있으면 PowerShell 요청이 프록시를 통해 라우팅됩니다.
세션 간에 이 설정을 유지하려면 해당 명령을 [PowerShell 프로필](/powershell/module/microsoft.powershell.core/about/about_profiles)에 추가합니다.

패키지를 설치하려면 프록시에서 다음 주소에 대한 HTTPS 연결을 허용해야 합니다.

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>로그인

Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> 모듈 자동 로딩을 비활성화한 경우 `Import-Module Az`을 사용하여 모듈을 수동으로 가져옵니다. 모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.

모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다. PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.

## <a name="update-the-azure-powershell-module"></a>Azure PowerShell 모듈 업데이트

Az 모듈의 패키지 방식으로 인해 [Update-Module](/powershell/module/powershellget/update-module) 명령에서 설치를 올바르게 업데이트하지 않습니다. Az 모듈을 설치하면 실제로 모든 종속 하위 모듈을 수집하고 설치하며, 각 서비스에 대한 cmdlet을 제공합니다.
즉, Azure PowerShell 모듈을 업데이트하려면 __업데이트__ 하는 대신 __다시 설치__ 해야 합니다. 이 작업은 설치와 동일한 방식으로 수행되지만 `-Force` 인수를 추가해야 할 수도 있습니다.

```powershell
Install-Module -Name Az -AllowClobber -Force
```

이렇게 하면 설치된 모듈을 덮어쓸 수 있지만 시스템에 이전 버전이 아직 남아 있을 수 있습니다.
Azure PowerShell의 이전 버전을 시스템에서 제거하는 방법을 알아보려면, [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.

## <a name="use-multiple-versions-of-azure-powershell"></a>여러 버전의 Azure PowerShell 사용

Azure PowerShell은 버전을 2개 이상 설치할 수 없습니다. 여러 버전의 Azure PowerShell이 설치되어 있는지 확인하려면 다음 명령을 사용합니다.

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Azure PowerShell의 버전을 제거하려면 [Azure PowerShell 모듈 제거](uninstall-az-ps.md)를 참조합니다.

`-RequiredVersion` 인수를 사용하여 `Az` 모듈의 특정 버전을 설치하거나 로드할 수 있습니다.

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

모듈 버전이 두 개 이상인 경우 모듈 자동 로드 및 `Import-Module`이 기본적으로 최신 버전을 로드합니다.

## <a name="provide-feedback"></a>피드백 제공

Azure Powershell에서 버그 발생 시, [ GitHub에서 문제를 제출](https://github.com/Azure/azure-powershell/issues)하세요.
명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.

## <a name="next-steps"></a>다음 단계

Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.
Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.
