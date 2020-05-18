---
title: Azure PowerShell을 설치하는 다른 방법 | Microsoft Docs
description: MSI 패키지 또는 웹 플랫폼 설치 관리자를 사용하여 Azure PowerShell을 설치하는 방법입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: c0ac4f6cfb803519b8dd711d3cca0d4a4f7e6f8b
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722461"
---
# <a name="other-installation-methods"></a>다른 설치 방법

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell에는 여러 설치 방법이 있습니다. PowerShell 갤러리와 PowerShellGet을 사용하는 것이 좋습니다. Azure PowerShell은 웹 플랫폼 설치 관리자(WebPI)를 사용하거나 GitHub에서 사용할 수 있는 MSI 파일을 사용하여 Windows에 설치할 수 있습니다.

## <a name="install-on-windows-using-the-web-platform-installer"></a>웹 플랫폼 설치 관리자를 사용하여 Windows에 설치

WebPI에서 최신 Azure PowerShell을 설치하는 것은 이전 버전과 같습니다.
[Azure PowerShell WebPI 패키지](https://aka.ms/webpi-azps)를 다운로드하고 설치를 시작합니다.

> [!NOTE]
> 이전에 PowerShell 갤러리에서 Azure 모듈을 설치한 경우에는 설치 관리자가 해당 모듈을 자동으로 제거합니다. 한 가지 버전의 Azure PowerShell을 설치하여 사용자 환경을 단순화합니다. 그러나 여러 버전이 동시에 설치된 시나리오가 있습니다.
>
> PowerShell 갤러리 모듈은 `$env:ProgramFiles\WindowsPowerShell\Modules`에서 모듈을 설치합니다. 반면, WebPI 설치 관리자는 `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`에서 Azure 모듈을 설치합니다.
>
> 설치 중에 오류가 발생하는 경우 `$env:ProgramFiles\WindowsPowerShell\Modules` 폴더에서 Azure \*폴더를 수동으로 제거한 다음 다시 설치하면 됩니다.

설치가 완료되면 `$env:PSModulePath` 설정에는 Azure PowerShell cmdlet이 들어 있는 디렉터리가 포함되어야 합니다. 다음 명령을 사용하여 Azure PowerShell이 제대로 설치되어 있는지 확인할 수 있습니다.

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> WebPI에서 설치할 때 발생할 수 있는 알려진 문제가 있습니다. 시스템 업데이트 또는 다른 설치로 인해 컴퓨터를 다시 시작해야 하는 경우 `$env:PSModulePath` 업데이트 과정에서 Azure PowerShell이 설치된 경로가 포함되지 않을 수 있습니다.

설치 후에 cmdlet을 로드하거나 실행하려고 할 때 다음과 같은 오류 메시지가 나타날 수 있습니다.

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

컴퓨터를 다시 시작하거나 정규화된 경로를 사용하는 모듈을 가져와서 이 오류를 해결할 수 있습니다. 다음은 그 예입니다.

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>MSI 패키지를 사용하여 Windows에 설치

Azure PowerShell은 [GitHub](https://github.com/Azure/azure-powershell/releases/latest)에서 사용할 수 있는 MSI 파일을 사용하여 설치할 수 있습니다. 이전 버전의 Azure 모듈이 설치된 경우 설치 관리자에서 자동으로 제거합니다. MSI 패키지는 `$env:ProgramFiles\WindowsPowerShell\Modules`에서 모듈을 설치하지만 특정 버전 폴더를 만들지는 않습니다.

