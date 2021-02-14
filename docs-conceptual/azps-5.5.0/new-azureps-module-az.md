---
title: Azure Az PowerShell 모듈 소개
description: Azure와 상호 작용하는 데 권장되는 모듈이자 AzureRM PowerShell 모듈을 대체하는 Az PowerShell 모듈을 소개합니다.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 9021a1d8fdc73aedb87b17631f8e67cb8ef79166
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012036"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Azure Az PowerShell 모듈 소개

## <a name="overview"></a>개요

Az PowerShell 모듈은 PowerShell에서 직접 Azure 리소스를 관리하기 위한 cmdlet 세트입니다. PowerShell은 Azure 리소스를 관리(예: CI/CD 파이프라인)하는 데 활용할 수 있는 강력한 자동화 기능을 제공합니다.

Az PowerShell 모듈은 AzureRM을 대체하며 Azure와 상호 작용하는 데 권장되는 버전입니다.

다음 방법 중 하나로 Az PowerShell 모듈을 사용할 수 있습니다.

* [PowerShellGet을 통해 Az PowerShell 모듈을 설치합니다](install-az-ps.md)(권장 옵션).
* [MSI를 통해 Az PowerShell 모듈을 설치합니다](install-az-ps-msi.md).
* [Azure Cloud Shell을 사용합니다](/azure/cloud-shell/overview).
* [Az PowerShell Docker 컨테이너를 사용합니다](azureps-in-docker.md).

## <a name="features"></a>기능

Az PowerShell 모듈은 다음과 같은 이점을 제공합니다.

* 보안 및 안정성
  * 토큰 캐시 암호화
  * 중간자(man-in-the-middle) 공격 유형 방지
  * ADFS 2019를 사용한 인증 지원
  * PowerShell 7의 사용자 이름 및 암호 인증
  * 연속 액세스 평가와 같은 기능 지원(2021년에 도입 예정)
* 모든 Azure 서비스 지원
  * 일반적으로 사용 가능한 모든 Azure 서비스에는 각각의 지원 PowerShell 모듈이 있습니다.
  * AzureRM 이후 여러 버그 수정 및 API 버전 업그레이드
* 새로운 기능
  * Cloud Shell 및 플랫폼 간 지원
  * 액세스 토큰을 가져와서 Azure 리소스에 액세스하는 데 사용 가능
  * Azure 리소스를 사용하여 고급 REST 작업에 사용할 수 있는 cmdlet

> [!NOTE]
> 모든 플랫폼에서 Az PowerShell과 함께 사용할 것을 권장하는 PowerShell 버전은 PowerShell 7 이상입니다.

Az PowerShell 모듈은 .NET Standard 라이브러리를 기반으로 하며 Windows, macOS 및 Linux를 비롯한 모든 플랫폼에서 PowerShell 7 이상과 함께 작동합니다. Windows PowerShell 5.1과도 호환됩니다.

저희는 모든 플랫폼에 Azure 지원을 제공하고 모든 Az PowerShell 모듈이 모든 플랫폼에서 작동할 수 있도록 최선을 다하고 있습니다.

## <a name="upgrade-your-environment-to-az"></a>현재 환경을 Az로 업그레이드

PowerShell의 최신 Azure 기능을 계속 유지하려면 Az 모듈로 마이그레이션해야 합니다. AzureRM에 대한 대체 모듈로 Az 모듈을 설치할 준비가 되지 않았으면 Az를 사용하여 실험할 수 있는 몇 가지 옵션이 있습니다.

* [Azure Cloud Shell](/azure/cloud-shell/overview)이 있는 `PowerShell` 환경을 사용합니다. Azure Cloud Shell은 Az 모듈이 설치되고 `Enable-AzureRM` 호환성 별칭을 사용하도록 설정된 상태로 제공되는 브라우저 기반 셸 환경입니다.
* Windows PowerShell 5.1에서 설치한 AzureRM 모듈을 그대로 두고 PowerShell 7 이상에서 Az 모듈을 설치하세요. Windows PowerShell 5.1과 PowerShell 7 이상은 별도의 모듈 컬렉션을 사용합니다. 지침에 따라 [최신 버전의 PowerShell](/powershell/scripting/install/installing-powershell)을 설치한 다음, PowerShell 7 이상에서 [Az 모듈을 설치](install-az-ps.md)합니다.

기존 AzureRM 설치에서 업그레이드하려면 다음을 수행합니다.

1. [Azure PowerShell AzureRM 모듈 제거](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Azure PowerShell Az 모듈 설치](install-az-ps.md)
1. **선택 사항**: 새 명령 집합을 습득하면서 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias)를 사용하여 AzureRM cmdlet에 대한 별칭을 추가할 수 있는 호환성 모드를 사용하도록 설정합니다. 자세한 내용은 다음 섹션 또는 [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)을 참조하세요.

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>기존 스크립트를 AzureRM에서 Az로 마이그레이션

스크립트가 여전히 AzureRM 모듈을 기반으로 하는 분들을 위해 마이그레이션에 도움이 되는 다음과 같은 몇 가지 리소스를 준비해 두었습니다.

* [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)
* [AzureRM에서 Az 1.0.0으로의 호환성이 손상되는 변경 전체 목록](migrate-az-1.0.0.md)
* [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet

## <a name="supportability"></a>지원 가능성

Az는 가장 최신 버전의 Azure용 PowerShell 모듈입니다. 문제 또는 기능 요청은 [GitHub 리포지토리](https://github.com/Azure/azure-powershell)에서 직접 기록할 수 있습니다. 또는 지원 계약을 맺은 경우에는 Microsoft 지원을 통해 기록할 수 있습니다. 기능 요청은 최신 버전의 Az에서 구현됩니다. 중요한 문제는 Az의 마지막 두 개 버전에서 구현됩니다.

AzureRM은 더 이상 새 cmdlet 또는 기능을 받지 않습니다. 그러나 AzureRM 모듈은 여전히 공식적으로 유지 관리되며 2021년 2월까지 중요한 수정이 이루어집니다.

## <a name="data-collection"></a>데이터 수집

Azure PowerShell은 기본적으로 원격 분석 데이터를 수집합니다. Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고, Azure PowerShell 환경을 개선시킵니다.
Microsoft Azure PowerShell은 프라이빗 또는 개인 데이터를 수집하지 않습니다. 예를 들어 사용 데이터는 성공률이 낮은 cmdlet과 같은 문제를 식별하고 작업의 우선 순위를 지정하는 데 도움이 됩니다.

이 데이터가 제공하는 인사이트가 많은 도움이 되지만, 사용 데이터를 제공하는 데 찬성하지 않는 분들도 있다는 것을 잘 알고 있습니다. [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet을 사용하여 데이터 수집을 사용하지 않도록 설정할 수 있습니다. [개인정보처리방침](https://privacy.microsoft.com/privacystatement)에서 자세한 내용을 확인할 수 있습니다.
