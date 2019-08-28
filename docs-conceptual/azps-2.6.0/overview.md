---
title: Azure PowerShell 개요
description: 설치 방법 및 시작 방법에 대한 정보가 담긴 Azure PowerShell Az 모듈의 개요입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052620"
---
# <a name="overview-of-azure-powershell"></a>Azure PowerShell 개요

Azure PowerShell은 Azure 리소스를 관리하기 위해 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 모델을 사용하는 cmdlet 집합을 제공합니다. Azure PowerShell은.NET 표준을 사용하여 Windows, macOS 및 Linux에서 사용할 수 있습니다.
Azure PowerShell은 Azure Cloud Shell에서도 사용할 수 있습니다.

## <a name="about-the-new-az-module"></a>새 Az 모듈 정보

이 설명서에서는 Azure PowerShell을 위한 새 Az 모듈을 설명합니다. 이 새 모듈은.NET 표준으로 처음부터 작성됩니다. .NET Standard를 사용하면 Azure PowerShell을 Windows의 PowerShell 5.1 또는 모든 플랫폼의 PowerShell Core 6.x 이상에서 실행할 수 있습니다. Az 모듈은 이제 PowerShell을 통해 Azure와 상호 작용하도록 의도된 방법입니다.
AzureRM의 버그 수정은 계속되지만, 새로운 기능은 더 이상 받지 않습니다.

[Azure PowerShell Az 모듈 소개](new-azureps-module-az.md)에서 명령의 이름이 변경된 내용과 AzureRM의 유지 관리 계획을 포함하여 새 모듈에 대한 자세한 내용을 확인할 수 있습니다. 지금 바로 새 모듈을 사용하여 시작하려는 경우 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조합니다.

[AzureRM 설명서](/powershell/azure/azurerm)도 제공됩니다.

> [!IMPORTANT]
>
> Azure 설명서가 새로운 모듈 cmdlet 이름을 반영하도록 업데이트되는 동안 아티클은 여전히 AzureRM 명령을 사용할 수 있습니다. Az 모듈을 설치한 후 `Enable-AzureRmAlias`를 사용하여 AzureRM cmdlet 별칭을 사용하도록 하는 것이 좋습니다. 자세한 내용은 [AzureRM에서 Az로 마이그레이션](migrate-from-azurerm-to-az.md)을 참조하세요.

## <a name="run-or-install"></a>실행 또는 설치

Azure PowerShell은 Windows의 PowerShell 5.1 이상 및 모든 플랫폼의 PowerShell Core 6.x 이상에 설치하거나 Azure Cloud Shell에서 실행할 수 있습니다.

* Azure Cloud Shell을 사용하여 브라우저에서 실행하려면 [Azure Cloud Shell에서 PowerShell 빠른 시작](/azure/cloud-shell/quickstart-powershell)을 참조하세요.
* 시스템에 Azure PowerShell을 설치하려면 [Azure PowerShell 설치](install-az-ps.md)를 참조합니다.

Azure PowerShell 최신 릴리스에 대한 자세한 내용은 [릴리스 정보](release-notes-azureps.md)를 참조하세요.

## <a name="get-started"></a>시작

[Azure PowerShell 시작하기](get-started-azureps.md) 아티클을 읽고 Azure PowerShell 기본 사항을 배워보세요. PowerShell에 대해 익숙하지 않으면 소개가 도움이 될 수 있습니다.

* [PowerShell 설치](/powershell/scripting/install/installing-powershell)
* [PowerShell 스크립팅](/powershell/scripting/powershell-scripting)
* [PowerShell 기본 사항: (파트 1)PowerShell 시작](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

다음 예제는 Azure의 일반적인 사용법을 알려줍니다.

* [Linux Virtual Machines](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Windows Virtual Machines](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Microsoft Learn을 통해 기술 쌓기

- [PowerShell을 사용하여 스크립트로 Azure 작업 자동화](/learn/modules/automate-azure-tasks-with-powershell/)
- [더 많은 대화형 학습 보기...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>다른 Azure PowerShell 모듈

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
