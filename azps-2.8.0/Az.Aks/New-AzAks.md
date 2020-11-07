---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698204"
---
# <span data-ttu-id="f9616-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="f9616-101">New-AzAks</span></span>

## <span data-ttu-id="f9616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9616-102">SYNOPSIS</span></span>
<span data-ttu-id="f9616-103">관리 되는 Kubernetes 클러스터를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f9616-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9616-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9616-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f9616-105">DESCRIPTION</span></span>

<span data-ttu-id="f9616-106">관리 되는 Kubernetes 클러스터를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f9616-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f9616-107">EXAMPLES</span></span>

### <span data-ttu-id="f9616-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9616-108">Example 1</span></span>

<span data-ttu-id="f9616-109">기본 매개 변수를 사용 하 여 관리 되는 Kubernetes 클러스터를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f9616-110">변수</span><span class="sxs-lookup"><span data-stu-id="f9616-110">PARAMETERS</span></span>

### <span data-ttu-id="f9616-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="f9616-111">-AdminUserName</span></span>
<span data-ttu-id="f9616-112">Linux 가상 컴퓨터의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="f9616-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9616-113">-AsJob</span></span>
<span data-ttu-id="f9616-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f9616-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9616-115">-Clidandsecret</span><span class="sxs-lookup"><span data-stu-id="f9616-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="f9616-116">AAD 응용 프로그램/서비스 사용자와 연결 된 클라이언트 id 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="f9616-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9616-117">-DefaultProfile</span></span>
<span data-ttu-id="f9616-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9616-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f9616-119">-DnsNamePrefix</span></span>
<span data-ttu-id="f9616-120">클러스터의 DNS 이름 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="f9616-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f9616-121">-Force</span></span>
<span data-ttu-id="f9616-122">클러스터를 이미 존재 하는 경우에도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="f9616-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="f9616-123">-KubernetesVersion</span></span>
<span data-ttu-id="f9616-124">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="f9616-125">-위치</span><span class="sxs-lookup"><span data-stu-id="f9616-125">-Location</span></span>
<span data-ttu-id="f9616-126">클러스터에 대 한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-126">Azure location for the cluster.</span></span>
<span data-ttu-id="f9616-127">리소스 그룹의 위치가 기본적으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="f9616-128">-이름</span><span class="sxs-lookup"><span data-stu-id="f9616-128">-Name</span></span>
<span data-ttu-id="f9616-129">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="f9616-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f9616-130">-NodeCount</span></span>
<span data-ttu-id="f9616-131">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="f9616-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="f9616-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="f9616-133">노드 풀의 각 노드에 대 한 OS 디스크의 크기 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="f9616-134">최소 30GB.</span><span class="sxs-lookup"><span data-stu-id="f9616-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="f9616-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="f9616-135">-NodeVmSize</span></span>
<span data-ttu-id="f9616-136">가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="f9616-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9616-137">-ResourceGroupName</span></span>
<span data-ttu-id="f9616-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9616-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="f9616-139">-SshKeyValue</span></span>
<span data-ttu-id="f9616-140">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="f9616-141">기본적으로 {HOME}/.ssh/id_rsa pub.</span><span class="sxs-lookup"><span data-stu-id="f9616-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="f9616-142">태그</span><span class="sxs-lookup"><span data-stu-id="f9616-142">-Tag</span></span>
<span data-ttu-id="f9616-143">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="f9616-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="f9616-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f9616-144">-Confirm</span></span>
<span data-ttu-id="f9616-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9616-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9616-146">-WhatIf</span></span>
<span data-ttu-id="f9616-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9616-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9616-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9616-149">CommonParameters</span></span>
<span data-ttu-id="f9616-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9616-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9616-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9616-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9616-152">입력</span><span class="sxs-lookup"><span data-stu-id="f9616-152">INPUTS</span></span>

### <span data-ttu-id="f9616-153">않아야</span><span class="sxs-lookup"><span data-stu-id="f9616-153">None</span></span>

## <span data-ttu-id="f9616-154">출력</span><span class="sxs-lookup"><span data-stu-id="f9616-154">OUTPUTS</span></span>

### <span data-ttu-id="f9616-155">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="f9616-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f9616-156">상속자</span><span class="sxs-lookup"><span data-stu-id="f9616-156">NOTES</span></span>

## <span data-ttu-id="f9616-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9616-157">RELATED LINKS</span></span>
