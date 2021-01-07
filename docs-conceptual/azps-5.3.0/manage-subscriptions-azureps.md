---
title: Azure PowerShell을 사용하여 Azure 구독 관리
description: Azure PowerShell을 사용하여 Azure 구독 관리
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 4f48e009d9769cba671ea54e8f619a9ad40603d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893854"
---
# <a name="use-multiple-azure-subscriptions"></a>여러 Azure 구독 사용

대부분의 Azure 사용자는 단일 구독만 가집니다. 그러나, 사용자가 여러 조직에 속해 있거나 또는 여러 그룹에 걸친 특정 리소스에 액세스하기 위해 조직이 분할된 경우 Azure 내에서 여러 구독을 가질 수 있습니다. CLI는 전역적으로 그리고 명령 당 구독을 선택하는 것을 지원합니다.

구독, 청구 및 비용 관리에 대한 자세한 내용은 [청구 및 비용 관리 설명서](/azure/billing/)를 참조하세요.

## <a name="tenants-users-and-subscriptions"></a>테넌트, 사용자 및 구독

Azure 내에서 테넌트, 사용자 및 구독 간의 차이에 대해 약간의 혼동이 있을 수 있습니다. _테넌트_ 는 전체 조직을 포괄하는 Azure Active Directory 엔터티입니다. 이 테넌트에는 하나 이상의 _구독_ 및 _사용자_ 가 있습니다. 사용자는 개인이며 소속된 조직인 테넌트 하나와만 연결됩니다. 사용자는 Azure에 로그인하여 리소스를 생성, 관리, 사용하는 계정입니다.
사용자는 Azure를 포함하여 클라우드 서비스를 사용하기로 Microsoft와 계약한 여러 _구독_ 에 액세스할 수 있습니다. 모든 리소스가 구독과 연결됩니다.

테넌트, 사용자 및 구독 간의 차이점에 대한 자세한 내용은 [Azure 클라우드 용어 사전](/azure/azure-glossary-cloud-terminology)을 참조하세요.  새 구독을 Azure Active Directory 테넌트에 추가하는 방법을 알아보려면 [Azure 구독을 Azure Active Directory 테넌트에 연결 또는 추가하는 방법](/azure/active-directory/active-directory-how-subscriptions-associated-directory)을 참조하세요.
특정 테넌트에 로그인하는 방법을 알아보려면 [Azure PowerShell로 로그인](/powershell/azure/authenticate-azureps)을 참조하세요.

## <a name="change-the-active-subscription"></a>활성 구독 변경

Azure PowerShell에서 구독 리소스에 액세스하려면, 현재 Azure 세션과 연결되어있는 구독을 변경해야 합니다.
활성 세션 컨텍스트, 즉 어떤 테넌트, 구독 및 사용자 cmdlet이 실행되어야 하는지에 대한 정보를 수정하면 됩니다.
구독을 변경하려면 먼저 Azure PowerShell 컨텍스트 개체를 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription)으로 검색한 다음, 현재 컨텍스트를 [Set-AzContext](/powershell/module/az.accounts/set-azcontext)로 바꾸어야 합니다.

다음 예제는 현재 활성 상태인 테넌트에서 구독하는 방법과 이를 활성 세션으로 설정하는 방법을 보여줍니다.

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

컨텍스트를 저장하는 방법이나 다양한 구독으로 작업하기 쉽도록 컨텍스트를 빠르게 전환하는 방법 등 Azure PowerShell 컨텍스트에 대해 더 자세히 알아보려면, [Azure PowerShell 컨텍스트로 자격 증명 유지하기](context-persistence.md)를 참조하세요.
