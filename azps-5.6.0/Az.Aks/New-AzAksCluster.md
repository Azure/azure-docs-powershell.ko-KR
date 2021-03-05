---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: 806c3a17dcfc470e01801548013d0d8c6ea58ae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008160"
---
# <span data-ttu-id="fde77-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="fde77-101">New-AzAksCluster</span></span>

## <span data-ttu-id="fde77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde77-102">SYNOPSIS</span></span>
<span data-ttu-id="fde77-103">새 관리되는 Kubernetes 클러스터를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="fde77-104">구문</span><span class="sxs-lookup"><span data-stu-id="fde77-104">SYNTAX</span></span>

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

## <span data-ttu-id="fde77-105">설명</span><span class="sxs-lookup"><span data-stu-id="fde77-105">DESCRIPTION</span></span>

<span data-ttu-id="fde77-106">새 Azure Kubernetes Service(AKS) 클러스터를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="fde77-107">예제</span><span class="sxs-lookup"><span data-stu-id="fde77-107">EXAMPLES</span></span>

### <span data-ttu-id="fde77-108">기본 params가 있는 AKS를 새로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="fde77-109">AKS에서 Windows Server 컨테이너를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="fde77-110">AKS에서 Windows Server 컨테이너를 만들하려면 AKS를 만들 때 다음 매개 변수를 4개 이상 지정해야 `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="fde77-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fde77-111">PARAMETERS</span></span>

