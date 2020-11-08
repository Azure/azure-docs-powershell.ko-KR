---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217111"
---
# <span data-ttu-id="78543-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="78543-101">New-AzAksCluster</span></span>

## <span data-ttu-id="78543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78543-102">SYNOPSIS</span></span>
<span data-ttu-id="78543-103">관리 되는 Kubernetes 클러스터를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78543-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="78543-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78543-104">SYNTAX</span></span>

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

## <span data-ttu-id="78543-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78543-105">DESCRIPTION</span></span>

<span data-ttu-id="78543-106">새 AKS (Azure Kubernetes Service) 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78543-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="78543-107">예제의</span><span class="sxs-lookup"><span data-stu-id="78543-107">EXAMPLES</span></span>

### <span data-ttu-id="78543-108">기본 매개 변수를 사용 하는 새 AKS.</span><span class="sxs-lookup"><span data-stu-id="78543-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="78543-109">AKS에 Windows Server 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78543-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="78543-110">AKS에 Windows Server 컨테이너를 만들려면 AKS를 만들 때 다음 매개 변수를 4 개 이상 지정 하 고, 값이 and로 각각 설정 되어야 합니다 `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` .</span><span class="sxs-lookup"><span data-stu-id="78543-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="78543-111">변수</span><span class="sxs-lookup"><span data-stu-id="78543-111">PARAMETERS</span></span>

### <span data-ttu-id="78543-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="78543-112">-AcrNameToAttach</span></span>
<span data-ttu-id="78543-113">AKS 서비스 사용자에 게 지정 된 ACR에 대 한 ' acrpull ' 역할을 부여 합니다 (예: myacr).</span><span class="sxs-lookup"><span data-stu-id="78543-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="78543-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="78543-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="78543-115">클러스터를 만들 때 사용할 수 있는 추가 기능 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="78543-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78543-116">-AsJob</span></span>
<span data-ttu-id="78543-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="78543-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78543-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78543-118">-DefaultProfile</span></span>
<span data-ttu-id="78543-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78543-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="78543-120">-DnsNamePrefix</span></span>
<span data-ttu-id="78543-121">클러스터의 DNS 이름 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="78543-122">사용자가 windows 컨테이너를 추가 하려는 경우 길이는 <= 9 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78543-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="78543-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="78543-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="78543-124">자동 scaler 설정 여부</span><span class="sxs-lookup"><span data-stu-id="78543-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="78543-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="78543-125">-EnableRbac</span></span>
<span data-ttu-id="78543-126">Kubernetes Role-Based 액세스 가능 여부</span><span class="sxs-lookup"><span data-stu-id="78543-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="78543-127">-Force</span><span class="sxs-lookup"><span data-stu-id="78543-127">-Force</span></span>
<span data-ttu-id="78543-128">클러스터를 이미 존재 하는 경우에도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78543-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="78543-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="78543-129">-GenerateSshKey</span></span>
<span data-ttu-id="78543-130">{HOME}/.ssh/id_rsa에 ssh 키 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78543-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="78543-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="78543-131">-KubernetesVersion</span></span>
<span data-ttu-id="78543-132">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="78543-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="78543-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="78543-134">Linux 가상 컴퓨터의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="78543-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="78543-135">-LoadBalancerSku</span></span>
<span data-ttu-id="78543-136">관리 되는 클러스터에 대 한 부하 분산 장치 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="78543-137">-위치</span><span class="sxs-lookup"><span data-stu-id="78543-137">-Location</span></span>
<span data-ttu-id="78543-138">클러스터에 대 한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-138">Azure location for the cluster.</span></span>
<span data-ttu-id="78543-139">리소스 그룹의 위치가 기본적으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78543-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="78543-140">-이름</span><span class="sxs-lookup"><span data-stu-id="78543-140">-Name</span></span>
<span data-ttu-id="78543-141">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="78543-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="78543-142">-NetworkPlugin</span></span>
<span data-ttu-id="78543-143">Kubernetes 네트워크 구축에 사용 되는 네트워크 플러그인.</span><span class="sxs-lookup"><span data-stu-id="78543-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="78543-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="78543-144">-NodeCount</span></span>
<span data-ttu-id="78543-145">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="78543-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="78543-146">-NodeMaxCount</span></span>
<span data-ttu-id="78543-147">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="78543-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="78543-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="78543-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="78543-149">노드에서 실행할 수 있는 최대 pods 수입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="78543-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="78543-150">-NodeMinCount</span></span>
<span data-ttu-id="78543-151">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="78543-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="78543-152">-NodeName</span></span>
<span data-ttu-id="78543-153">구독 및 리소스 그룹의 컨텍스트에서 에이전트 풀 프로필의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="78543-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="78543-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="78543-155">노드 풀의 각 노드에 대 한 OS 디스크의 크기 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="78543-156">최소 30GB.</span><span class="sxs-lookup"><span data-stu-id="78543-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="78543-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="78543-157">-NodePoolMode</span></span>
<span data-ttu-id="78543-158">NodePoolMode는 노드 풀의 모드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="78543-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="78543-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="78543-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="78543-160">낮은 우선 순위의 가상 머신 확장 집합에 대 한 제거 정책을 지정 하는 데 사용 되는 ScaleSetEvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="78543-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="78543-161">기본적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78543-161">Default to Delete.</span></span>

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

