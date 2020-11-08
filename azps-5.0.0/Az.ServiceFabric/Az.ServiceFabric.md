---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217022"
---
# <span data-ttu-id="ab8d6-101">Az ServiceFabric 모듈</span><span class="sxs-lookup"><span data-stu-id="ab8d6-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="ab8d6-102">설명은</span><span class="sxs-lookup"><span data-stu-id="ab8d6-102">Description</span></span>
<span data-ttu-id="ab8d6-103">보안 클러스터 만들기, 클러스터 인증서를 통해 롤링, 클러스터에서 노드 추가 또는 제거 등의 엔드-2-엔드 작업을 자동화 하는 데 사용할 수 있는 Azure Service Fabric 모듈입니다. 모든 작업의 전체 목록은 아래에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="ab8d6-104">Az ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab8d6-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="ab8d6-105">추가-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ab8d6-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="ab8d6-106">클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="ab8d6-107">추가-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ab8d6-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="ab8d6-108">클러스터에 보조 클러스터 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="ab8d6-109">추가-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ab8d6-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="ab8d6-110">인증서 일반 이름 또는 지문을 클러스터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="ab8d6-111">이렇게 하면 클라이언트 인증을 위해 agains 인증서가 클러스터에 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="ab8d6-112">추가-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="ab8d6-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="ab8d6-113">노드 형식에 vm 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="ab8d6-114">추가-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="ab8d6-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="ab8d6-115">노드 형식에 인증서 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="ab8d6-116">추가-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ab8d6-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="ab8d6-117">클러스터의 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="ab8d6-118">추가-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="ab8d6-119">기존 클러스터에 새 노드 형식을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="ab8d6-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab8d6-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="ab8d6-121">서비스 패브릭 응용 프로그램 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="ab8d6-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="ab8d6-123">서비스 패브릭 응용 프로그램 유형 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="ab8d6-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab8d6-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="ab8d6-125">서비스 패브릭 응용 프로그램 유형 버전 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="ab8d6-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ab8d6-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="ab8d6-127">클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="ab8d6-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="ab8d6-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="ab8d6-129">관리 되는 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="ab8d6-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="ab8d6-131">관리 노드 형식 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="ab8d6-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab8d6-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="ab8d6-133">지정 된 응용 프로그램 및 클러스터 아래에서 서비스 패브릭 서비스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="ab8d6-134">새로운 AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab8d6-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="ab8d6-135">지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="ab8d6-136">새로운 AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="ab8d6-137">지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램 종류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="ab8d6-138">새로운 AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab8d6-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="ab8d6-139">지정 된 리소스 그룹 및 클러스터 아래에 새 응용 프로그램 종류 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="ab8d6-140">새로운 AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ab8d6-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="ab8d6-141">이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="ab8d6-142">제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="ab8d6-143">자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="ab8d6-144">새로운 AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="ab8d6-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="ab8d6-145">새 관리 되는 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="ab8d6-146">새로운 AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="ab8d6-147">새 노드 형식 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-147">Create new node type resource.</span></span>

### [<span data-ttu-id="ab8d6-148">새로운 AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab8d6-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="ab8d6-149">지정 된 응용 프로그램 및 클러스터 아래에 새 service fabric 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="ab8d6-150">제거-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab8d6-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="ab8d6-151">클러스터에서 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-151">Remove an application from the cluster.</span></span> <span data-ttu-id="ab8d6-152">이렇게 하면 응용 프로그램 아래에 있는 서비스가 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="ab8d6-153">제거-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="ab8d6-154">서비스 패브릭 제거 클러스터의 응용 프로그램 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="ab8d6-155">이 리소스 아래에 모든 유형의 버전이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="ab8d6-156">제거-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab8d6-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="ab8d6-157">서비스 패브릭 제거 클러스터의 응용 프로그램 유형 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="ab8d6-158">제거-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ab8d6-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="ab8d6-159">클라이언트 인증에 사용 되지 않는 클라이언트 인증서 또는 인증서 주체 이름 (s)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="ab8d6-160">제거-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ab8d6-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="ab8d6-161">클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="ab8d6-162">제거-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="ab8d6-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="ab8d6-163">클러스터 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="ab8d6-164">제거-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ab8d6-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="ab8d6-165">Remvoe는 손도장 또는 일반 이름으로 클라이언트 인증서를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="ab8d6-166">제거-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="ab8d6-167">노드 형식 또는 노드 형식 내의 특정 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="ab8d6-168">제거-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="ab8d6-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="ab8d6-169">노드 형식에서 vm 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="ab8d6-170">제거-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ab8d6-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="ab8d6-171">클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="ab8d6-172">제거-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="ab8d6-173">클러스터에서 전체 노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="ab8d6-174">제거-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab8d6-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="ab8d6-175">클러스터에서 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="ab8d6-176">제거-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ab8d6-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="ab8d6-177">클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="ab8d6-178">다시 시작-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="ab8d6-179">노드 형식에서 특정 노드를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="ab8d6-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="ab8d6-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="ab8d6-181">클러스터 리소스 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="ab8d6-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="ab8d6-183">-이미지로 매개 변수를 사용 하 여 노드 형식의 특정 ndes에 대해 노드 형식 리소스 속성을 설정 하거나 이미지로 된 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="ab8d6-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ab8d6-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="ab8d6-185">하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="ab8d6-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="ab8d6-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="ab8d6-187">클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="ab8d6-188">업데이트-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab8d6-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="ab8d6-189">서비스 패브릭 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-189">Update a service fabric application.</span></span> <span data-ttu-id="ab8d6-190">이렇게 하면 응용 프로그램 매개 변수를 업데이트 하 고 응용 프로그램 업그레이드를 트리거할 응용 프로그램 유형 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="ab8d6-191">업데이트-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ab8d6-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="ab8d6-192">클러스터의 노드 형식에 대 한 내구성 계층 또는 VmSku를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="ab8d6-193">업데이트-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ab8d6-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="ab8d6-194">클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8d6-194">Update the reliability tier of the primary node type in a cluster.</span></span>

