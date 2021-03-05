---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963627"
---
# <span data-ttu-id="a9849-101">Az.ServiceFabric 모듈</span><span class="sxs-lookup"><span data-stu-id="a9849-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="a9849-102">설명</span><span class="sxs-lookup"><span data-stu-id="a9849-102">Description</span></span>
<span data-ttu-id="a9849-103">보안 클러스터 만들기, 클러스터 인증서 롤오프, 클러스터에서 노드 추가 또는 제거 등의 엔드-2 엔드 작업을 자동화하는 데 사용할 수 있는 Azure Service Fabric 모듈 모든 작업의 전체 목록은 아래에 나열되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="a9849-104">Az.ServiceFabric Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a9849-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="a9849-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a9849-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="a9849-106">클라이언트 인증을 위해 클러스터에 일반적인 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="a9849-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a9849-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="a9849-108">클러스터에 보조 클러스터 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="a9849-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a9849-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="a9849-110">클러스터에 인증서 일반 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="a9849-111">이렇게 하면 클라이언트 인증을 위해 클러스터가 다시 인증서를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="a9849-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="a9849-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="a9849-113">노드 유형에 vm 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="a9849-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="a9849-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="a9849-115">노드 유형에 인증서 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="a9849-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a9849-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="a9849-117">클러스터의 특정 노드 유형에 노드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="a9849-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="a9849-119">기존 클러스터에 새 노드 형식을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="a9849-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a9849-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="a9849-121">Service Fabric 애플리케이션 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="a9849-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a9849-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="a9849-123">Service Fabric 애플리케이션 유형 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="a9849-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a9849-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="a9849-125">Service Fabric 애플리케이션 유형 버전 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="a9849-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a9849-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="a9849-127">클러스터 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="a9849-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a9849-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="a9849-129">관리되는 클러스터 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="a9849-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="a9849-131">관리되는 노드 형식 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="a9849-132">Get-AzServiceFabricServicService</span><span class="sxs-lookup"><span data-stu-id="a9849-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="a9849-133">지정된 애플리케이션 및 클러스터에서 Service Fabric 서비스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="a9849-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a9849-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="a9849-135">지정된 리소스 그룹 및 클러스터에서 새 서비스 패브릭 애플리케이션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="a9849-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a9849-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="a9849-137">지정된 리소스 그룹 및 클러스터 아래에서 새 서비스 패브릭 애플리케이션 유형을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="a9849-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a9849-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="a9849-139">지정된 리소스 그룹 및 클러스터 아래에서 새 애플리케이션 형식 버전을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="a9849-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a9849-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="a9849-141">이 명령은 사용자가 제공하는 인증서 또는 시스템이 생성한 자체 서명된 인증서를 사용하여 새 서비스 패브릭 클러스터를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="a9849-142">기본 템플릿 또는 사용자가 제공하는 사용자 지정 템플릿을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="a9849-143">자체 서명된 인증서를 내보낼 폴더를 지정하거나 나중에 키 자격 증명 모음에서 해당 인증서를 인출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="a9849-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a9849-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="a9849-145">새 관리되는 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="a9849-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="a9849-147">새 노드 형식 리소스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-147">Create new node type resource.</span></span>

### [<span data-ttu-id="a9849-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a9849-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="a9849-149">지정된 애플리케이션 및 클러스터에서 새 서비스 패브릭 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="a9849-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a9849-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="a9849-151">클러스터에서 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-151">Remove an application from the cluster.</span></span> <span data-ttu-id="a9849-152">이렇게 하면 애플리케이션에서 모든 서비스가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="a9849-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a9849-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="a9849-154">클러스터에서 Service 패브릭 애플리케이션 유형을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="a9849-155">이렇게 하면 이 리소스의 모든 형식 버전이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="a9849-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a9849-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="a9849-157">클러스터에서 Service 패브릭 애플리케이션 형식 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="a9849-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a9849-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="a9849-159">클러스터에 대한 클라이언트 인증에 사용되는 클라이언트 인증서 또는 인증서 주체 이름에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="a9849-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a9849-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="a9849-161">클러스터 보안에 사용되는 클러스터 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="a9849-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a9849-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="a9849-163">클러스터 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="a9849-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a9849-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="a9849-165">지문 또는 일반적인 이름으로 클라이언트 인증서를 Remvoe합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="a9849-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="a9849-167">노드 유형 내에서 노드 유형 또는 특정 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="a9849-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="a9849-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="a9849-169">노드 형식에서 vm 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="a9849-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a9849-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="a9849-171">클러스터에서 특정 노드 유형에서 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="a9849-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="a9849-173">클러스터에서 전체 노드 유형을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="a9849-174">Remove-AzServiceFabricServicService</span><span class="sxs-lookup"><span data-stu-id="a9849-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="a9849-175">클러스터에서 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="a9849-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a9849-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="a9849-177">클러스터에서 하나 또는 여러 Service Fabric 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="a9849-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="a9849-179">노드 형식에서 특정 노드를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="a9849-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="a9849-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="a9849-181">클러스터 리소스 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="a9849-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9849-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="a9849-183">-Reimage 매개 변수를 사용하여 노드 형식 리소스 속성을 설정하거나 노드 형식의 특정 ndes에서 리미지 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="a9849-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a9849-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="a9849-185">클러스터에 하나 또는 여러 Service Fabric 설정을 추가하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="a9849-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a9849-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="a9849-187">클러스터의 Service Fabric 업그레이드 유형을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="a9849-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a9849-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="a9849-189">서비스 패브릭 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-189">Update a service fabric application.</span></span> <span data-ttu-id="a9849-190">이렇게 하면 애플리케이션 매개 변수를 업데이트하고/또는 애플리케이션 업그레이드를 트리거하는 애플리케이션 형식 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="a9849-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a9849-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="a9849-192">클러스터의 노드 형식의 내구성 계층 또는 VmSku를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="a9849-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a9849-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="a9849-194">클러스터의 기본 노드 형식의 안정성 계층을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a9849-194">Update the reliability tier of the primary node type in a cluster.</span></span>

