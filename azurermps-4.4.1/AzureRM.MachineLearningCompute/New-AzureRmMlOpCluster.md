---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533060"
---
# <span data-ttu-id="2a17b-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2a17b-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="2a17b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a17b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a17b-103">새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a17b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a17b-104">SYNTAX</span></span>

### <span data-ttu-id="2a17b-105">OperationalizationCluster 인스턴스 정의에서 새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2a17b-106">Cmdlet 입력 매개 변수를 통해 새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2a17b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2a17b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a17b-108">새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="2a17b-109">이렇게 하면 클러스터 개체, 컨테이너 서비스, 필요한 경우, application insights, azure 컨테이너 레지스트리가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="2a17b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2a17b-110">EXAMPLES</span></span>

### <span data-ttu-id="2a17b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a17b-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="2a17b-112">Orchestrator로 azure 컨테이너 서비스와 Kubernetes를 사용 하 여 새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="2a17b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2a17b-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="2a17b-114">로컬에서 새 operationalization 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="2a17b-115">이렇게 하면 azure 컨테이너 레지스트리, application insights 및 저장소 계정이 만들어지지만 컨테이너 서비스는 생성 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="2a17b-116">변수</span><span class="sxs-lookup"><span data-stu-id="2a17b-116">PARAMETERS</span></span>

### <span data-ttu-id="2a17b-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="2a17b-117">-AgentCount</span></span>
<span data-ttu-id="2a17b-118">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="2a17b-119">-AgentVmSize</span></span>
<span data-ttu-id="2a17b-120">ACS 클러스터의 에이전트 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2a17b-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="2a17b-122">Azure 컨테이너 레지스트리에 대 한 URI로,이를 만드는 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a17b-123">-InputObject</span></span>
<span data-ttu-id="2a17b-124">Operationalization 클러스터 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2a17b-125">-ClusterType</span></span>
<span data-ttu-id="2a17b-126">Operationalization 클러스터 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="2a17b-127">-Confirm</span></span>
<span data-ttu-id="2a17b-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a17b-129">-설명</span><span class="sxs-lookup"><span data-stu-id="2a17b-129">-Description</span></span>
<span data-ttu-id="2a17b-130">ACS 클러스터의 마스터 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="2a17b-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="2a17b-132">전역 서비스 구성에 대 한 추가 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="2a17b-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="2a17b-134">업데이트에 대 한 구성 ETag입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-135">-위치</span><span class="sxs-lookup"><span data-stu-id="2a17b-135">-Location</span></span>
<span data-ttu-id="2a17b-136">Operationalization 클러스터의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="2a17b-137">-MasterCount</span></span>
<span data-ttu-id="2a17b-138">ACS 클러스터의 마스터 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-139">-이름</span><span class="sxs-lookup"><span data-stu-id="2a17b-139">-Name</span></span>
<span data-ttu-id="2a17b-140">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="2a17b-141">-OrchestratorType</span></span>
<span data-ttu-id="2a17b-142">ACS 클러스터의 orchestrator 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a17b-143">-ResourceGroupName</span></span>
<span data-ttu-id="2a17b-144">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="2a17b-145">-ClientId</span></span>
<span data-ttu-id="2a17b-146">ACS 클러스터의 orchestrator service principal id입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-147">-비밀</span><span class="sxs-lookup"><span data-stu-id="2a17b-147">-Secret</span></span>
<span data-ttu-id="2a17b-148">ACS 클러스터의 orchestrator service principal secret.</span><span class="sxs-lookup"><span data-stu-id="2a17b-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="2a17b-149">-SslCName</span></span>
<span data-ttu-id="2a17b-150">SSL 인증서에 대 한 CName</span><span class="sxs-lookup"><span data-stu-id="2a17b-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="2a17b-151">-SslCertificate</span></span>
<span data-ttu-id="2a17b-152">Base64 문자열로 인코딩된 PEM 형식의 SSL 인증서 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="2a17b-153">-SslKey</span></span>
<span data-ttu-id="2a17b-154">Base64 문자열로 인코딩된 PEM 형식의 SSL 키 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="2a17b-155">-SslStatus</span></span>
<span data-ttu-id="2a17b-156">SSL 상태</span><span class="sxs-lookup"><span data-stu-id="2a17b-156">SSL status.</span></span>
<span data-ttu-id="2a17b-157">가능한 값은 ' 사용 ' 및 ' 사용 안 함 '입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2a17b-158">-StorageAccount</span></span>
<span data-ttu-id="2a17b-159">저장소 계정 중 하나를 만드는 대신 사용 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a17b-160">-WhatIf</span></span>
<span data-ttu-id="2a17b-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a17b-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a17b-162">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2a17b-163">입력</span><span class="sxs-lookup"><span data-stu-id="2a17b-163">INPUTS</span></span>

### <span data-ttu-id="2a17b-164">않아야</span><span class="sxs-lookup"><span data-stu-id="2a17b-164">None</span></span>


## <span data-ttu-id="2a17b-165">출력</span><span class="sxs-lookup"><span data-stu-id="2a17b-165">OUTPUTS</span></span>

### <span data-ttu-id="2a17b-166">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="2a17b-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="2a17b-167">상속자</span><span class="sxs-lookup"><span data-stu-id="2a17b-167">NOTES</span></span>

## <span data-ttu-id="2a17b-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a17b-168">RELATED LINKS</span></span>

