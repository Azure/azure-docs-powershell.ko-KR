---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264413"
---
# <a name="azure-stack-module-180"></a>Azure Stack 모듈 1.8.0

## <a name="requirements"></a>요구 사항:

지원되는 최소 Azure Stack 버전은 1910입니다.

참고: 이전 버전의 Azure Stack인 경우 [Azure Stack Powershell 설치](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)를 확인하세요.

## <a name="install"></a>설치

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>릴리스 정보

* 1910 업데이트 지원
* 변경 내용은 다음과 같습니다.

    - **새 DRP 관리 모듈**: DRP(배포 리소스 공급자)를 사용하여 Azure Stack Hub에 대한 리소스 공급자 오케스트레이션 배포를 수행할 수 있습니다. 이러한 명령은 Azure Resource Manager 레이어와 상호 작용하여 DRP와 상호 작용합니다.

    - **BRP**:
        - Azure 스택 인프라 백업에 대한 단일 역할 복원을 지원합니다.
        - cmdlet R`estore-AzsBackup`에 `RoleName` 매개 변수를 추가합니다.

    - **FRP**: API 버전 2019-05-01을 사용하는 **드라이브** 및 **볼륨** 리소스의 호환성이 손상되는 변경입니다. 기능은 Azure Stack 1910 이상에서 지원됩니다.
        - ID 값, `Name`, `HealthStatus` 및 `OperationalStatus`가 변경되었습니다.
        - **드라이브** 리소스에 새 속성 `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` 및 `StoragePool`이 지원됩니다.
        - **드라이브** 리소스의 `CanPool` 및 `CannotPoolReason` 속성은 더 이상 사용되지 않습니다. `OperationalStatus`를 대신 사용하세요.
