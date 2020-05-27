---
title: Azure PowerShell 설치 및 구성 | Microsoft Docs
description: Azure PowerShell을 처음으로 설치하고 구성하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 6f894546364e6a5ae06e1915a166edb258ccc698
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386751"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>PowerShellGet으로 Azure PowerShell을 설치

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

이 아티클에서는 PowerShellGet을 사용하여 Windows용 PowerShell 5.x용 Azure PowerShell 모듈을 설치하는 단계를 설명합니다. PowerShellGet 및 모듈 관리는 Azure PowerShell을 설치하는 더 좋은 방법이지만 대신 웹 플랫폼 설치 관리자 또는 MSI 패키지로 설치하려는 경우 [다른 설치 방법](other-install.md)을 참조합니다.

Azure 클래식 배포 모델은 본 버전의 Azure PowerShell에서 지원되지 않습니다. 클래식 배포에 대한 지원은 [Azure PowerShell Service Management 모듈 설치](/powershell/azure/servicemanagement/install-azure-ps) 지침을 참조합니다.

> [!IMPORTANT]
> MacOS 또는 Linux 용 AzureRM 모듈은 지원되지 않습니다. 이러한 플랫폼에서 Azure PowerShell cmdlet을 사용하려면 [Az 모듈을 설치](/powershell/azure/install-az-ps)합니다.

## <a name="step-1-install-powershellget"></a>1단계: PowerShellGet 설치

PowerShell 갤러리에서 항목을 설치하려면 PowerShellGet 모듈이 필요합니다. 적절한 버전의 PowerShellGet 및 다른 시스템 요구 사항이 있는지 확인합니다. PowerShellGet이 시스템에 설치되어 있는지 확인하려면 다음 명령을 실행합니다.


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

다음과 비슷하게 표시됩니다.

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

PowerShellGet 버전 1.1.2.0 이상이 필요합니다. PowerShellGet을 업데이트하려면 다음 명령을 사용합니다.

```powershell-interactive
Install-Module PowerShellGet -Force
```

