---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492678"
---
# <span data-ttu-id="0af55-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0af55-101">New-AzAksCluster</span></span>

## <span data-ttu-id="0af55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af55-102">SYNOPSIS</span></span>
<span data-ttu-id="0af55-103">관리되는 새 Kubernetes 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0af55-104">구문</span><span class="sxs-lookup"><span data-stu-id="0af55-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af55-105">설명</span><span class="sxs-lookup"><span data-stu-id="0af55-105">DESCRIPTION</span></span>

<span data-ttu-id="0af55-106">새 AKS(Azure Kubernetes Service) 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="0af55-107">예제</span><span class="sxs-lookup"><span data-stu-id="0af55-107">EXAMPLES</span></span>

### <span data-ttu-id="0af55-108">기본 파라메인 AKS를 새로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="0af55-109">AKS에서 Windows Server 컨테이너를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="0af55-110">AKS에서 Windows Server 컨테이너를 만들하려면 AKS를 만들 때 다음 매개 변수를 4개 이상 지정해야 합니다. 이 값은 각각 및 그 값에 `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` 해당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="0af55-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0af55-111">PARAMETERS</span></span>

### <span data-ttu-id="0af55-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="0af55-112">-AcrNameToAttach</span></span>
<span data-ttu-id="0af55-113">지정된 ACR의 'acrpull' 역할을 AKS 서비스 주체(예: myacr)에 부여</span><span class="sxs-lookup"><span data-stu-id="0af55-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="0af55-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="0af55-115">클러스터를 만들 때 사용할 추가 기능 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0af55-116">-AsJob</span></span>
<span data-ttu-id="0af55-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0af55-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af55-118">-DefaultProfile</span></span>
<span data-ttu-id="0af55-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0af55-120">-DnsNamePrefix</span></span>
<span data-ttu-id="0af55-121">클러스터에 대한 DNS 이름 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="0af55-122">사용자가 windows 컨테이너를 <경우 길이는 9입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-122">The length must be <= 9 if users plan to add windows container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="0af55-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="0af55-124">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="0af55-124">Whether to enable auto-scaler</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="0af55-125">-EnableRbac</span></span>
<span data-ttu-id="0af55-126">Kubernetes 및 Access를 Role-Based 여부</span><span class="sxs-lookup"><span data-stu-id="0af55-126">Whether to enable Kubernetes Role-Based Access</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-127">-Force</span><span class="sxs-lookup"><span data-stu-id="0af55-127">-Force</span></span>
<span data-ttu-id="0af55-128">클러스터가 이미 있는 경우에도 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="0af55-128">Create cluster even if it already exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="0af55-129">-GenerateSshKey</span></span>
<span data-ttu-id="0af55-130">{HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="0af55-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="0af55-131">-KubernetesVersion</span></span>
<span data-ttu-id="0af55-132">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-132">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="0af55-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="0af55-134">Linux Virtual Machines의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="0af55-135">-LoadBalancerSku</span></span>
<span data-ttu-id="0af55-136">관리되는 클러스터에 대한 부하 균형 조정기 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-136">The load balancer sku for the managed cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-137">-Location</span><span class="sxs-lookup"><span data-stu-id="0af55-137">-Location</span></span>
<span data-ttu-id="0af55-138">클러스터에 대한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-138">Azure location for the cluster.</span></span>
<span data-ttu-id="0af55-139">기본값은 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-139">Defaults to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-140">-Name</span><span class="sxs-lookup"><span data-stu-id="0af55-140">-Name</span></span>
<span data-ttu-id="0af55-141">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="0af55-142">-NetworkPlugin</span></span>
<span data-ttu-id="0af55-143">Kubernetes 네트워크를 구축하는 데 사용되는 네트워크 플러그 인입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="0af55-144">-NodeCount</span></span>
<span data-ttu-id="0af55-145">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-145">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="0af55-146">-NodeMaxCount</span></span>
<span data-ttu-id="0af55-147">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="0af55-147">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="0af55-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="0af55-149">노드에서 실행할 수 있는 최대 Pod 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-149">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="0af55-150">-NodeMinCount</span></span>
<span data-ttu-id="0af55-151">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-151">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="0af55-152">-NodeName</span></span>
<span data-ttu-id="0af55-153">구독 및 리소스 그룹의 컨텍스트에서 에이전트 풀 프로필의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="0af55-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="0af55-155">노드 풀의 각 노드에 대한 OS 디스크의 크기(GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="0af55-156">최소 30GB.</span><span class="sxs-lookup"><span data-stu-id="0af55-156">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="0af55-157">-NodePoolMode</span></span>
<span data-ttu-id="0af55-158">NodePoolMode는 노드 풀의 모드를 표현합니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-158">NodePoolMode represents mode of an node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="0af55-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="0af55-160">우선 순위가 낮은 가상 머신 확장 집합에 대한 지우기 정책을 지정하는 데 사용할 ScaleSetEvictionPolicy입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="0af55-161">기본값은 삭제입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-161">Default to Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="0af55-162">-NodeSetPriority</span></span>
<span data-ttu-id="0af55-163">가상 머신 확장 집합 우선 순위를 지정하는 데 사용할 ScaleSetPriority입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="0af55-164">기본값은 일반입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-164">Default to regular.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="0af55-165">-NodeVmSetType</span></span>
<span data-ttu-id="0af55-166">AgentPoolType은 에이전트 풀의 유형을 나타남</span><span class="sxs-lookup"><span data-stu-id="0af55-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="0af55-167">가능한 값은 'VirtualMachineScaleSets', 'AvailabilitySet'입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="0af55-168">-NodeVmSize</span></span>
<span data-ttu-id="0af55-169">Virtual Machine의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="0af55-170">기본값은 Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="0af55-170">Default value is Standard_D2_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="0af55-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="0af55-172">VNet SubnetID는 VNet의 서브넷 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af55-173">-ResourceGroupName</span></span>
<span data-ttu-id="0af55-174">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-174">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="0af55-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="0af55-176">AAD 애플리케이션/서비스 주체와 연결된 클라이언트 ID 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="0af55-177">-SshKeyValue</span></span>
<span data-ttu-id="0af55-178">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="0af55-179">기본값은 {HOME}/.ssh/id_rsa.pub입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0af55-180">-SubnetName</span></span>
<span data-ttu-id="0af55-181">VirtualNode 추가 기능의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-181">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="0af55-182">-Tag</span></span>
<span data-ttu-id="0af55-183">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="0af55-183">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="0af55-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="0af55-185">Windows VM에 사용할 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-185">The administrator username to use for Windows VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="0af55-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="0af55-187">Windows VM에 사용할 관리자 암호의 길이는 12자 이상으로, 소문자(예: 1개와 특수 문자 1개)를 `[a-z]` `[A-Z]` 포함해야 `[!@#$%^&_()]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0af55-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="0af55-189">모니터링 추가 기능의 작업 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-189">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0af55-190">-Confirm</span></span>
<span data-ttu-id="0af55-191">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af55-192">-WhatIf</span></span>
<span data-ttu-id="0af55-193">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0af55-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0af55-194">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af55-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af55-195">CommonParameters</span></span>
<span data-ttu-id="0af55-196">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0af55-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af55-197">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0af55-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af55-198">입력</span><span class="sxs-lookup"><span data-stu-id="0af55-198">INPUTS</span></span>

### <span data-ttu-id="0af55-199">없음</span><span class="sxs-lookup"><span data-stu-id="0af55-199">None</span></span>

## <span data-ttu-id="0af55-200">출력</span><span class="sxs-lookup"><span data-stu-id="0af55-200">OUTPUTS</span></span>

### <span data-ttu-id="0af55-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0af55-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="0af55-202">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0af55-202">NOTES</span></span>

## <span data-ttu-id="0af55-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0af55-203">RELATED LINKS</span></span>
