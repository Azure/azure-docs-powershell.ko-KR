---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522560"
---
# <span data-ttu-id="d98bd-101">ServiceFabric 모듈 AzureRM</span><span class="sxs-lookup"><span data-stu-id="d98bd-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="d98bd-102">설명은</span><span class="sxs-lookup"><span data-stu-id="d98bd-102">Description</span></span>
<span data-ttu-id="d98bd-103">보안 클러스터 만들기, 클러스터 인증서를 통해 롤링, 클러스터에서 노드 추가 또는 제거 등의 엔드-2-엔드 작업을 자동화 하는 데 사용할 수 있는 Azure Service Fabric 모듈입니다. 모든 작업의 전체 목록은 아래에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d98bd-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="d98bd-104">ServiceFabric Cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="d98bd-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="d98bd-105">추가-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="d98bd-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="d98bd-106">응용 프로그램 인증서로 사용할 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d98bd-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="d98bd-107">추가-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d98bd-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="d98bd-108">클라이언트 인증을 위한 클러스터 설정에 일반 이름 또는 지문 추가</span><span class="sxs-lookup"><span data-stu-id="d98bd-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="d98bd-109">추가-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d98bd-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="d98bd-110">클러스터에 보조 클러스터 인증서를 추가 하 여 기존 인증서로 롤링</span><span class="sxs-lookup"><span data-stu-id="d98bd-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="d98bd-111">추가-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d98bd-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="d98bd-112">특정 노드 형식에 노드/Vm을 클러스터에 추가</span><span class="sxs-lookup"><span data-stu-id="d98bd-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="d98bd-113">추가-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="d98bd-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="d98bd-114">기존 클러스터에 노드 형식/Vm 추가</span><span class="sxs-lookup"><span data-stu-id="d98bd-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="d98bd-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d98bd-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="d98bd-116">클러스터 리소스에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d98bd-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="d98bd-117">새로운 AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d98bd-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="d98bd-118">새 ServiceFabric 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d98bd-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="d98bd-119">이 명령에는 다양 한 시나리오를 다루는 오버 로드가 여러 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d98bd-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="d98bd-120">제거-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d98bd-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="d98bd-121">클러스터에 액세스 하는 데 사용 되는 클라이언트 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="d98bd-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="d98bd-122">제거-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d98bd-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="d98bd-123">클러스터 보안에 사용 되지 않도록 클러스터 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="d98bd-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="d98bd-124">제거-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d98bd-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="d98bd-125">클러스터에서 특정 노드 유형에 서 노드 제거</span><span class="sxs-lookup"><span data-stu-id="d98bd-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="d98bd-126">제거-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="d98bd-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="d98bd-127">클러스터에서 노드 유형 제거</span><span class="sxs-lookup"><span data-stu-id="d98bd-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="d98bd-128">제거-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d98bd-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="d98bd-129">클러스터에서 하나 이상의 ServiceFabric 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d98bd-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="d98bd-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d98bd-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="d98bd-131">하나 이상의 ServiceFabric 설정을 클러스터에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d98bd-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="d98bd-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="d98bd-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="d98bd-133">클러스터의 ServiceFabric 업그레이드 유형 변경</span><span class="sxs-lookup"><span data-stu-id="d98bd-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="d98bd-134">업데이트-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="d98bd-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="d98bd-135">클러스터의 영속성 계층 변경</span><span class="sxs-lookup"><span data-stu-id="d98bd-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="d98bd-136">업데이트-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="d98bd-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="d98bd-137">클러스터의 안정성 계층 변경</span><span class="sxs-lookup"><span data-stu-id="d98bd-137">Change the reliability tier of a cluster</span></span>
