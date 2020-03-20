---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: ef034424c72d88b3ceb28956da9ca56e4a7f3941
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402717"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="1460a-103">Azure Stack 모듈 1.8.1</span><span class="sxs-lookup"><span data-stu-id="1460a-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="1460a-104">요구 사항:</span><span class="sxs-lookup"><span data-stu-id="1460a-104">Requirements:</span></span>

<span data-ttu-id="1460a-105">지원되는 최소 Azure Stack 버전은 1910입니다.</span><span class="sxs-lookup"><span data-stu-id="1460a-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="1460a-106">참고: 이전 버전의 Azure Stack인 경우 [Azure Stack Powershell 설치](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="1460a-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="1460a-107">설치</span><span class="sxs-lookup"><span data-stu-id="1460a-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="1460a-108">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="1460a-108">Release Notes</span></span>

* <span data-ttu-id="1460a-109">1910 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="1460a-109">Supported with 1910 update</span></span>
