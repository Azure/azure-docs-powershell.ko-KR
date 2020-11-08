---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217103"
---
# <span data-ttu-id="0c7be-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0c7be-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="0c7be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7be-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7be-103">관리 Kubernetes 클러스터를 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0c7be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c7be-104">SYNTAX</span></span>

### <span data-ttu-id="0c7be-105">defaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c7be-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7be-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7be-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7be-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7be-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c7be-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0c7be-108">DESCRIPTION</span></span>
<span data-ttu-id="0c7be-109">관리 Kubernetes 클러스터를 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0c7be-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0c7be-110">EXAMPLES</span></span>

### <span data-ttu-id="0c7be-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c7be-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="0c7be-112">Kubernetes 클러스터의 노드 수를 5로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="0c7be-113">변수</span><span class="sxs-lookup"><span data-stu-id="0c7be-113">PARAMETERS</span></span>

### <span data-ttu-id="0c7be-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c7be-114">-AsJob</span></span>
<span data-ttu-id="0c7be-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0c7be-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c7be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7be-116">-DefaultProfile</span></span>
<span data-ttu-id="0c7be-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c7be-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0c7be-118">-DnsNamePrefix</span></span>
<span data-ttu-id="0c7be-119">클러스터의 DNS 이름 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="0c7be-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="0c7be-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="0c7be-121">자동 scaler 설정 여부</span><span class="sxs-lookup"><span data-stu-id="0c7be-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="0c7be-122">-Id</span><span class="sxs-lookup"><span data-stu-id="0c7be-122">-Id</span></span>
<span data-ttu-id="0c7be-123">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="0c7be-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c7be-124">-InputObject</span></span>
<span data-ttu-id="0c7be-125">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="0c7be-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="0c7be-126">-KubernetesVersion</span></span>
<span data-ttu-id="0c7be-127">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="0c7be-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="0c7be-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="0c7be-129">Linux 가상 컴퓨터의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="0c7be-130">-위치</span><span class="sxs-lookup"><span data-stu-id="0c7be-130">-Location</span></span>
<span data-ttu-id="0c7be-131">클러스터에 대 한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-131">Azure location for the cluster.</span></span>
<span data-ttu-id="0c7be-132">리소스 그룹의 위치가 기본적으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="0c7be-133">-이름</span><span class="sxs-lookup"><span data-stu-id="0c7be-133">-Name</span></span>
<span data-ttu-id="0c7be-134">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="0c7be-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="0c7be-135">-NodeCount</span></span>
<span data-ttu-id="0c7be-136">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="0c7be-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="0c7be-137">-NodeMaxCount</span></span>
<span data-ttu-id="0c7be-138">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="0c7be-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="0c7be-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="0c7be-139">-NodeMinCount</span></span>
<span data-ttu-id="0c7be-140">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="0c7be-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="0c7be-141">-NodeName</span></span>
<span data-ttu-id="0c7be-142">구독 및 리소스 그룹의 컨텍스트에서 에이전트 풀 프로필의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="0c7be-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="0c7be-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="0c7be-144">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="0c7be-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="0c7be-145">-NodePoolMode</span></span>
<span data-ttu-id="0c7be-146">NodePoolMode는 노드 풀의 모드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="0c7be-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="0c7be-147">-NodeVmSize</span></span>
<span data-ttu-id="0c7be-148">가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="0c7be-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7be-149">-ResourceGroupName</span></span>
<span data-ttu-id="0c7be-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="0c7be-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="0c7be-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="0c7be-152">AAD 응용 프로그램/서비스 사용자와 연결 된 클라이언트 id 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="0c7be-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="0c7be-153">-SshKeyValue</span></span>
<span data-ttu-id="0c7be-154">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="0c7be-155">기본적으로 {HOME}/.ssh/id_rsa pub.</span><span class="sxs-lookup"><span data-stu-id="0c7be-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="0c7be-156">태그</span><span class="sxs-lookup"><span data-stu-id="0c7be-156">-Tag</span></span>
<span data-ttu-id="0c7be-157">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="0c7be-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="0c7be-158">-확인</span><span class="sxs-lookup"><span data-stu-id="0c7be-158">-Confirm</span></span>
<span data-ttu-id="0c7be-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7be-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7be-160">-WhatIf</span></span>
<span data-ttu-id="0c7be-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7be-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c7be-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7be-163">CommonParameters</span></span>
<span data-ttu-id="0c7be-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7be-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7be-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c7be-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7be-166">입력</span><span class="sxs-lookup"><span data-stu-id="0c7be-166">INPUTS</span></span>

### <span data-ttu-id="0c7be-167">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="0c7be-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="0c7be-168">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c7be-168">System.String</span></span>

## <span data-ttu-id="0c7be-169">출력</span><span class="sxs-lookup"><span data-stu-id="0c7be-169">OUTPUTS</span></span>

### <span data-ttu-id="0c7be-170">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="0c7be-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="0c7be-171">상속자</span><span class="sxs-lookup"><span data-stu-id="0c7be-171">NOTES</span></span>

## <span data-ttu-id="0c7be-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c7be-172">RELATED LINKS</span></span>
