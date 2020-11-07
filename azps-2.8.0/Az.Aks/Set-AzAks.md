---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698200"
---
# <span data-ttu-id="e9c9f-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="e9c9f-101">Set-AzAks</span></span>

## <span data-ttu-id="e9c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c9f-103">관리 Kubernetes 클러스터를 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e9c9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9c9f-104">SYNTAX</span></span>

### <span data-ttu-id="e9c9f-105">defaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e9c9f-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9c9f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9c9f-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9c9f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9c9f-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c9f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e9c9f-108">DESCRIPTION</span></span>
<span data-ttu-id="e9c9f-109">관리 Kubernetes 클러스터를 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e9c9f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e9c9f-110">EXAMPLES</span></span>

### <span data-ttu-id="e9c9f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9c9f-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="e9c9f-112">Kubernetes 클러스터의 노드 수를 5로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="e9c9f-113">변수</span><span class="sxs-lookup"><span data-stu-id="e9c9f-113">PARAMETERS</span></span>

### <span data-ttu-id="e9c9f-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="e9c9f-114">-AdminUserName</span></span>
<span data-ttu-id="e9c9f-115">Linux 가상 컴퓨터의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="e9c9f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9c9f-116">-AsJob</span></span>
<span data-ttu-id="e9c9f-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e9c9f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9c9f-118">-Clidandsecret</span><span class="sxs-lookup"><span data-stu-id="e9c9f-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="e9c9f-119">AAD 응용 프로그램/서비스 사용자와 연결 된 클라이언트 id 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="e9c9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c9f-120">-DefaultProfile</span></span>
<span data-ttu-id="e9c9f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c9f-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e9c9f-122">-DnsNamePrefix</span></span>
<span data-ttu-id="e9c9f-123">클러스터의 DNS 이름 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="e9c9f-124">-Id</span><span class="sxs-lookup"><span data-stu-id="e9c9f-124">-Id</span></span>
<span data-ttu-id="e9c9f-125">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e9c9f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9c9f-126">-InputObject</span></span>
<span data-ttu-id="e9c9f-127">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9c9f-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e9c9f-128">-KubernetesVersion</span></span>
<span data-ttu-id="e9c9f-129">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="e9c9f-130">-위치</span><span class="sxs-lookup"><span data-stu-id="e9c9f-130">-Location</span></span>
<span data-ttu-id="e9c9f-131">클러스터에 대 한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-131">Azure location for the cluster.</span></span>
<span data-ttu-id="e9c9f-132">리소스 그룹의 위치가 기본적으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="e9c9f-133">-이름</span><span class="sxs-lookup"><span data-stu-id="e9c9f-133">-Name</span></span>
<span data-ttu-id="e9c9f-134">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="e9c9f-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e9c9f-135">-NodeCount</span></span>
<span data-ttu-id="e9c9f-136">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="e9c9f-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e9c9f-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="e9c9f-138">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="e9c9f-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="e9c9f-139">-NodeVmSize</span></span>
<span data-ttu-id="e9c9f-140">가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="e9c9f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c9f-141">-ResourceGroupName</span></span>
<span data-ttu-id="e9c9f-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="e9c9f-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e9c9f-143">-SshKeyValue</span></span>
<span data-ttu-id="e9c9f-144">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="e9c9f-145">기본적으로 {HOME}/.ssh/id_rsa pub.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="e9c9f-146">태그</span><span class="sxs-lookup"><span data-stu-id="e9c9f-146">-Tag</span></span>
<span data-ttu-id="e9c9f-147">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="e9c9f-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="e9c9f-148">-확인</span><span class="sxs-lookup"><span data-stu-id="e9c9f-148">-Confirm</span></span>
<span data-ttu-id="e9c9f-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c9f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c9f-150">-WhatIf</span></span>
<span data-ttu-id="e9c9f-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c9f-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c9f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c9f-153">CommonParameters</span></span>
<span data-ttu-id="e9c9f-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c9f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c9f-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c9f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c9f-156">입력</span><span class="sxs-lookup"><span data-stu-id="e9c9f-156">INPUTS</span></span>

### <span data-ttu-id="e9c9f-157">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="e9c9f-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="e9c9f-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e9c9f-158">System.String</span></span>

## <span data-ttu-id="e9c9f-159">출력</span><span class="sxs-lookup"><span data-stu-id="e9c9f-159">OUTPUTS</span></span>

### <span data-ttu-id="e9c9f-160">Aks. p U<c13> Netescluster</span><span class="sxs-lookup"><span data-stu-id="e9c9f-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e9c9f-161">상속자</span><span class="sxs-lookup"><span data-stu-id="e9c9f-161">NOTES</span></span>

## <span data-ttu-id="e9c9f-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9c9f-162">RELATED LINKS</span></span>
