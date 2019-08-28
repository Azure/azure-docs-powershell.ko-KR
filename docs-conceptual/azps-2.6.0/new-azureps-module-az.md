---
title: Azure PowerShell Az 모듈 소개
description: AzureRM 모듈을 대체하는 새로운 Azure PowerShell 모듈 Az을 소개합니다.
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 21d41b6e14d1b39a78e40daee74b80de3a80c2a0
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052603"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>새로운 Azure PowerShell Az 모듈 소개

2018년 12월부터 Azure PowerShell Az 모듈은 일반 릴리스로 출시되며 이는 Azure와 상호 작용하기 위한 PowerShell 모듈입니다. Az는 짧아진 명령과 향상된 안정성을 제공하며, 여러 플랫폼을 지원합니다. Az는 또한 AzureRM과 기능 패리티를 가지고 있어 간편한 마이그레이션 경로를 제공합니다.

Az 모듈을 사용하면 이제 Azure PowerShell이 Windows의 PowerShell 5.1과 호환되며, Windows, macOS 및 Linux를 포함하여 지원되는 모든 플랫폼의 PowerShell Core 6.x 이상과 호환됩니다.

Az는 새로운 모듈이기 때문에 버전이 1.0.0으로 다시 설정되었습니다.

## <a name="why-a-new-module"></a>새 모듈인 이유는?

주요 업데이트는 불편할 수 있으므로 PowerShell의 Azure와 상호 작용할 수 있는 새 cmdlet이 포함된 새 모듈 세트를 도입하기로 결정한 이유를 알 수 있도록 해야 합니다.

가장 크고 중요한 변화는 PowerShell이 [PowerShell Core 6.x](/powershell/scripting/overview)가 도입된 이후 .NET Standard 라이브러리에 기반한 여러 플랫폼에서 사용할 수 있는 제품이 되었다는 것입니다.
Azure 지원을 모든 플랫폼에 제공하기 위해 노력하고 있습니다. 즉 .NET Standard를 사용하고 PowerShell Core와 호환되도록 Azure PowerShell 모듈을 업데이트해야 합니다. 기존 AzureRM 모듈을 사용하고 이러한 지원을 추가하기 위해 복잡한 변경을 도입하는 대신 Az 모듈을 만들었습니다.

또한 새 모듈을 만듦으로써 엔지니어가 cmdlet 및 모듈의 디자인과 이름 지정을 일관되게 유지할 수 있게 되었습니다. 이제 모든 모듈이 `Az.` 접두사로 시작하고, 모든 cmdlet에서 _동사_-`Az`_명사_ 형식을 사용합니다. 이전에는 cmdlet 이름이 더 길었을 뿐만 아니라 cmdlet 이름이 일치하지 않았습니다.

모듈 수도 감소했습니다. 동일한 서비스에서 작동한 일부 모듈은 롤백되었으며, 관리 평면 및 데이터 평면 cmdlet은 이제 해당 서비스용 단일 모듈 내에 모두 포함됩니다. 종속성 및 가져오기를 수동으로 관리하는 사용자에게는 이 작업이 훨씬 간단해집니다.

팀에서 새 Azure PowerShell 모듈을 구축하는 데 필요한 중요한 작업을 변경함으로써 그 어느 때보다 훨씬 쉽고, 더 많은 플랫폼에서 PowerShell cmdlet을 통해 Azure를 사용할 수 있도록 노력했습니다.

## <a name="upgrade-to-az"></a>Az로 업그레이드

PowerShell의 최신 Azure 기능을 계속 유지하려면 가능한 한 빨리 Az 모듈로 마이그레이션해야 합니다. AzureRM에 대한 대체 모듈로 Az 모듈을 설치할 준비가 되지 않았으면 Az를 사용하여 실험할 수 있는 몇 가지 옵션이 있습니다.

* [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview)이 있는 `PowerShell` 환경을 사용합니다.
  Azure Cloud Shell은 Az 모듈이 설치되고 `Enable-AzureRM` 호환성 별칭을 사용하도록 설정된 브라우저 기반 셸 환경입니다.
* Windows용 PowerShell 5.1과 함께 설치된 AzureRM 모듈을 유지하는 한편, PowerShell Core 6.x 이상용 Az 모듈도 설치합니다. Windows용 PowerShell 5.1과 PowerShell Core는 별도의 모듈 모음을 사용합니다. [PowerShell Core 설치](/powershell/scripting/install/installing-powershell-core-on-windows) 지침을 수행한 다음, PowerShell Core 터미널에서 [Az 모듈을 설치](install-az-ps.md)합니다.

기존 AzureRM 설치에서 업그레이드하려면 다음을 수행합니다.

1. [Azure PowerShell AzureRM 모듈 제거](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Azure PowerShell Az 모듈 설치](install-az-ps.md)
3. __선택 사항__: 새 명령 집합을 습득하면서 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias)를 사용하여 AzureRM cmdlet에 대한 별칭을 추가할 수 있는 호환성 모드를 사용하도록 설정합니다. 자세한 내용은 다음 섹션 또는 [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)을 참조하세요.

## <a name="migrate-existing-scripts-to-az"></a>기존 스크립트를 Az로 마이그레이션

새로운 cmdlet 이름은 쉽게 익힐 수 있도록 되었습니다. cmdlet 이름에 `AzureRm` 또는 `Azure`를 사용하는 대신 `Az`를 사용합니다. 예를 들어, 이전 명령 `New-AzureRMVm`은 `New-AzVm`이 됩니다.
마이그레이션은 단순히 새 cmdlet 이름을 습득하는 것 이상입니다. 이름이 바뀐 모듈, 매개 변수 및 기타 중요한 변경이 있습니다.

AzureRM에서 Az로 마이그레이션하는 프로세스를 지원하기 위해 다음과 같이 다양한 리소스를 갖추고 있습니다.

* [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)
* [AzureRM에서 Az 1.0.0으로의 호환성이 손상되는 변경 전체 목록](migrate-az-1.0.0.md)
* [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet

Az 모듈에는 새 구문으로 업데이트하는 동안 기존 스크립트를 사용할 수 있게 하는 호환성 모드가 있습니다. [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet은 별칭을 통해 호환성 모드를 사용하도록 설정하여 Az로의 전체 마이그레이션을 수행하는 동안 최소한의 수정으로 기존 스크립트를 사용할 수 있게 합니다.

> [!IMPORTANT]
> cmdlet 이름이 별칭으로 지정되어 있더라도 여전히 Az cmdlet에 대한 새(또는 이름이 바뀐) 매개 변수가 있거나 반환 값이 변경되었을 수 있습니다. 별칭을 사용하도록 설정하여 마이그레이션을 처리할 것으로 기대하지 마세요! 업데이트가 필요할 수 있는 스크립트의 위치를 찾으려면 [호환성이 손상되는 변경 전체 목록](migrate-az-1.0.0.md)을 참조하세요.

## <a name="continued-support-for-azurerm"></a>지속적인 AzureRM 지원

AzureRM은 더 이상 새 cmdlet 또는 기능을 받지 않습니다. 그러나 AzureRM 모듈은 여전히 공식적으로 유지되며 2020년 12월까지 버그 수정도 이루어집니다.