---
title: MSI로 Azure PowerShell 설치
description: PowerShellGet을 사용하지 않고 MSI를 사용하여 Azure PowerShell을 설치하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 9bb2a0d611c4cc39172fc6c51d375a1b47f834ed
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002982"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>MSI로 Windows에 Azure PowerShell 설치

이 문서에서는 MSI를 사용하여 Azure PowerShell을 Windows에 설치하는 방법에 대해 설명합니다. MSI 설치 관리자는 PowerShell 갤러리가 방화벽에 의해 차단될 수 있거나 오프라인 설치 관리자가 필요한 환경에 제공됩니다. Azure PowerShell 설치에는 PowerShellGet을 사용하는 방법이 권장됩니다. PowerShellGet을 사용하여 Azure PowerShell을 설치하는 방법은 [PowerShellGet으로 Azure PowerShell 설치하기](install-az-ps.md)를 참조합니다.

## <a name="requirements"></a>요구 사항

Azure PowerShell용 MSI 설치 관리자는 Windows의 PowerShell 5.1에 대해서__만__ 작동합니다. Windows가 아닌 플랫폼 또는 이후 버전의 PowerShell에 설치하려면 [PowerShellGet으로 설치](install-az-ps.md)합니다.
PowerShell 버전을 확인하려면 다음 명령을 실행합니다.

```powershell-interactive
$PSVersionTable.PSVersion
```

PowerShell 5.1에서 Azure PowerShell을 사용하려면 다음을 수행합니다.

1. 필요한 경우 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)로 업데이트합니다. Windows 10을 사용하는 경우 PowerShell 5.1이 이미 설치되어 있습니다.
2. [.NET Framework 4.7.2 이상](/dotnet/framework/install)을 설치합니다.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI 패키지를 사용하여 Windows에 설치 및 업데이트

Windows용 Azure PowerShell은 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v3.3.0-January2020)에서 사용할 수 있는 MSI 파일을 사용하여 설치됩니다. 이전 버전의 Azure 모듈이 MSI로 설치된 경우 설치 관리자에서 자동으로 제거합니다. MSI 패키지는 `${env:ProgramFiles}\WindowsPowerShell\Modules`에서 모듈을 설치합니다.

Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> 모듈 자동 로딩을 비활성화한 경우 `Import-Module Az`을 사용하여 모듈을 수동으로 가져와야 합니다. 모듈 구조화 방식으로 인해 최대 1분 정도 걸릴 수 있습니다.

모든 새 PowerShell 세션에 대해 이 단계를 반복해야 합니다. PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.

## <a name="provide-feedback"></a>피드백 제공

Azure Powershell에서 버그 발생 시, [ GitHub에서 문제를 제출](https://github.com/Azure/azure-powershell/issues)하세요.
명령줄에서 피드백을 제공하려면 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 사용해 보세요.

## <a name="next-steps"></a>다음 단계

Azure PowerShell 모듈 및 모듈의 기능에 대해 자세히 알아보려면, [Azure PowerShell 시작](get-started-azureps.md)을 참조하세요.
Azure PowerShell에 익숙하고 AzureRM에서 마이그레이션해야 하는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.
