---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867526"
---
# <span data-ttu-id="58dae-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="58dae-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="58dae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58dae-102">SYNOPSIS</span></span>
<span data-ttu-id="58dae-103">새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="58dae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58dae-104">SYNTAX</span></span>

### <span data-ttu-id="58dae-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="58dae-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58dae-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="58dae-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58dae-107">설명은</span><span class="sxs-lookup"><span data-stu-id="58dae-107">DESCRIPTION</span></span>
<span data-ttu-id="58dae-108">새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="58dae-109">이렇게 하면 클러스터 개체, 컨테이너 서비스, 필요한 경우, application insights, azure 컨테이너 레지스트리가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="58dae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="58dae-110">EXAMPLES</span></span>

### <span data-ttu-id="58dae-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="58dae-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="58dae-112">Orchestrator로 azure 컨테이너 서비스와 Kubernetes를 사용 하 여 새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="58dae-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="58dae-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="58dae-114">로컬에서 새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="58dae-115">이렇게 하면 azure 컨테이너 레지스트리, application insights 및 저장소 계정이 만들어지지만 컨테이너 서비스는 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="58dae-116">변수</span><span class="sxs-lookup"><span data-stu-id="58dae-116">PARAMETERS</span></span>

### <span data-ttu-id="58dae-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="58dae-117">-AgentCount</span></span>
<span data-ttu-id="58dae-118">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="58dae-119">-AgentVmSize</span></span>
<span data-ttu-id="58dae-120">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="58dae-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="58dae-122">Azure 컨테이너 레지스트리에 대 한 URI로,이를 만드는 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="58dae-123">-ClientId</span></span>
<span data-ttu-id="58dae-124">ACS 클러스터의 orchestrator service principal id입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="58dae-125">-ClusterType</span></span>
<span data-ttu-id="58dae-126">Operationalization 클러스터 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58dae-127">-DefaultProfile</span></span>
<span data-ttu-id="58dae-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58dae-129">-설명</span><span class="sxs-lookup"><span data-stu-id="58dae-129">-Description</span></span>
<span data-ttu-id="58dae-130">ACS 클러스터의 마스터 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="58dae-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="58dae-132">전역 서비스 구성에 대 한 추가 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="58dae-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="58dae-134">업데이트에 대 한 구성 ETag입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58dae-135">-InputObject</span></span>
<span data-ttu-id="58dae-136">Operationalization 클러스터 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-137">-위치</span><span class="sxs-lookup"><span data-stu-id="58dae-137">-Location</span></span>
<span data-ttu-id="58dae-138">Operationalization 클러스터의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="58dae-139">-MasterCount</span></span>
<span data-ttu-id="58dae-140">ACS 클러스터의 마스터 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-141">-이름</span><span class="sxs-lookup"><span data-stu-id="58dae-141">-Name</span></span>
<span data-ttu-id="58dae-142">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-142">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="58dae-143">-OrchestratorType</span></span>
<span data-ttu-id="58dae-144">ACS 클러스터의 orchestrator 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58dae-145">-ResourceGroupName</span></span>
<span data-ttu-id="58dae-146">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-146">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-147">-비밀</span><span class="sxs-lookup"><span data-stu-id="58dae-147">-Secret</span></span>
<span data-ttu-id="58dae-148">ACS 클러스터의 orchestrator service principal secret.</span><span class="sxs-lookup"><span data-stu-id="58dae-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="58dae-149">-SslCertificate</span></span>
<span data-ttu-id="58dae-150">Base64 문자열로 인코딩된 PEM 형식의 SSL 인증서 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="58dae-151">-SslCName</span></span>
<span data-ttu-id="58dae-152">SSL 인증서에 대 한 CName</span><span class="sxs-lookup"><span data-stu-id="58dae-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="58dae-153">-SslKey</span></span>
<span data-ttu-id="58dae-154">Base64 문자열로 인코딩된 PEM 형식의 SSL 키 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="58dae-155">-SslStatus</span></span>
<span data-ttu-id="58dae-156">SSL 상태</span><span class="sxs-lookup"><span data-stu-id="58dae-156">SSL status.</span></span>
<span data-ttu-id="58dae-157">가능한 값은 ' 사용 ' 및 ' 사용 안 함 '입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="58dae-158">-StorageAccount</span></span>
<span data-ttu-id="58dae-159">저장소 계정 중 하나를 만드는 대신 사용 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58dae-160">-확인</span><span class="sxs-lookup"><span data-stu-id="58dae-160">-Confirm</span></span>
<span data-ttu-id="58dae-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58dae-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58dae-162">-WhatIf</span></span>
<span data-ttu-id="58dae-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58dae-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58dae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58dae-165">CommonParameters</span></span>
<span data-ttu-id="58dae-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58dae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58dae-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58dae-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58dae-168">입력</span><span class="sxs-lookup"><span data-stu-id="58dae-168">INPUTS</span></span>

### <span data-ttu-id="58dae-169">않아야</span><span class="sxs-lookup"><span data-stu-id="58dae-169">None</span></span>

## <span data-ttu-id="58dae-170">출력</span><span class="sxs-lookup"><span data-stu-id="58dae-170">OUTPUTS</span></span>

### <span data-ttu-id="58dae-171">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="58dae-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="58dae-172">상속자</span><span class="sxs-lookup"><span data-stu-id="58dae-172">NOTES</span></span>

## <span data-ttu-id="58dae-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58dae-173">RELATED LINKS</span></span>