### <span data-ttu-id="fde77-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="fde77-112">-AcrNameToAttach</span></span>
<span data-ttu-id="fde77-113">지정된 ACR의 'acrpull' 역할을 AKS 서비스 주체(예: myacr)에 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="fde77-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="fde77-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="fde77-115">클러스터를 만들 때 사용할 추가 기능 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="fde77-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fde77-116">-AsJob</span></span>
<span data-ttu-id="fde77-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fde77-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fde77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde77-118">-DefaultProfile</span></span>
<span data-ttu-id="fde77-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde77-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="fde77-120">-DnsNamePrefix</span></span>
<span data-ttu-id="fde77-121">클러스터에 대한 DNS 이름 도두사입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="fde77-122">사용자가 windows 컨테이너를 <경우 길이 = 9를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="fde77-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="fde77-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="fde77-124">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="fde77-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="fde77-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="fde77-125">-EnableRbac</span></span>
<span data-ttu-id="fde77-126">Kubernetes에서 Access를 사용하도록 Role-Based 여부</span><span class="sxs-lookup"><span data-stu-id="fde77-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="fde77-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fde77-127">-Force</span></span>
<span data-ttu-id="fde77-128">클러스터가 이미 있는 경우에도 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="fde77-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="fde77-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="fde77-129">-GenerateSshKey</span></span>
<span data-ttu-id="fde77-130">{HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="fde77-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="fde77-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="fde77-131">-KubernetesVersion</span></span>
<span data-ttu-id="fde77-132">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="fde77-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="fde77-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="fde77-134">Linux Virtual Machines의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="fde77-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="fde77-135">-LoadBalancerSku</span></span>
<span data-ttu-id="fde77-136">관리되는 클러스터에 대한 부하 균형 조정기 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="fde77-137">-Location</span><span class="sxs-lookup"><span data-stu-id="fde77-137">-Location</span></span>
<span data-ttu-id="fde77-138">클러스터의 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-138">Azure location for the cluster.</span></span>
<span data-ttu-id="fde77-139">리소스 그룹의 위치를 기본값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="fde77-140">-Name</span><span class="sxs-lookup"><span data-stu-id="fde77-140">-Name</span></span>
<span data-ttu-id="fde77-141">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="fde77-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="fde77-142">-NetworkPlugin</span></span>
<span data-ttu-id="fde77-143">Kubernetes 네트워크를 구축하는 데 사용되는 네트워크 플러그 인입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="fde77-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="fde77-144">-NodeCount</span></span>
<span data-ttu-id="fde77-145">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="fde77-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="fde77-146">-NodeMaxCount</span></span>
<span data-ttu-id="fde77-147">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="fde77-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="fde77-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="fde77-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="fde77-149">노드에서 실행할 수 있는 최대 Pod 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="fde77-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="fde77-150">-NodeMinCount</span></span>
<span data-ttu-id="fde77-151">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="fde77-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="fde77-152">-NodeName</span></span>
<span data-ttu-id="fde77-153">구독 및 리소스 그룹의 컨텍스트에서 에이전트 풀 프로필의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="fde77-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="fde77-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="fde77-155">노드 풀의 각 노드에 대한 OS 디스크의 GB 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="fde77-156">최소 30GB.</span><span class="sxs-lookup"><span data-stu-id="fde77-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="fde77-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="fde77-157">-NodePoolMode</span></span>
<span data-ttu-id="fde77-158">NodePoolMode는 노드 풀의 모드를 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="fde77-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fde77-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="fde77-160">ScaleSetEvictionPolicy를 사용하여 우선 순위가 낮은 가상 머신 확장 집합에 대한 eviction 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="fde77-161">기본적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-161">Default to Delete.</span></span>

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

### <span data-ttu-id="fde77-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="fde77-162">-NodeSetPriority</span></span>
<span data-ttu-id="fde77-163">Virtual Machine Scale Set 우선 순위를 지정하는 데 사용할 ScaleSetPriority입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="fde77-164">기본값은 일반입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-164">Default to regular.</span></span>

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

### <span data-ttu-id="fde77-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="fde77-165">-NodeVmSetType</span></span>
<span data-ttu-id="fde77-166">AgentPoolType은 에이전트 풀의 유형을 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="fde77-167">가능한 값에는 'VirtualMachineScaleSets', 'AvailabilitySet'이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="fde77-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="fde77-168">-NodeVmSize</span></span>
<span data-ttu-id="fde77-169">Virtual Machine의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="fde77-170">기본값은 Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="fde77-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="fde77-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="fde77-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="fde77-172">VNet SubnetID는 VNet의 서브넷 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="fde77-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde77-173">-ResourceGroupName</span></span>
<span data-ttu-id="fde77-174">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="fde77-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="fde77-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="fde77-176">AAD 애플리케이션/서비스 주체와 연결된 클라이언트 ID 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="fde77-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="fde77-177">-SshKeyValue</span></span>
<span data-ttu-id="fde77-178">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="fde77-179">기본값은 {HOME}/.ssh/id_rsa.pub입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="fde77-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fde77-180">-SubnetName</span></span>
<span data-ttu-id="fde77-181">VirtualNode 추가온의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="fde77-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="fde77-182">-Tag</span></span>
<span data-ttu-id="fde77-183">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="fde77-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="fde77-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="fde77-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="fde77-185">Windows VM에 사용할 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="fde77-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="fde77-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="fde77-187">Windows VM에 사용할 관리자 암호는 하나 이상의 소문자 문자(예: 하나 및 특수 문자 1개)를 포함하는 길이가 12 이상이 `[a-z]` `[A-Z]` 되어야 `[!@#$%^&*()]` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="fde77-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="fde77-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="fde77-189">모니터링 추가 기능의 작업 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="fde77-190">-확인</span><span class="sxs-lookup"><span data-stu-id="fde77-190">-Confirm</span></span>
<span data-ttu-id="fde77-191">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde77-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde77-192">-WhatIf</span></span>
<span data-ttu-id="fde77-193">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde77-194">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde77-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde77-195">CommonParameters</span></span>
<span data-ttu-id="fde77-196">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fde77-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde77-197">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fde77-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde77-198">입력</span><span class="sxs-lookup"><span data-stu-id="fde77-198">INPUTS</span></span>

### <span data-ttu-id="fde77-199">없음</span><span class="sxs-lookup"><span data-stu-id="fde77-199">None</span></span>

## <span data-ttu-id="fde77-200">출력</span><span class="sxs-lookup"><span data-stu-id="fde77-200">OUTPUTS</span></span>

### <span data-ttu-id="fde77-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fde77-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fde77-202">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fde77-202">NOTES</span></span>

## <span data-ttu-id="fde77-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fde77-203">RELATED LINKS</span></span>
