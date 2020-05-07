---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053318"
---
# <a name="azure-stack-module-160"></a>Azure Stack 모듈 1.6.0

## <a name="requirements"></a>요구 사항:
최소 지원 Azure Stack 버전은 1811입니다.

참고: 이전 버전을 사용하는 경우 1.6.0 버전을 설치하세요.

## <a name="install"></a>설치
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>릴리스 정보
* 1811 업데이트 지원
* Azs.Compute.Admin 모듈
    * New-DataDiskObject에 대한 Azs 접두사가 수정되고 향후 사용되지 않을 것이라는 경고와 함께 별칭이 추가되었습니다.
* Azs.Update.Admin 모듈
    * Install-AzsUpdate 실행 전에 Test-AzureStack에 대해 경고를 추가하는 것이 좋습니다.
* Azs.Fabric.Admin
    * 새 cmdlet(기능은 Azure Stack 1811 이상에서 지원됨)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * 사용 중단
        * Get-AzsInfrastructureVolume은 이제 Get-AzsVolume cmdlet에 대한 별칭입니다.
* Azs.InfrastructureInsights.Admin
    *  새 cmdlet Repair-AzsAlert 추가
* Azs.Storage.Admin
    * 기본 할당량 값이 사용되지 않는 버그 수정
* Azs.Subscriptions.Admin 모듈
    * New-AddonPlanDefinitionObject에 대한 Azs 접두사가 수정되고 향후 사용되지 않을 것이라는 경고와 함께 별칭이 추가되었습니다.
