---
title: Azure PowerShell을 설치하는 다른 방법
description: PowerShellGet을 사용하지 않고 MSI를 사용하여 Azure PowerShell을 설치하는 방법
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 82375cc4267f468f562d138c4cdec6131e34ae32
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534529"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>MSI로 Windows에 Azure PowerShell 설치

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

이 문서에서는 MSI를 사용하여 Azure PowerShell을 Windows에 설치하는 방법에 대해 설명합니다.  
시스템에 필요한 경우에만 이러한 설치 방법을 사용합니다. Windows에 Azure PowerShell 설치에는 PowerShellGet을 사용하는 방법이 권장됩니다. PowerShellGet을 사용하여 Azure PowerShell을 설치하는 방법은 [PowerShellGet으로 Azure PowerShell 설치하기](install-azurerm-ps.md)를 참조합니다.

> [!NOTE]
> 웹 플랫폼 설치 관리자 설치 방법은 Azure PowerShell 6.x 이상 버전에서는 더 이상 사용할 수 없습니다. 웹 플랫폼 설치 관리자를 사용해야 하는 경우에는 MSI를 대신 사용해 보세요. 또는 이전 버전의 Azure PowerShell을 설치할 수도 있습니다.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI 패키지를 사용하여 Windows에 설치 및 업데이트

Windows PowerShell 5.x용 Azure PowerShell은 [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)에서 사용할 수 있는 MSI 파일을 사용하여 설치할 수 있습니다. 이전 버전의 Azure 모듈이 MSI로 설치된 경우 설치 관리자에서 자동으로 제거합니다. MSI 패키지는 `${env:ProgramFiles}\WindowsPowerShell\Modules`에서 모듈을 설치합니다. `AzureRM` 및 `Azure` 모듈 모두 설치됩니다.

> [!NOTE]
> Azure 클래식 배포 모델을 사용하는 경우 `Azure` 모듈만 사용합니다.

Azure PowerShell을 사용하여 작업을 시작하려면 Azure 자격 증명으로 로그인합니다.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> 모듈 자동 로딩을 비활성화한 경우 `Import-Module AzureRM`을 사용하여 모듈을 수동으로 가져와야 합니다. 모듈 구조화 방식으로 인해 몇 초 정도 걸릴 수 있습니다.

모든 새 PowerShell 세션에 대해 이 단계를 반복해야 합니다. PowerShell 세션 간에 Azure 로그인을 유지하는 방법을 보려면 [PowerShell 세션간에 사용자 자격 증명 유지](context-persistence.md)를 참조하세요.
