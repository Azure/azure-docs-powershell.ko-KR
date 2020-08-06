---
title: Azure PowerShell 시작
description: ''
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.openlocfilehash: c0b8ab83052bbe069abe170955f9409eca2118d6
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566316"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="a4177-102">Azure PowerShell 시작</span><span class="sxs-lookup"><span data-stu-id="a4177-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="a4177-103">Azure PowerShell은 명령줄에서 Azure 리소스를 관리하기 위해 설계되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span>
<span data-ttu-id="a4177-104">Azure Resource Manager 모델을 사용하는 자동화된 도구를 만들려는 경우 Azure PowerShell을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span> <span data-ttu-id="a4177-105">[Azure Cloud Shell](/azure/cloud-shell/overview)과 함께 브라우저에서 사용하거나 로컬 컴퓨터에 설치하여 사용해 보세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="a4177-106">이 문서에서는 Azure PowerShell을 시작하는 방법 및 핵심 개념을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="a4177-107">Azure Cloud Shell에서 설치 또는 실행</span><span class="sxs-lookup"><span data-stu-id="a4177-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="a4177-108">Azure PowerShell을 시작하는 가장 쉬운 방법은 Azure Cloud Shell 환경에서 시도하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span> <span data-ttu-id="a4177-109">Azure Cloud Shell을 실행하려면 [Azure Cloud Shell에서 PowerShell 빠른 시작](/azure/cloud-shell/quickstart-powershell)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span> <span data-ttu-id="a4177-110">Cloud Shell은 Linux 컨테이너에서 PowerShell을 실행하므로 Windows 관련 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-110">Cloud Shell runs PowerShell on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="a4177-111">로컬 컴퓨터에 Azure PowerShell을 설치할 준비가 되면 [Azure PowerShell 모듈 설치](install-az-ps.md)의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="a4177-112">Azure에 로그인</span><span class="sxs-lookup"><span data-stu-id="a4177-112">Sign in to Azure</span></span>

