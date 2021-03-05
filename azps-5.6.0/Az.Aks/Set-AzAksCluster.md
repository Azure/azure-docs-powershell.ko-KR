---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0cf25018ad9cb432b739f5beeb147d20272d7f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002027"
---
# <span data-ttu-id="db46b-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="db46b-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="db46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db46b-102">SYNOPSIS</span></span>
<span data-ttu-id="db46b-103">관리되는 Kubernetes 클러스터를 업데이트하거나 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="db46b-104">구문</span><span class="sxs-lookup"><span data-stu-id="db46b-104">SYNTAX</span></span>

### <span data-ttu-id="db46b-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="db46b-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db46b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db46b-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db46b-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db46b-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db46b-108">설명</span><span class="sxs-lookup"><span data-stu-id="db46b-108">DESCRIPTION</span></span>
<span data-ttu-id="db46b-109">관리되는 Kubernetes 클러스터를 업데이트하거나 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="db46b-110">예제</span><span class="sxs-lookup"><span data-stu-id="db46b-110">EXAMPLES</span></span>

### <span data-ttu-id="db46b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="db46b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="db46b-112">Kubernetes 클러스터의 노드 수를 5로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="db46b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="db46b-113">PARAMETERS</span></span>

### <span data-ttu-id="db46b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db46b-114">-AsJob</span></span>
<span data-ttu-id="db46b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="db46b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db46b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db46b-116">-DefaultProfile</span></span>
<span data-ttu-id="db46b-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db46b-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="db46b-118">-DnsNamePrefix</span></span>
<span data-ttu-id="db46b-119">클러스터에 대한 DNS 이름 도두사입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="db46b-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="db46b-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="db46b-121">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="db46b-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="db46b-122">-Id</span><span class="sxs-lookup"><span data-stu-id="db46b-122">-Id</span></span>
<span data-ttu-id="db46b-123">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="db46b-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db46b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db46b-124">-InputObject</span></span>
<span data-ttu-id="db46b-125">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db46b-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="db46b-126">-KubernetesVersion</span></span>
<span data-ttu-id="db46b-127">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="db46b-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="db46b-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="db46b-129">Linux Virtual Machines의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="db46b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="db46b-130">-Location</span></span>
<span data-ttu-id="db46b-131">클러스터의 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-131">Azure location for the cluster.</span></span>
<span data-ttu-id="db46b-132">리소스 그룹의 위치를 기본값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="db46b-133">-Name</span><span class="sxs-lookup"><span data-stu-id="db46b-133">-Name</span></span>
<span data-ttu-id="db46b-134">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db46b-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="db46b-135">-NodeCount</span></span>
<span data-ttu-id="db46b-136">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="db46b-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="db46b-137">-NodeMaxCount</span></span>
<span data-ttu-id="db46b-138">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="db46b-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="db46b-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="db46b-139">-NodeMinCount</span></span>
<span data-ttu-id="db46b-140">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="db46b-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="db46b-141">-NodeName</span></span>
<span data-ttu-id="db46b-142">구독 및 리소스 그룹의 컨텍스트에서 에이전트 풀 프로필의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="db46b-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="db46b-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="db46b-144">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="db46b-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="db46b-145">-NodePoolMode</span></span>
<span data-ttu-id="db46b-146">NodePoolMode는 노드 풀의 모드를 나타내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="db46b-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="db46b-147">-NodeVmSize</span></span>
<span data-ttu-id="db46b-148">Virtual Machine의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="db46b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db46b-149">-ResourceGroupName</span></span>
<span data-ttu-id="db46b-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db46b-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="db46b-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="db46b-152">AAD 애플리케이션/서비스 주체와 연결된 클라이언트 ID 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db46b-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="db46b-153">-SshKeyValue</span></span>
<span data-ttu-id="db46b-154">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="db46b-155">기본값은 {HOME}/.ssh/id_rsa.pub입니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="db46b-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="db46b-156">-Tag</span></span>
<span data-ttu-id="db46b-157">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="db46b-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="db46b-158">-확인</span><span class="sxs-lookup"><span data-stu-id="db46b-158">-Confirm</span></span>
<span data-ttu-id="db46b-159">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db46b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db46b-160">-WhatIf</span></span>
<span data-ttu-id="db46b-161">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db46b-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db46b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db46b-163">CommonParameters</span></span>
<span data-ttu-id="db46b-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db46b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db46b-165">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db46b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db46b-166">입력</span><span class="sxs-lookup"><span data-stu-id="db46b-166">INPUTS</span></span>

### <span data-ttu-id="db46b-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="db46b-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="db46b-168">System.String</span><span class="sxs-lookup"><span data-stu-id="db46b-168">System.String</span></span>

## <span data-ttu-id="db46b-169">출력</span><span class="sxs-lookup"><span data-stu-id="db46b-169">OUTPUTS</span></span>

### <span data-ttu-id="db46b-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="db46b-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="db46b-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db46b-171">NOTES</span></span>

## <span data-ttu-id="db46b-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db46b-172">RELATED LINKS</span></span>
