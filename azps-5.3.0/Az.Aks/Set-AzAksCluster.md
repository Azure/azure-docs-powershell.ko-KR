---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492668"
---
# <span data-ttu-id="1c3b0-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="1c3b0-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="1c3b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3b0-103">관리되는 Kubernetes 클러스터를 업데이트하거나 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1c3b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c3b0-104">SYNTAX</span></span>

### <span data-ttu-id="1c3b0-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c3b0-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c3b0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c3b0-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c3b0-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c3b0-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3b0-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c3b0-108">DESCRIPTION</span></span>
<span data-ttu-id="1c3b0-109">관리되는 Kubernetes 클러스터를 업데이트하거나 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1c3b0-110">예제</span><span class="sxs-lookup"><span data-stu-id="1c3b0-110">EXAMPLES</span></span>

### <span data-ttu-id="1c3b0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c3b0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="1c3b0-112">Kubernetes 클러스터의 노드 수를 5로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="1c3b0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3b0-113">PARAMETERS</span></span>

### <span data-ttu-id="1c3b0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c3b0-114">-AsJob</span></span>
<span data-ttu-id="1c3b0-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1c3b0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c3b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3b0-116">-DefaultProfile</span></span>
<span data-ttu-id="1c3b0-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3b0-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="1c3b0-118">-DnsNamePrefix</span></span>
<span data-ttu-id="1c3b0-119">클러스터에 대한 DNS 이름 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="1c3b0-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="1c3b0-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="1c3b0-121">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="1c3b0-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="1c3b0-122">-Id</span><span class="sxs-lookup"><span data-stu-id="1c3b0-122">-Id</span></span>
<span data-ttu-id="1c3b0-123">관리되는 Kubernetes 클러스터의 ID</span><span class="sxs-lookup"><span data-stu-id="1c3b0-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="1c3b0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c3b0-124">-InputObject</span></span>
<span data-ttu-id="1c3b0-125">일반적으로 파이프라인을 통해 전달되는 PSKubernetesCluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1c3b0-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="1c3b0-126">-KubernetesVersion</span></span>
<span data-ttu-id="1c3b0-127">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="1c3b0-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="1c3b0-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="1c3b0-129">Linux Virtual Machines의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="1c3b0-130">-Location</span><span class="sxs-lookup"><span data-stu-id="1c3b0-130">-Location</span></span>
<span data-ttu-id="1c3b0-131">클러스터에 대한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-131">Azure location for the cluster.</span></span>
<span data-ttu-id="1c3b0-132">기본값은 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="1c3b0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1c3b0-133">-Name</span></span>
<span data-ttu-id="1c3b0-134">Kubernetes 관리되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="1c3b0-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1c3b0-135">-NodeCount</span></span>
<span data-ttu-id="1c3b0-136">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1c3b0-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="1c3b0-137">-NodeMaxCount</span></span>
<span data-ttu-id="1c3b0-138">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="1c3b0-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="1c3b0-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="1c3b0-139">-NodeMinCount</span></span>
<span data-ttu-id="1c3b0-140">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="1c3b0-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1c3b0-141">-NodeName</span></span>
<span data-ttu-id="1c3b0-142">구독 및 리소스 그룹의 컨텍스트에서 에이전트 풀 프로필의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="1c3b0-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="1c3b0-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="1c3b0-144">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1c3b0-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="1c3b0-145">-NodePoolMode</span></span>
<span data-ttu-id="1c3b0-146">NodePoolMode는 노드 풀의 모드를 표현합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="1c3b0-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="1c3b0-147">-NodeVmSize</span></span>
<span data-ttu-id="1c3b0-148">Virtual Machine의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="1c3b0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3b0-149">-ResourceGroupName</span></span>
<span data-ttu-id="1c3b0-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c3b0-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="1c3b0-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="1c3b0-152">AAD 애플리케이션/서비스 주체와 연결된 클라이언트 ID 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="1c3b0-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="1c3b0-153">-SshKeyValue</span></span>
<span data-ttu-id="1c3b0-154">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="1c3b0-155">기본값은 {HOME}/.ssh/id_rsa.pub입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="1c3b0-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c3b0-156">-Tag</span></span>
<span data-ttu-id="1c3b0-157">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="1c3b0-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="1c3b0-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3b0-158">-Confirm</span></span>
<span data-ttu-id="1c3b0-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3b0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3b0-160">-WhatIf</span></span>
<span data-ttu-id="1c3b0-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c3b0-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3b0-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3b0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3b0-163">CommonParameters</span></span>
<span data-ttu-id="1c3b0-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3b0-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c3b0-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3b0-166">입력</span><span class="sxs-lookup"><span data-stu-id="1c3b0-166">INPUTS</span></span>

### <span data-ttu-id="1c3b0-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1c3b0-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="1c3b0-168">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3b0-168">System.String</span></span>

## <span data-ttu-id="1c3b0-169">출력</span><span class="sxs-lookup"><span data-stu-id="1c3b0-169">OUTPUTS</span></span>

### <span data-ttu-id="1c3b0-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1c3b0-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1c3b0-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c3b0-171">NOTES</span></span>

## <span data-ttu-id="1c3b0-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c3b0-172">RELATED LINKS</span></span>
