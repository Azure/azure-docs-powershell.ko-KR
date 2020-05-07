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
# <a name="azure-stack-module-180"></a><span data-ttu-id="f4d27-103">Azure Stack 모듈 1.8.0</span><span class="sxs-lookup"><span data-stu-id="f4d27-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d27-104">요구 사항:</span><span class="sxs-lookup"><span data-stu-id="f4d27-104">Requirements:</span></span>

<span data-ttu-id="f4d27-105">지원되는 최소 Azure Stack 버전은 1910입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="f4d27-106">참고: 이전 버전의 Azure Stack인 경우 [Azure Stack Powershell 설치](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="f4d27-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="f4d27-107">설치</span><span class="sxs-lookup"><span data-stu-id="f4d27-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="f4d27-108">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="f4d27-108">Release Notes</span></span>

* <span data-ttu-id="f4d27-109">1910 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="f4d27-109">Supported with 1910 update</span></span>
* <span data-ttu-id="f4d27-110">변경 내용은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-110">Changes include:</span></span>

    - <span data-ttu-id="f4d27-111">**새 DRP 관리 모듈**: DRP(배포 리소스 공급자)를 사용하여 Azure Stack Hub에 대한 리소스 공급자 오케스트레이션 배포를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="f4d27-112">이러한 명령은 Azure Resource Manager 레이어와 상호 작용하여 DRP와 상호 작용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="f4d27-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="f4d27-113">**BRP**:</span></span>
        - <span data-ttu-id="f4d27-114">Azure 스택 인프라 백업에 대한 단일 역할 복원을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="f4d27-115">cmdlet R`estore-AzsBackup`에 `RoleName` 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="f4d27-116">**FRP**: API 버전 2019-05-01을 사용하는 **드라이브** 및 **볼륨** 리소스의 호환성이 손상되는 변경입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="f4d27-117">기능은 Azure Stack 1910 이상에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="f4d27-118">ID 값, `Name`, `HealthStatus` 및 `OperationalStatus`가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="f4d27-119">**드라이브** 리소스에 새 속성 `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` 및 `StoragePool`이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4d27-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="f4d27-120">**드라이브** 리소스의 `CanPool` 및 `CannotPoolReason` 속성은 더 이상 사용되지 않습니다. `OperationalStatus`를 대신 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="f4d27-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
