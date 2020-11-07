---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711218"
---
# <span data-ttu-id="e9f48-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="e9f48-101">New-AzureRmAks</span></span>

## <span data-ttu-id="e9f48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f48-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f48-103">관리 되는 Kubernetes 클러스터를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9f48-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f48-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e9f48-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f48-106">관리 되는 Kubernetes 클러스터를 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e9f48-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e9f48-107">EXAMPLES</span></span>

### <span data-ttu-id="e9f48-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9f48-108">Example 1</span></span>
<span data-ttu-id="e9f48-109">기본 매개 변수를 사용 하 여 관리 되는 Kubernetes 클러스터 새로 만들기</span><span class="sxs-lookup"><span data-stu-id="e9f48-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e9f48-110">변수</span><span class="sxs-lookup"><span data-stu-id="e9f48-110">PARAMETERS</span></span>

### <span data-ttu-id="e9f48-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="e9f48-111">-AdminUserName</span></span>
<span data-ttu-id="e9f48-112">Linux 가상 컴퓨터의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9f48-113">-AsJob</span></span>
<span data-ttu-id="e9f48-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e9f48-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-115">-Clidandsecret</span><span class="sxs-lookup"><span data-stu-id="e9f48-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="e9f48-116">AAD 응용 프로그램/서비스 사용자와 연결 된 클라이언트 id 및 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f48-117">-DefaultProfile</span></span>
<span data-ttu-id="e9f48-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e9f48-119">-DnsNamePrefix</span></span>
<span data-ttu-id="e9f48-120">클러스터의 DNS 이름 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e9f48-121">-Force</span></span>
<span data-ttu-id="e9f48-122">클러스터를 이미 존재 하는 경우에도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e9f48-123">-KubernetesVersion</span></span>
<span data-ttu-id="e9f48-124">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-125">-위치</span><span class="sxs-lookup"><span data-stu-id="e9f48-125">-Location</span></span>
<span data-ttu-id="e9f48-126">클러스터에 대 한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-126">Azure location for the cluster.</span></span>
<span data-ttu-id="e9f48-127">리소스 그룹의 위치가 기본적으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-128">-이름</span><span class="sxs-lookup"><span data-stu-id="e9f48-128">-Name</span></span>
<span data-ttu-id="e9f48-129">Kubernetes 관리 되는 클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e9f48-130">-NodeCount</span></span>
<span data-ttu-id="e9f48-131">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e9f48-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="e9f48-133">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="e9f48-134">-NodeVmSize</span></span>
<span data-ttu-id="e9f48-135">가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f48-136">-ResourceGroupName</span></span>
<span data-ttu-id="e9f48-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e9f48-138">-SshKeyValue</span></span>
<span data-ttu-id="e9f48-139">SSH 키 파일 값 또는 키 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="e9f48-140">기본적으로 {HOME}/.ssh/id_rsa pub.</span><span class="sxs-lookup"><span data-stu-id="e9f48-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-141">태그</span><span class="sxs-lookup"><span data-stu-id="e9f48-141">-Tag</span></span>
<span data-ttu-id="e9f48-142">리소스에 적용할 태그</span><span class="sxs-lookup"><span data-stu-id="e9f48-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-143">-확인</span><span class="sxs-lookup"><span data-stu-id="e9f48-143">-Confirm</span></span>
<span data-ttu-id="e9f48-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f48-145">-WhatIf</span></span>
<span data-ttu-id="e9f48-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f48-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f48-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f48-148">CommonParameters</span></span>
<span data-ttu-id="e9f48-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9f48-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f48-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f48-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f48-151">입력</span><span class="sxs-lookup"><span data-stu-id="e9f48-151">INPUTS</span></span>

### <span data-ttu-id="e9f48-152">않아야</span><span class="sxs-lookup"><span data-stu-id="e9f48-152">None</span></span>

## <span data-ttu-id="e9f48-153">출력</span><span class="sxs-lookup"><span data-stu-id="e9f48-153">OUTPUTS</span></span>

### <span data-ttu-id="e9f48-154">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="e9f48-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e9f48-155">상속자</span><span class="sxs-lookup"><span data-stu-id="e9f48-155">NOTES</span></span>

## <span data-ttu-id="e9f48-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9f48-156">RELATED LINKS</span></span>