PowerShellGet을 설치하지 않은 경우 이 문서의 [PowerShellGet을 가져오는 방법](#how-to-get-powershellget) 섹션을 참조하세요.

> [!NOTE]
> PowerShellGet을 사용하려면 스크립트를 실행할 수 있게 하는 실행 정책이 필요합니다. PowerShell의 실행 정책에 대한 자세한 내용은 [실행 정책 정보](/powershell/module/microsoft.powershell.core/about/about_execution_policies)(영문)를 참조하세요.
>
> [!IMPORTANT]
> 이 문서에서 설명된 모듈인 AzureRM에서는 .NET Framework를 사용합니다. 이렇게 하면 .NET Core를 사용하는 PowerShell 6.0과 호환되지 않습니다. PowerShell 6.0을 사용하는 경우, [macOS 및 Linux에 대한 설치 지침](install-azurermps-maclinux.md)을 따릅니다.

## <a name="step-2-install-azure-powershell"></a>2단계: Azure Powershell 설치

PowerShell 갤러리에서 Azure PowerShell을 설치하려면 상승된 권한이 필요합니다. 상승된 PowerShell 세션에서 다음 명령을 실행합니다.

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

기본적으로 PowerShell 갤러리는 PowerShellGet에 대한 신뢰할 수 있는 리포지토리로 구성되지 않습니다. PSGallery를 처음 사용할 때는 다음과 같은 메시지가 표시됩니다.

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

설치를 계속하려면 'Yes' 또는 'Yes to All'로 답변합니다.

> [!NOTE]
> NuGet 2.8.5.201 이전 버전을 사용하는 경우 최신 버전의 NuGet을 다운로드하여 설치하라는 메시지가 표시됩니다.

AzureRM 모듈은 Azure Resource Manager cmdlet의 롤업 모듈입니다. AzureRM 모듈을 설치하는 경우 이전에 설치되지 않은 Azure PowerShell 모듈이 PowerShell 갤러리에서 다운로드되고 설치됩니다.

이전 버전의 Azure PowerShell이 설치된 경우 오류가 나타날 수 있습니다. 이 문제를 해결하려면 이 문서의 [새 Azure PowerShell 버전으로 업데이트](#update-azps) 섹션을 참조하세요.

## <a name="step-3-load-the-azurerm-module"></a>3단계: AzureRM 모듈 로드

모듈이 설치되면 PowerShell 세션에 모듈을 로드해야 합니다. 이 작업은 일반(권한이 상승되지 않은) PowerShell 세션에서 수행해야 합니다. 모듈은 다음과 같이 `Import-Module` cmdlet을 사용하여 로드됩니다.

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>다음 단계

Azure PowerShell을 사용하는 방법에 대한 자세한 내용은 다음 문서를 참조하세요.

* [Azure PowerShell 시작](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>문제 보고 및 피드백

도구에서 버그가 발견되면 GitHub 리포지토리의 [문제](https://github.com/Azure/azure-powershell/issues) 섹션에 문제를 기록해 주세요. 명령줄에서 피드백을 제공하려면 `Send-Feedback` cmdlet을 사용해 보세요.

## <a name="frequently-asked-questions"></a>질문과 대답

### <a name="how-to-get-powershellget"></a>PowerShellGet을 가져오는 방법

|OS 버전|설치 지침|
|---|---|
|Windows 10 또는 Windows Server 2016을 사용합니다.|OS에 포함된 WMF(Windows Management Framework) 5.0으로 빌드됩니다.|
|PowerShell 5로 업그레이드하려고 합니다.|[최신 버전의 WMF 설치](https://www.microsoft.com/download/details.aspx?id=54616)|
|PowerShell 3 또는 PowerShell 4를 사용하는 Windows 버전에서 실행됩니다.|[PackageManagement 모듈 가져오기](https://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/>Azure PowerShell 버전 확인

가능한 한 빨리 최신 버전으로 업그레이드하는 것이 좋지만 여러 버전의 Azure PowerShell이 지원됩니다. 설치한 Azure PowerShell의 버전을 확인하려면 명령줄에서 `Get-InstalledModule AzureRM`을 실행합니다.

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>클래식 배포 방법에 대한 지원

클래식 배포 모델을 사용하는 배포가 있는 경우 Azure PowerShell의 Service Management 버전을 설치할 수 있습니다. 자세한 내용은 [Azure PowerShell Service Management 모듈 설치](/powershell/azure/servicemanagement/install-azure-ps)를 참조하세요. Azure 모듈과 AzureRM 모듈은 공통 종속성을 공유합니다. Azure와 AzureRM 모듈을 둘 다 사용하는 경우 각 패키지의 동일한 버전을 설치해야 합니다.

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/>새 Azure PowerShell 버전으로 업데이트

서비스 관리 모듈을 포함하는 이전 버전의 Azure PowerShell이 설치되어 있는 경우 다음과 같은 오류가 나타날 수 있습니다.

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

이 오류 메시지에 나오는 것처럼 -AllowClobber 매개 변수를 사용해서 모듈을 설치해야 합니다. 다음 명령을 사용합니다.

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

자세한 내용은 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module)에 대한 도움말 항목을 참조하세요.

### <a name="installing-module-versions-side-by-side"></a>단계별 모듈 버전 설치

PowerShellGet 설치 방법은 여러 버전의 설치를 지원하는 유일한 방법입니다. 예를 들어 업데이트할 시간이나 리소스가 없는 이전 버전의 Azure PowerShell을 사용하여 작성한 스크립트가 있을 수 있습니다. 다음 명령에서는 여러 버전의 Azure PowerShell을 설치하는 방법을 보여 줍니다.

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

PowerShell 세션에서 한 버전의 모듈만 로드할 수 있습니다. 새 PowerShell 창을 열고 `Import-Module`을 사용하여 특정 버전의 AzureRM cmdlet을 가져와야 합니다.

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> 2\.1.0 버전 및 1.2.6 버전은 나란히 설치하여 사용하도록 설계된 첫 번째 모듈 버전입니다. 이전 버전의 Azure PowerShell을 로드하는 경우는 호환되지 않는 **AzureRM.Profile** 모듈 버전이 로드됩니다. 그 결과 cmdlet을 실행할 때마다 로그인하라는 메시지가 표시됩니다.

### <a name="other-installation-methods"></a>다른 설치 방법

웹 플랫폼 설치 관리자 또는 MSI 패키지를 사용하여 설치하는 방법에 대한 자세한 내용은 [다른 설치 방법](other-install.md)을 참조하세요.
