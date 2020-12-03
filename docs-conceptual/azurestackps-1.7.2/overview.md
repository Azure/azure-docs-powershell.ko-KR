---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427380"
---
# <a name="azure-stack-module-172"></a>Azure Stack 모듈 1.7.2

## <a name="requirements"></a>요구 사항:

지원되는 최소 Azure Stack 버전은 1904입니다.

참고: 이전 버전의 Azure Stack인 경우 [Azure Stack Powershell 설치](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)를 확인하세요.

## <a name="install"></a>설치

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>릴리스 정보

* 1904 업데이트 지원
* 이는 호환성이 손상되는 변경 릴리스입니다. 호환성이 손상되는 변경에 대한 자세한 내용은 <https://aka.ms/azspshmigration170>를 참조하세요.
* 호환성이 손상되는 변경 내용: Backup이 인증서 기반 암호화 모드로 변경됩니다. 대칭 키에 대한 지원은 사용되지 않습니다.
* 호환성이 손상되는 변경에 대한 자세한 내용은 https://aka.ms/azspshmigration170를 참조하세요.
* Azs.Storage.Admin 모듈 
* 버그 수정 - 새 스토리지 할당량이 제공되지 않을 경우 기본값을 사용합니다.