---
title: Azure PowerShell 시작
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c60036ba8be6282007aa34a0bb9c0d9e33197072
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657674"
---
# <a name="get-started-with-azure-powershell"></a>Azure PowerShell 시작

Azure PowerShell은 명령줄에서 Azure 리소스를 관리하기 위해 설계되었습니다. Azure Resource Manager 모델을 사용하는 자동화된 도구를 만들려는 경우 Azure PowerShell을 사용하세요.
[Azure Cloud Shell](/azure/cloud-shell/overview)과 함께 브라우저에서 사용하거나 로컬 컴퓨터에 설치하여 사용해 보세요.

이 문서에서는 Azure PowerShell을 시작하는 방법 및 핵심 개념을 설명합니다.

## <a name="install-or-run-in-azure-cloud-shell"></a>Azure Cloud Shell에서 설치 또는 실행

Azure PowerShell을 시작하는 가장 쉬운 방법은 Azure Cloud Shell 환경에서 시도하는 것입니다.
Azure Cloud Shell을 실행하려면 [Azure Cloud Shell에서 PowerShell 빠른 시작](/azure/cloud-shell/quickstart-powershell)을 참조하세요.
Cloud Shell은 Linux 컨테이너에서 PowerShell 6을 실행하므로 Windows 관련 기능을 사용할 수 없습니다.

로컬 컴퓨터에 Azure PowerShell을 설치할 준비가 되면 [Azure PowerShell 모듈 설치](install-az-ps.md)의 지침을 따릅니다.

## <a name="sign-in-to-azure"></a>Azure에 로그인

`Connect-AzAccount` cmdlet을 사용하여 대화형으로 로그인합니다. Cloud Shell을 사용하는 경우 이 단계를 건너뜁니다. Azure Cloud Shell 세션은 Cloud Shell 세션을 시작한 환경, 구독 및 테넌트에 대해 이미 인증되었습니다.

```azurepowershell-interactive
Connect-AzAccount
```

미국 이외 지역의 경우 `-Environment` 매개 변수를 사용하여 로그인합니다. [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet을 사용하여 해당 지역의 환경 이름을 가져옵니다. 예를 들어, Azure 중국 21Vianet에 로그인하려면 다음을 수행합니다.

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

사용 하는 토큰을 얻게 https://microsoft.com/devicelogin 합니다. 브라우저에서 이 페이지를 열고 토큰을 입력하여 Azure 계정 자격 증명으로 로그인하고 Azure PowerShell을 승인하세요. 

로그인하면 어떤 Azure 구독이 활성화되어 있는지 나타내는 정보가 나타납니다. 계정에 Azure 구독이 여러 개 있고 다른 항목을 선택하려면 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription)을 사용하여 사용 가능한 구독을 가져오고 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet을 구독 ID와 함께 사용하세요.
Azure PowerShell에서 Azure 구독을 관리하는 방법에 대한 자세한 내용은 [여러 Azure 구독 사용](manage-subscriptions-azureps.md)을 참조하세요.

Azure 계정에 로그인하면 Azure PowerShell cmdlet을 사용하여 구독에서 관리자 리소스에 액세스할 수 있습니다. 로그인 프로세스 및 인증 방법에 대한 자세한 내용은 [Azure PowerShell을 사용하여 로그인](authenticate-azureps.md)을 참조합니다.

## <a name="find-commands"></a>명령 찾기

Azure PowerShell cmdlet은 PowerShell을 위한 표준 명명 규칙인 `VERB-NOUN`을 따릅니다. 동사는 작업(예: `New`,`Get`,`Set`,`Remove`)을 설명하고 명사는 리소스 종류를 설명합니다(예:`AzVM`,`AzKeyVaultCertificate`,`AzFirewall`,`AzVirtualNetworkGateway`). Azure PowerShell에서 명사는 항상 접두사 `Az`를 사용하여 시작합니다. 표준 동사의 전체 목록은 [PowerShell 명령에 대한 승인된 동사](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands)를 참조합니다.

사용 가능한 명사, 동사 및 Azure PowerShell 모듈을 알면 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet을 사용하여 명령을 찾을 수 있습니다. 예를 들어 `Get` 동사를 사용하는 VM 관련 명령을 모두 찾으려면 다음을 수행합니다.

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

일반 명령을 찾는 데 도움이 되도록 이 표에는 리소스 종류, 해당 Azure PowerShell 모듈 및 `Get-Command`와 함께 사용할 명사 접두사가 나열되어 있습니다.

| 리소스 종류 | Azure PowerShell 모듈 | 명사 접두사 |
|---------------|-------------------------|----------------|
| [리소스 그룹](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [가상 머신](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [스토리지 계정](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [Key Vault](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [웹 애플리케이션](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [SQL 데이터베이스](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

Azure PowerShell의 모듈 전체 목록은 GitHub에서 호스팅되는 [Azure PowerShell 모듈 목록](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)을 참조하세요.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>빠른 시작 및 자습서로 Azure PowerShell 기본 내용 학습

Azure PowerShell을 시작하려면 가상 머신 설정 및 쿼리 방법에 대한 심층적인 자습서를 참조해 보세요.

> [!div class="nextstepaction"]
> [Azure PowerShell로 가상 머신 만들기](azureps-vm-tutorial.yml)

기타 인기 Azure 서비스에 대한 Azure PowerShell 빠른 시작도 있습니다.

* [스토리지 계정을 만드는](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Azure Blob Storage 간에 개체 전송](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Azure Key Vault에서 비밀을 만들고 검색](/azure/key-vault/quick-create-powershell)
* [Azure SQL 데이터베이스 및 방화벽 만들기](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Azure Container Instances의 컨테이너 실행](/azure/container-instances/container-instances-quickstart-powershell)
* [가상 머신 확장 집합 만들기(VMSS)](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [표준 부하 분산 장치 만들기](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>다음 단계

* [Azure PowerShell로 로그인](authenticate-azureps.md)
* [Azure PowerShell을 사용하여 Azure 구독 관리](manage-subscriptions-azureps.md)
* [Azure PowerShell로 서비스 주체 만들기](create-azure-service-principal-azureps.md)
* 커뮤니티에서 도움말을 가져옵니다.
  * [MSDN의 azure 포럼](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [스택 오버플로](http://go.microsoft.com/fwlink/?LinkId=320213)