<span data-ttu-id="a4177-113">[Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet을 사용하여 대화형으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-113">Sign in interactively with the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span> <span data-ttu-id="a4177-114">Cloud Shell을 사용하는 경우 이 단계를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-114">Skip this step if you use Cloud Shell.</span></span> <span data-ttu-id="a4177-115">Azure Cloud Shell 세션은 Cloud Shell 세션을 시작한 환경, 구독 및 테넌트에 대해 이미 인증되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-115">Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="a4177-116">Azure 클라우드 서비스는 지역 데이터 처리법을 준수하는 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-116">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="a4177-117">지역 클라우드의 계정의 경우 **Environment** 매개 변수를 사용하여 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-117">For accounts in a regional cloud, use the **Environment** parameter to sign in.</span></span> <span data-ttu-id="a4177-118">[Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet을 사용하여 해당 지역의 환경 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-118">Get the name of the environment for your region using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span>
<span data-ttu-id="a4177-119">예를 들어, Azure 중국 21Vianet에 로그인하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-119">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="a4177-120">Windows PowerShell 5.1 환경에서는 Azure 계정의 사용자 이름 및 암호를 제공하는 로그인 대화 상자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-120">In Windows PowerShell 5.1 environments, you'll receive a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="a4177-121">다른 모든 버전의 PowerShell에서는 [microsoft.com/devicelogin](https://microsoft.com/devicelogin)에서 사용할 토큰이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-121">On every other version of PowerShell, you'll get a token to use on [microsoft.com/devicelogin](https://microsoft.com/devicelogin).</span></span> <span data-ttu-id="a4177-122">브라우저에서 이 페이지를 열고 토큰을 입력하여 Azure 계정 자격 증명으로 로그인하고 Azure PowerShell을 승인하세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-122">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="a4177-123">로그인하면 어떤 Azure 구독이 활성화되어 있는지 나타내는 정보가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-123">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="a4177-124">계정에 Azure 구독이 여러 개 있고 다른 항목을 선택하려면 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription)을 사용하여 사용 가능한 구독을 가져오고 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet을 구독 ID와 함께 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-124">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span> <span data-ttu-id="a4177-125">Azure PowerShell에서 Azure 구독을 관리하는 방법에 대한 자세한 내용은 [여러 Azure 구독 사용](manage-subscriptions-azureps.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-125">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="a4177-126">Azure 계정에 로그인하면 Azure PowerShell cmdlet을 사용하여 구독에서 관리자 리소스에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-126">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="a4177-127">로그인 프로세스 및 인증 방법에 대한 자세한 내용은 [Azure PowerShell을 사용하여 로그인](authenticate-azureps.md)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-127">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="a4177-128">명령 찾기</span><span class="sxs-lookup"><span data-stu-id="a4177-128">Find commands</span></span>

<span data-ttu-id="a4177-129">Azure PowerShell cmdlet은 PowerShell을 위한 표준 명명 규칙인 `Verb-Noun`을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-129">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `Verb-Noun`.</span></span> <span data-ttu-id="a4177-130">동사는 작업(예: `New`,`Get`,`Set`,`Remove`)을 설명하고 명사는 리소스 종류를 설명합니다(예:`AzVM`,`AzKeyVaultCertificate`,`AzFirewall`,`AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="a4177-130">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="a4177-131">Azure PowerShell에서 명사는 항상 접두사 `Az`를 사용하여 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-131">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="a4177-132">표준 동사의 전체 목록은 [PowerShell 명령에 대한 승인된 동사](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands)를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-132">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="a4177-133">사용 가능한 명사, 동사 및 Azure PowerShell 모듈을 알면 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet을 사용하여 명령을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-133">Knowing the nouns, verbs, and the Azure PowerShell modules available helps you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="a4177-134">예를 들어 `Get` 동사를 사용하는 VM 관련 명령을 모두 찾으려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-134">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="a4177-135">일반 명령을 찾는 데 도움이 되도록 이 표에는 리소스 종류, 해당 Azure PowerShell 모듈 및 `Get-Command`와 함께 사용할 명사 접두사가 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-135">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

|                              <span data-ttu-id="a4177-136">리소스 유형</span><span class="sxs-lookup"><span data-stu-id="a4177-136">Resource type</span></span>                              |                   <span data-ttu-id="a4177-137">Azure PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="a4177-137">Azure PowerShell module</span></span>                    |    <span data-ttu-id="a4177-138">명사 접두사</span><span class="sxs-lookup"><span data-stu-id="a4177-138">Noun prefix</span></span>     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [<span data-ttu-id="a4177-139">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="a4177-139">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="a4177-140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a4177-140">Az.Resources</span></span>](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [<span data-ttu-id="a4177-141">가상 머신</span><span class="sxs-lookup"><span data-stu-id="a4177-141">Virtual machines</span></span>](/azure/virtual-machines)                             | [<span data-ttu-id="a4177-142">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a4177-142">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [<span data-ttu-id="a4177-143">스토리지 계정</span><span class="sxs-lookup"><span data-stu-id="a4177-143">Storage accounts</span></span>](/azure/storage/common/storage-introduction)          | [<span data-ttu-id="a4177-144">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a4177-144">Az.Storage</span></span>](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [<span data-ttu-id="a4177-145">Key Vault</span><span class="sxs-lookup"><span data-stu-id="a4177-145">Key Vault</span></span>](/azure/key-vault/key-vault-whatis)                          | [<span data-ttu-id="a4177-146">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a4177-146">Az.KeyVault</span></span>](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [<span data-ttu-id="a4177-147">웹 애플리케이션</span><span class="sxs-lookup"><span data-stu-id="a4177-147">Web applications</span></span>](/azure/app-service)                                  | [<span data-ttu-id="a4177-148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a4177-148">Az.Websites</span></span>](/powershell/module/az.websites)                | `AzWebApp`         |
| [<span data-ttu-id="a4177-149">SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a4177-149">SQL databases</span></span>](/azure/sql-database)                                    | [<span data-ttu-id="a4177-150">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a4177-150">Az.Sql</span></span>](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

<span data-ttu-id="a4177-151">Azure PowerShell의 모듈 전체 목록은 GitHub에서 호스팅되는 [Azure PowerShell 모듈 목록](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-151">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="telemetry"></a><span data-ttu-id="a4177-152">원격 분석</span><span class="sxs-lookup"><span data-stu-id="a4177-152">Telemetry</span></span>

<span data-ttu-id="a4177-153">Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-153">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="a4177-154">Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고 Azure PowerShell 환경을 향상시킵니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-154">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="a4177-155">Microsoft Azure PowerShell은 프라이빗 또는 개인 데이터를 수집하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-155">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="a4177-156">데이터 수집을 사용하지 않도록 하려면 [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection)을 실행하여 명시적으로 옵트아웃해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-156">To disable data collection, you must explicitly opt out by executing [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection).</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="a4177-157">빠른 시작 및 자습서로 Azure PowerShell 기본 내용 학습</span><span class="sxs-lookup"><span data-stu-id="a4177-157">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="a4177-158">Azure PowerShell을 시작하려면 가상 머신 설정 및 쿼리 방법에 대한 심층적인 자습서를 참조해 보세요.</span><span class="sxs-lookup"><span data-stu-id="a4177-158">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a4177-159">Azure PowerShell로 가상 머신 만들기</span><span class="sxs-lookup"><span data-stu-id="a4177-159">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="a4177-160">기타 인기 Azure 서비스에 대한 Azure PowerShell 빠른 시작도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-160">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="a4177-161">스토리지 계정을 만드는</span><span class="sxs-lookup"><span data-stu-id="a4177-161">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="a4177-162">Azure Blob Storage 간에 개체 전송</span><span class="sxs-lookup"><span data-stu-id="a4177-162">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="a4177-163">Azure Key Vault에서 비밀을 만들고 검색</span><span class="sxs-lookup"><span data-stu-id="a4177-163">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="a4177-164">Azure SQL 데이터베이스 및 방화벽 만들기</span><span class="sxs-lookup"><span data-stu-id="a4177-164">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="a4177-165">Azure Container Instances의 컨테이너 실행</span><span class="sxs-lookup"><span data-stu-id="a4177-165">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="a4177-166">Virtual Machine Scale Set 만들기</span><span class="sxs-lookup"><span data-stu-id="a4177-166">Create a Virtual Machine Scale Set</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="a4177-167">표준 부하 분산 장치 만들기</span><span class="sxs-lookup"><span data-stu-id="a4177-167">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="a4177-168">다음 단계</span><span class="sxs-lookup"><span data-stu-id="a4177-168">Next steps</span></span>

* [<span data-ttu-id="a4177-169">Azure PowerShell로 로그인</span><span class="sxs-lookup"><span data-stu-id="a4177-169">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="a4177-170">Azure PowerShell을 사용하여 Azure 구독 관리</span><span class="sxs-lookup"><span data-stu-id="a4177-170">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="a4177-171">Azure PowerShell로 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a4177-171">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="a4177-172">커뮤니티에서 도움말을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4177-172">Get help from the community:</span></span>
  * [<span data-ttu-id="a4177-173">MSDN의 azure 포럼</span><span class="sxs-lookup"><span data-stu-id="a4177-173">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="a4177-174">스택 오버플로</span><span class="sxs-lookup"><span data-stu-id="a4177-174">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
