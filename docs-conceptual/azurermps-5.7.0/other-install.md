---
title: Azure PowerShell을 설치하는 다른 방법
description: PowerShellGet을 사용하지 않고 Azure PowerShell을 설치하는 방법
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 55a89861c3bcca41b940d34d945cd43690331f3e
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83385765"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>MSI 또는 웹 플랫폼 설치 관리자를 사용하여 Windows에 Azure PowerShell 설치

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

이 문서에서는 MSI 또는 웹 플랫폼 설치 관리자(WebPI)를 사용하여 Azure PowerShell을 Windows에 설치하는 방법에 대해 설명합니다.  
시스템에 필요한 경우에만 이러한 설치 방법을 사용합니다. Windows에 Azure PowerShell 설치에는 PowerShellGet을 사용하는 방법이 권장됩니다. PowerShellGet을 사용하여 Azure PowerShell을 설치하는 방법은 [PowerShellGet으로 Azure PowerShell 설치하기](install-azurerm-ps.md)를 참조합니다.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI 패키지를 사용하여 Windows에 설치 및 업데이트

Azure PowerShell은 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018)에서 사용할 수 있는 MSI 파일을 사용하여 설치할 수 있습니다. 이전 버전의 Azure 모듈이 MSI로 설치된 경우 설치 관리자에서 자동으로 제거합니다. MSI 패키지는 `${env:ProgramFiles}\WindowsPowerShell\Modules`에서 모듈을 설치합니다. `AzureRM` 및 `Azure` 모듈 모두 설치됩니다.

> [!NOTE]
> Azure 클래식 배포 모델을 사용하는 경우 `Azure` 모듈만 사용합니다.

Azure PowerShell을 사용하여 작업을 시작 하려면 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet을 사용하여 현재 PowerShell 세션에 `AzureRM`을 로드한 후 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다. `AzureRM` 모듈을 자동으로 가져오려면 PowerShell 프로필을 설정해야 하며, 프로필 설정은 [프로필 정보](/powershell/module/microsoft.powershell.core/about/about_profiles)에서 알아볼 수 있습니다.
Azure 로그인을 세션 간에 유지하는 방법을 알아보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조합니다.

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>웹 플랫폼 설치 관리자를 사용하여 Windows에 설치 및 업데이트

[Azure PowerShell WebPI 패키지](https://aka.ms/webpi-azps)를 다운로드하고 설치를 시작합니다. 이전 버전의 Azure 모듈이 MSI로부터 또는 WebPI로 설치된 경우 설치 관리자에서 자동으로 제거합니다. 모듈이 `${env:ProgramFiles}\WindowsPowerShell\Modules`에 설치됩니다. `AzureRM` 및 `Azure` 모듈 모두 설치됩니다.

> [!NOTE]
> Azure 클래식 배포 모델을 사용하는 경우 `Azure` 모듈만 사용합니다.

Azure PowerShell을 사용하여 작업을 시작 하려면 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet을 사용하여 현재 PowerShell 세션에 `AzureRM`을 로드한 후 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

모든 새 PowerShell 세션에 대해 이러한 단계를 반복해야 합니다. `AzureRM` 모듈을 자동으로 가져오려면 PowerShell 프로필을 설정해야 하며, 프로필 설정은 [프로필 정보](/powershell/module/microsoft.powershell.core/about/about_profiles)에서 알아볼 수 있습니다.
Azure 로그인을 세션 간에 유지하는 방법을 알아보려면 [PowerShell 세션 간에 사용자 자격 증명 유지](context-persistence.md)를 참조합니다.