### <span data-ttu-id="78543-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="78543-162">-NodeSetPriority</span></span>
<span data-ttu-id="78543-163">가상 컴퓨터 크기 집합 우선 순위를 지정 하는 데 사용 되는 ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="78543-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="78543-164">기본값을 일반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="78543-164">Default to regular.</span></span>

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

### <span data-ttu-id="78543-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="78543-165">-NodeVmSetType</span></span>
<span data-ttu-id="78543-166">AgentPoolType은 에이전트 풀의 형식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="78543-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="78543-167">사용할 수 있는 값은 다음과 같습니다. ' VirtualMachineScaleSets ', ' AvailabilitySet '</span><span class="sxs-lookup"><span data-stu-id="78543-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="78543-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="78543-168">-NodeVmSize</span></span>
<span data-ttu-id="78543-169">가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="78543-170">기본값은 Standard_D2_v2입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="78543-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="78543-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="78543-172">VNet SubnetID VNet의 서브넷 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78543-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="78543-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78543-173">-ResourceGroupName</span></span>
<span data-ttu-id="78543-174">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="78543-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="78543-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="78543-176">AAD 응용 프로그램/서비스 사용자와 연결 된 클라이언트 id 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="78543-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="78543-177">-SshKeyValue</span></span>
<span data-ttu-id="78543-178">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="78543-179">기본적으로 {HOME}/.ssh/id_rsa pub.</span><span class="sxs-lookup"><span data-stu-id="78543-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="78543-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="78543-180">-SubnetName</span></span>
<span data-ttu-id="78543-181">VirtualNode addon의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="78543-182">태그</span><span class="sxs-lookup"><span data-stu-id="78543-182">-Tag</span></span>
<span data-ttu-id="78543-183">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="78543-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="78543-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="78543-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="78543-185">Windows Vm에 사용할 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="78543-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="78543-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="78543-187">Windows Vm에 사용할 관리자 암호는 최소 12 자이 하 여야 하 고 하나 이상의 `[a-z]` `[A-Z]` 특수 문자를 포함 하 여 최소 한 개의 소문자가 있는 경우 `[!@#$%^&_()]` 입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="78543-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="78543-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="78543-189">모니터링 추가 기능 작업 영역의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="78543-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="78543-190">-확인</span><span class="sxs-lookup"><span data-stu-id="78543-190">-Confirm</span></span>
<span data-ttu-id="78543-191">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78543-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78543-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78543-192">-WhatIf</span></span>
<span data-ttu-id="78543-193">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78543-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78543-194">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78543-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78543-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78543-195">CommonParameters</span></span>
<span data-ttu-id="78543-196">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78543-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78543-197">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78543-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78543-198">입력</span><span class="sxs-lookup"><span data-stu-id="78543-198">INPUTS</span></span>

### <span data-ttu-id="78543-199">않아야</span><span class="sxs-lookup"><span data-stu-id="78543-199">None</span></span>

## <span data-ttu-id="78543-200">출력</span><span class="sxs-lookup"><span data-stu-id="78543-200">OUTPUTS</span></span>

### <span data-ttu-id="78543-201">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="78543-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="78543-202">상속자</span><span class="sxs-lookup"><span data-stu-id="78543-202">NOTES</span></span>

## <span data-ttu-id="78543-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78543-203">RELATED LINKS</span></span>
