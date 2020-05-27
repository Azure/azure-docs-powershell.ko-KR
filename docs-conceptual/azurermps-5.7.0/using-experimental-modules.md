---
title: 실험적 Azure PowerShell 모듈 사용
description: 실험적 Azure PowerShell 모듈의 기본 원칙 및 사용을 이해합니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: 9cd88919b51f24d19579b865d9f3d5cc779b62d9
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534791"
---
# <a name="using-experimental-azure-powershell-modules"></a>실험적 Azure PowerShell 모듈 사용

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell 팀은 Azure의 개발자 도구(특히 CLI)에 중점을 두고 Azure PowerShell 환경에 많은 향상된 기능을 실험하고 있습니다.

## <a name="experimentation-methodology"></a>실험적 방법론

실험을 용이하게 하기 위해 기존 Azure SDK 기능을 새롭고 사용하기에 더 쉬운 방법으로 구현하는 새 Azure PowerShell 모듈을 만들었습니다. 대부분의 경우에서 cmdlet은 기존 cmdlet을 정확하게 반영합니다. 단, 실험적 cmdlet은 Azure 리소스를 더 쉽게 만들고 관리할 수 있도록 약식 표기와 더 스마트한 기본값을 제공합니다.

이러한 모듈은 기존 Azure PowerShell 모듈과 함께 설치할 수 있습니다. cmdlet 이름은 더 짧은 이름을 제공하여 이름이 기존의 실험용이 아닌 cmdlet과 상충하는 것을 방지하기 위해 더 짧아졌습니다.

실험적 모듈은 다음 명명 규칙을 사용합니다. `AzureRM.*.Experiments` 이 명명 규칙은 미리 보기 모듈의 이름 지정인 `AzureRM.*.Preview`와 비슷합니다. 미리 보기 모듈은 실험적 모듈과는 다릅니다. 미리 보기 모듈은 미리 보기 제품으로만 사용할 수 있는 Azure 서비스의 새로운 기능을 구현합니다. 미리 보기 모듈은 기존 Azure PowerShell 모듈을 대신하며 동일한 cmdlet 및 매개 변수 이름을 사용합니다.

## <a name="how-to-install-an-experimental-module"></a>실험적 모듈 설치 방법

실험적 모듈은 기존 Azure PowerShell 모듈과 마찬가지로 PowerShell 갤러리에 게시됩니다. 실험적 모듈 목록을 보려면 다음 명령을 실행하십시오.

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

실험적 모듈을 설치하려면 관리자 권한 PowerShell 세션에서 다음 명령을 사용합니다.

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>설명서 및 지원

설명서는 설치 패키지에 포함되어 있으며 `Get-Help` cmdlet을 사용하여 액세스됩니다. 실험적 모듈에 대한 공식 설명서는 게시되지 않습니다.

이러한 모듈을 테스트하는 것이 좋습니다. 기능성을 개선하고 사용자의 요구에 응답할 수 있도록 사용자 의견을 보내주세요. 단, 실험을 위해 이러한 모듈에 대한 지원은 제한적입니다. GitHub 리포지토리에서 [문제](https://github.com/Azure/azure-powershell/issues)를 만들면 질문 또는 문제 보고서를 제출할 수 있습니다.

## <a name="experiments-and-areas-of-improvement"></a>향상된 기능의 실험 및 영역

이러한 향상된 기능은 경쟁 제품의 핵심적인 차이점을 기준으로 선택되었습니다. 예를 들어 Azure CLI 2.0은 _API 노출 영역_이 아닌 _시나리오_를 기준 명령으로 사용합니다.
Azure CLI 2.0은 최종 사용자가 더 쉽게 시나리오를 “시작”할 수 있도록 여러 스마트한 기본값을 사용합니다.

### <a name="core-improvements"></a>주요 향상된 기능

주요 향상된 기능은 “상식”으로 간주되며, 약간의 실험은 이러한 업데이트 구현을 진전시키기 위해 필요합니다.

- 시나리오 기반 cmdlet - <em>*모든</em> cmdlet은 Azure REST 서비스가 아닌 시나리오로 설계되어야 합니다.

- 더 짧은 이름 - cmdlet의 이름(예: `New-AzureRmVM` => `New-AzVm`) 및 매개 변수 이름(예: `-ResourceGroupName` => `-Rg`)를 포함합니다. “이전” cmdlet과의 호환성에 대한 별칭을 사용합니다. _이전 버전과 호환되는_ 매개 변수 집합을 제공합니다.

- 스마트한 기본값 - 스마트한 기본값을 만들어 “필요한” 정보를 채웁니다. 다음은 그 예입니다.
  - 리소스 그룹
  - 위치
  - 종속 리소스

### <a name="experimental-improvements"></a>실험적 향상된 기능

실험적 향상된 기능은 팀에서 실험을 통해 유효성을 검사하려는 중요한 변경 내용을 제공합니다.

- 단순 형식 - 복잡한 형식과 구성 개체는 피해서 시나리오를 만듭니다. 하나 또는 두 개의 매개 변수로 구성을 간소화합니다.

- “스마트한 만들기” - “스마트한 만들기”를 구현하는 모든 시나리오에는 매개 변수가 필요 _없습니다_. 모든 필수 정보는 Azure PowerShell에 의해 독자적으로 선택됩니다.

- 회색 매개 변수 - 대부분의 경우에서 일부 매개 변수는 “회색” 또는 반 선택적일 수 있습니다. 매개 변수가 지정되지 않은 경우 사용자에게 해당 항목에 대해 매개 변수를 생성할 것인지 묻는 메시지가 표시됩니다. 또한 사용자 동의 하에 회색 매개 변수가 컨텍스트를 기준으로 값을 유추하는 것이 적합합니다.
  예를 들어 회색 매개 변수가 최근 사용된 값을 제안하는 것이 적합할 수 있습니다.

- `-Auto` 스위치 - `-Auto` 스위치는 메인라인 경로에서 필수 매개 변수의 무결성을 유지 관리하는 동시에 사용자가 _모든 항목의 기본값을 설정_할 수 있는 “옵트인” 방식을 제공합니다.

### <a name="feature-specific-switches"></a>기능별 스위치

예를 들어 “웹앱 만들기” 시나리오에는 기존 git 리포지토리에 “azure” 원격을 자동으로 추가하는 `-Git` 또는 `-AddRemote` 스위치가 있을 수 있습니다.

- 설정 가능한 기본값 - 사용자는 `-ResourceGroupName` 및 `-Location`과 같은 특정 유비쿼터스 매개 변수의 기본값을 설정할 수 있어야 합니다.

- 크기 기본값 - 리소스 “크기”는 다양한 리소스 제공자가 서로 다른 이름을 사용하기 때문에 사용자가 혼란스러울 수 있습니다(예: “Standard\_DS1\_v2” 또는 “S1”). 그러나 대부분의 사용자는 비용에 더 민감합니다. 따라서 가격 책정 일정에 따라 “범용” 크기를 정의하는 것이 적합합니다. 사용자가 특정 크기를 정할 수도 있고, 아니면 Azure PowerShell에서 리소스 예산에 따라 _최상의 옵션_을 선택하도록 할 수도 있습니다.

- 출력 형식 - Azure PowerShell은 현재 `PSObject`를 반환하고 약간의 콘솔 출력이 있습니다. Azure PowerShell은 “스마트한 기본값” 사용에 관해 사용자에게 몇 가지 정보를 표시해야 할 수도 있습니다.
