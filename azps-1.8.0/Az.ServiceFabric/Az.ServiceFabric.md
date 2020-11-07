---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93688875"
---
# <span data-ttu-id="8e0c6-101">Az ServiceFabric 모듈</span><span class="sxs-lookup"><span data-stu-id="8e0c6-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="8e0c6-102">설명은</span><span class="sxs-lookup"><span data-stu-id="8e0c6-102">Description</span></span>
<span data-ttu-id="8e0c6-103">보안 클러스터 만들기, 클러스터 인증서를 통해 롤링, 클러스터에서 노드 추가 또는 제거 등의 엔드-2-엔드 작업을 자동화 하는 데 사용할 수 있는 Azure Service Fabric 모듈입니다. 모든 작업의 전체 목록은 아래에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="8e0c6-104">Az ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e0c6-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="8e0c6-105">추가-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="8e0c6-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="8e0c6-106">클러스터를 구성 하는 가상 컴퓨터 크기 집합에 새 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="8e0c6-107">인증서는 응용 프로그램 인증서로 사용 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="8e0c6-108">추가-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8e0c6-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="8e0c6-109">클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="8e0c6-110">추가-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8e0c6-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="8e0c6-111">클러스터에 보조 클러스터 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="8e0c6-112">추가-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="8e0c6-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="8e0c6-113">클러스터의 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="8e0c6-114">추가-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="8e0c6-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="8e0c6-115">기존 클러스터에 새 노드 형식을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="8e0c6-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8e0c6-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="8e0c6-117">클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="8e0c6-118">새로운 AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8e0c6-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="8e0c6-119">이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="8e0c6-120">제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="8e0c6-121">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="8e0c6-122">제거-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8e0c6-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="8e0c6-123">클라이언트 인증에 사용 되지 않는 클라이언트 인증서 또는 인증서 주체 이름 (s)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="8e0c6-124">제거-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8e0c6-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="8e0c6-125">클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="8e0c6-126">제거-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="8e0c6-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="8e0c6-127">클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="8e0c6-128">제거-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="8e0c6-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="8e0c6-129">클러스터에서 전체 노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="8e0c6-130">제거-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="8e0c6-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="8e0c6-131">클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="8e0c6-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="8e0c6-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="8e0c6-133">하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="8e0c6-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="8e0c6-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="8e0c6-135">클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="8e0c6-136">업데이트-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="8e0c6-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="8e0c6-137">클러스터의 노드 형식에 대 한 내구성 계층 또는 VmSku를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="8e0c6-138">업데이트-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="8e0c6-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="8e0c6-139">클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-139">Update the reliability tier of the primary node type in a cluster.</span></span>

