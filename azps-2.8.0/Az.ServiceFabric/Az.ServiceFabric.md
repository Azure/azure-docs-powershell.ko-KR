---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93689066"
---
# <span data-ttu-id="fb045-101">Az ServiceFabric 모듈</span><span class="sxs-lookup"><span data-stu-id="fb045-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="fb045-102">설명은</span><span class="sxs-lookup"><span data-stu-id="fb045-102">Description</span></span>
<span data-ttu-id="fb045-103">보안 클러스터 만들기, 클러스터 인증서를 통해 롤링, 클러스터에서 노드 추가 또는 제거 등의 엔드-2-엔드 작업을 자동화 하는 데 사용할 수 있는 Azure Service Fabric 모듈입니다. 모든 작업의 전체 목록은 아래에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="fb045-104">Az ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb045-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="fb045-105">추가-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb045-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="fb045-106">클러스터를 구성 하는 가상 컴퓨터 크기 집합에 새 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="fb045-107">인증서는 응용 프로그램 인증서로 사용 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="fb045-108">추가-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb045-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="fb045-109">클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="fb045-110">추가-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb045-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="fb045-111">클러스터에 보조 클러스터 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="fb045-112">추가-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="fb045-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="fb045-113">클러스터의 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="fb045-114">추가-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fb045-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="fb045-115">기존 클러스터에 새 노드 형식을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="fb045-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb045-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="fb045-117">서비스 패브릭 응용 프로그램 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="fb045-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb045-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="fb045-119">서비스 패브릭 응용 프로그램 유형 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="fb045-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb045-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="fb045-121">서비스 패브릭 응용 프로그램 유형 버전 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="fb045-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fb045-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="fb045-123">클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="fb045-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb045-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="fb045-125">지정 된 응용 프로그램 및 클러스터 아래에서 서비스 패브릭 서비스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="fb045-126">새로운 AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb045-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="fb045-127">지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="fb045-128">새로운 AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb045-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="fb045-129">지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램 종류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="fb045-130">새로운 AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb045-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="fb045-131">지정 된 리소스 그룹 및 클러스터 아래에 새 응용 프로그램 종류 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="fb045-132">새로운 AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fb045-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="fb045-133">이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="fb045-134">제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="fb045-135">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="fb045-136">새로운 AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb045-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="fb045-137">지정 된 응용 프로그램 및 클러스터 아래에 새 service fabric 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="fb045-138">제거-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb045-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="fb045-139">클러스터에서 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-139">Remove an application from the cluster.</span></span> <span data-ttu-id="fb045-140">이렇게 하면 응용 프로그램 아래에 있는 서비스가 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="fb045-141">제거-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb045-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="fb045-142">서비스 패브릭 제거 클러스터의 응용 프로그램 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="fb045-143">이 리소스 아래에 모든 유형의 버전이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="fb045-144">제거-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb045-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="fb045-145">서비스 패브릭 제거 클러스터의 응용 프로그램 유형 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="fb045-146">제거-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb045-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="fb045-147">클라이언트 인증에 사용 되지 않는 클라이언트 인증서 또는 인증서 주체 이름 (s)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="fb045-148">제거-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb045-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="fb045-149">클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="fb045-150">제거-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="fb045-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="fb045-151">클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="fb045-152">제거-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fb045-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="fb045-153">클러스터에서 전체 노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="fb045-154">제거-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb045-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="fb045-155">클러스터에서 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="fb045-156">제거-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="fb045-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="fb045-157">클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="fb045-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="fb045-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="fb045-159">하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="fb045-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="fb045-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="fb045-161">클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="fb045-162">업데이트-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb045-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="fb045-163">서비스 패브릭 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-163">Update a service fabric application.</span></span> <span data-ttu-id="fb045-164">이렇게 하면 응용 프로그램 매개 변수를 업데이트 하 고 응용 프로그램 업그레이드를 트리거할 응용 프로그램 유형 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="fb045-165">업데이트-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="fb045-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="fb045-166">클러스터의 노드 형식에 대 한 내구성 계층 또는 VmSku를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="fb045-167">업데이트-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="fb045-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="fb045-168">클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb045-168">Update the reliability tier of the primary node type in a cluster.</span></span>

