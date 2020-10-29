---
title: Azure PowerShell Service Management 모듈 설치 및 구성 | Microsoft Docs
description: Azure PowerShell을 처음으로 설치하고 구성하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2860d5c7642b137c1cb14a38fa13d59ec2a4123c
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523209"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Azure PowerShell Service Management 모듈 설치

[PowerShell 갤러리](https://www.powershellgallery.com/)에서 Azure PowerShell을 설치하는 것이 기본적인 설치 방법입니다.

## <a name="step-1-install-powershellget"></a>1단계: PowerShellGet 설치

PowerShell 갤러리에서 항목을 설치하려면 PowerShellGet 모듈이 필요합니다. 적절한 버전의 PowerShellGet 및 다른 시스템 요구 사항이 있는지 확인합니다. PowerShellGet이 시스템에 설치되어 있는지 확인하려면 다음 명령을 실행합니다.

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

다음과 비슷하게 표시됩니다.

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

PowerShellGet을 설치하지 않은 경우 [PowerShellGet을 가져오는 방법](#how-to-get-powershellget)을 참조하세요.

## <a name="step-2-install-azure-powershell"></a>2단계: Azure PowerShell 설치

관리자 권한으로 실행하는 Windows PowerShell 콘솔에서 다음 명령을 실행합니다.

```powershell
Install-Module Azure
```

Azure 모듈은 Azure Resource Manager cmdlet의 롤업 모듈입니다. AzureRM 모듈을 설치하는 경우 이전에 설치되지 않은 다른 Azure 모듈을 PowerShell 갤러리에서 다운로드하고 설치합니다.

Azure Service Management 모듈은 Azure PowerShell Resource Manager 모듈을 사용하여 종속성을 공유합니다. Azure PowerShell Resource Manager 모듈을 설치한 경우 `-AllowClobber` 매개 변수를 설치 명령에 추가해야 합니다. 이렇게 하면 이 기존 공유 종속성을 업데이트합니다. 이 매개 변수가 없으면 모듈을 설치하지 못합니다.

```powershell
Install-Module Azure -AllowClobber
```

이 모듈을 설치한 후에 다음 명령을 실행하여 모듈을 가져올 수 있습니다.

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>cmdlet을 사용하려면

Azure Service Management cmdlet을 사용하려면 먼저 Azure 계정에 로그인합니다. 계정에 로그인하려면 이제 다음 명령을 실행합니다.

```powershell
Add-AzureAccount
```

Azure PowerShell에서는 Azure에 로그인한 후에 지정된 세션에 대한 컨텍스트를 만듭니다. 해당 컨텍스트는 해당 세션 내에서 모든 cmdlet에 사용할 Azure PowerShell 환경, 계정, 테넌트 및 구독을 포함합니다. 이제 아래의 모듈을 사용할 준비가 완료되었습니다.

## <a name="azure-service-management-cmdlets"></a>Azure Service Management cmdlet

Azure PowerShell 모듈은 자주 업데이트됩니다. 모듈에 있지 않은 cmdlet 또는 매개 변수가 온라인 cmdlet 도움말에 포함되는 경우 최신 버전의 모듈을 다운로드하고 설치합니다. 모듈의 버전을 찾으려면 `(Get-InstalledModule Azure).Version`을 입력합니다.

Azure에서 일반적인 일부 작업을 자동화할 수 있는 샘플 스크립트는 [Windows Azure 스크립트 센터](http://www.windowsazure.com/documentation/scripts/)를 참조하세요.

Windows PowerShell을 설치, 학습, 사용 및 사용자 지정하는 방법에 대한 일반적인 정보는 [Windows PowerShell을 사용하여 스크립팅](/powershell/scripting/learn/ps101/00-introduction)을 참조하세요.

### <a name="how-to-get-powershellget"></a>PowerShellGet을 가져오는 방법

|OS 버전|설치 지침|
|---|---|
|Windows 10 또는 Windows Server 2016을 사용합니다.|OS에 포함된 WMF(Windows Management Framework) 5.0으로 빌드됩니다.|
|PowerShell 5로 업그레이드하려고 합니다.|[최신 버전의 WMF 설치](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a>Azure PowerShell 버전 확인

가능한 한 빨리 최신 버전으로 업그레이드하는 것이 좋지만 여러 버전의 Azure PowerShell이 지원됩니다. 설치한 Azure PowerShell의 버전을 확인하려면 명령줄에서 `Get-InstalledModule Azure`을 실행합니다.

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
