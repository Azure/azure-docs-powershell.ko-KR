---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215748"
---
# <span data-ttu-id="84b7e-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="84b7e-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="84b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="84b7e-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="84b7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84b7e-104">SYNTAX</span></span>

### <span data-ttu-id="84b7e-105">SetByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="84b7e-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="84b7e-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="84b7e-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="84b7e-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="84b7e-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="84b7e-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="84b7e-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b7e-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="84b7e-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b7e-113">설명은</span><span class="sxs-lookup"><span data-stu-id="84b7e-113">DESCRIPTION</span></span>
<span data-ttu-id="84b7e-114">**AzSynapseIntegrationRuntime** cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="84b7e-115">예제의</span><span class="sxs-lookup"><span data-stu-id="84b7e-115">EXAMPLES</span></span>

### <span data-ttu-id="84b7e-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="84b7e-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="84b7e-117">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="84b7e-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="84b7e-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="84b7e-119">Cmdlet은 공유 통합 런타임을 사용 하는 작업 영역을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="84b7e-120">`-SharedIntegrationRuntimeResourceId`매개 변수를 사용 하는 경우에도이를 `-Type` 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="84b7e-121">Cmdlet을 실행 하기 전에 통합 런타임을 사용할 수 있는 권한을 작업 영역에 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="84b7e-122">변수</span><span class="sxs-lookup"><span data-stu-id="84b7e-122">PARAMETERS</span></span>

### <span data-ttu-id="84b7e-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="84b7e-123">-AuthKey</span></span>
<span data-ttu-id="84b7e-124">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="84b7e-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="84b7e-126">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="84b7e-127">-CatalogPricingTier</span></span>
<span data-ttu-id="84b7e-128">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84b7e-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="84b7e-130">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="84b7e-131">-DataFlowComputeType</span></span>
<span data-ttu-id="84b7e-132">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 계산 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="84b7e-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="84b7e-134">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 핵심 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="84b7e-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="84b7e-136">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 ttl (time to live) 설정 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="84b7e-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="84b7e-138">프록시로 사용 되는 Self-Hosted 통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="84b7e-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="84b7e-140">Self-Hosted와 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 준비 데이터 저장소를 참조 하는 Azure Blob 저장소 연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="84b7e-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="84b7e-142">스테이징 데이터 저장소에서 Self-Hosted와 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 경로입니다. 지정 하지 않으면 기본 컨테이너가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b7e-143">-DefaultProfile</span></span>
<span data-ttu-id="84b7e-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b7e-145">-설명</span><span class="sxs-lookup"><span data-stu-id="84b7e-145">-Description</span></span>
<span data-ttu-id="84b7e-146">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="84b7e-147">-에디션</span><span class="sxs-lookup"><span data-stu-id="84b7e-147">-Edition</span></span>
<span data-ttu-id="84b7e-148">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="84b7e-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="84b7e-150">사용자 지정 설치 스크립트 없이 구성 및 타사 구성 요소를 설정 하는 데 사용할 수 있는 SSIS 통합 런타임의 빠른 사용자 지정 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-151">-Force</span><span class="sxs-lookup"><span data-stu-id="84b7e-151">-Force</span></span>
<span data-ttu-id="84b7e-152">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="84b7e-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84b7e-153">-InputObject</span></span>
<span data-ttu-id="84b7e-154">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="84b7e-155">-LicenseType</span></span>
<span data-ttu-id="84b7e-156">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="84b7e-157">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="84b7e-158">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="84b7e-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="84b7e-159">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="84b7e-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-160">-위치</span><span class="sxs-lookup"><span data-stu-id="84b7e-160">-Location</span></span>
<span data-ttu-id="84b7e-161">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="84b7e-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="84b7e-163">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-164">-이름</span><span class="sxs-lookup"><span data-stu-id="84b7e-164">-Name</span></span>
<span data-ttu-id="84b7e-165">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="84b7e-166">-NodeCount</span></span>
<span data-ttu-id="84b7e-167">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="84b7e-168">-NodeSize</span></span>
<span data-ttu-id="84b7e-169">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="84b7e-170">-PublicIP</span></span>
<span data-ttu-id="84b7e-171">통합 런타임에서 사용 하는 정적 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b7e-172">-ResourceGroupName</span></span>
<span data-ttu-id="84b7e-173">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84b7e-174">-ResourceId</span></span>
<span data-ttu-id="84b7e-175">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="84b7e-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="84b7e-177">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="84b7e-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="84b7e-179">공유 자체 호스팅 통합 런타임의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-180">-서브넷</span><span class="sxs-lookup"><span data-stu-id="84b7e-180">-Subnet</span></span>
<span data-ttu-id="84b7e-181">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-182">-Type</span><span class="sxs-lookup"><span data-stu-id="84b7e-182">-Type</span></span>
<span data-ttu-id="84b7e-183">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="84b7e-184">-VNetId</span></span>
<span data-ttu-id="84b7e-185">통합 런타임이 연결 되는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84b7e-186">-WorkspaceName</span></span>
<span data-ttu-id="84b7e-187">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="84b7e-188">-WorkspaceObject</span></span>
<span data-ttu-id="84b7e-189">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b7e-190">-확인</span><span class="sxs-lookup"><span data-stu-id="84b7e-190">-Confirm</span></span>
<span data-ttu-id="84b7e-191">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b7e-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b7e-192">-WhatIf</span></span>
<span data-ttu-id="84b7e-193">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b7e-194">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b7e-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b7e-195">CommonParameters</span></span>
<span data-ttu-id="84b7e-196">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84b7e-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b7e-197">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="84b7e-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b7e-198">입력</span><span class="sxs-lookup"><span data-stu-id="84b7e-198">INPUTS</span></span>

### <span data-ttu-id="84b7e-199">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="84b7e-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="84b7e-200">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="84b7e-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="84b7e-201">출력</span><span class="sxs-lookup"><span data-stu-id="84b7e-201">OUTPUTS</span></span>

### <span data-ttu-id="84b7e-202">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="84b7e-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="84b7e-203">상속자</span><span class="sxs-lookup"><span data-stu-id="84b7e-203">NOTES</span></span>

## <span data-ttu-id="84b7e-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84b7e-204">RELATED LINKS</span></span>
