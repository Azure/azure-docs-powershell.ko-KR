---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305999"
---
# <span data-ttu-id="82cf7-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="82cf7-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="82cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="82cf7-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="82cf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82cf7-104">SYNTAX</span></span>

### <span data-ttu-id="82cf7-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="82cf7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82cf7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82cf7-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cf7-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="82cf7-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cf7-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="82cf7-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cf7-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="82cf7-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cf7-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="82cf7-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82cf7-111">설명은</span><span class="sxs-lookup"><span data-stu-id="82cf7-111">DESCRIPTION</span></span>
<span data-ttu-id="82cf7-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="82cf7-113">예제의</span><span class="sxs-lookup"><span data-stu-id="82cf7-113">EXAMPLES</span></span>

### <span data-ttu-id="82cf7-114">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="82cf7-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="82cf7-115">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="82cf7-116">예제 2: 자체 호스팅 통합 런타임 공유</span><span class="sxs-lookup"><span data-stu-id="82cf7-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="82cf7-117">Cmdlet은 공유 통합 런타임을 사용 하기 위해 ADF를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="82cf7-118">`-SharedIntegrationRuntimeResourceId`매개 변수를 사용 하는 경우에도이를 `-Type` 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="82cf7-119">Cmdlet을 실행 하기 전에 통합 런타임을 사용할 수 있는 권한을 데이터 팩터리에 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="82cf7-120">예제 3: Self-Hosted IR을 Azure에 대 한 프록시로 ADF의 SSIS IR로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    PublicIPs                         : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="82cf7-121">Cmdlet 업데이트 Azure-SSIS 통합 런타임을 통해 자체 호스팅 통합 런타임을 데이터 프록시로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="82cf7-122">변수</span><span class="sxs-lookup"><span data-stu-id="82cf7-122">PARAMETERS</span></span>

### <span data-ttu-id="82cf7-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="82cf7-123">-AuthKey</span></span>
<span data-ttu-id="82cf7-124">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="82cf7-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="82cf7-126">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="82cf7-127">-CatalogPricingTier</span></span>
<span data-ttu-id="82cf7-128">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="82cf7-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="82cf7-130">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82cf7-131">-DataFactoryName</span></span>
<span data-ttu-id="82cf7-132">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="82cf7-133">-DataFlowComputeType</span></span>
<span data-ttu-id="82cf7-134">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 계산 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="82cf7-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="82cf7-136">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 핵심 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-136">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="82cf7-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="82cf7-138">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 ttl (time to live) 설정 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="82cf7-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="82cf7-140">프록시로 사용 되는 Self-Hosted 통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="82cf7-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="82cf7-142">Self-Hosted 및 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 준비 데이터 저장소를 참조 하는 Azure Blob 저장소 연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="82cf7-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="82cf7-144">스테이징 데이터 저장소에서 Self-Hosted와 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 경로를 지정 하지 않으면 기본 컨테이너가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cf7-145">-DefaultProfile</span></span>
<span data-ttu-id="82cf7-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82cf7-147">-설명</span><span class="sxs-lookup"><span data-stu-id="82cf7-147">-Description</span></span>
<span data-ttu-id="82cf7-148">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="82cf7-149">-에디션</span><span class="sxs-lookup"><span data-stu-id="82cf7-149">-Edition</span></span>
<span data-ttu-id="82cf7-150">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-151">-Force</span><span class="sxs-lookup"><span data-stu-id="82cf7-151">-Force</span></span>
<span data-ttu-id="82cf7-152">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="82cf7-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82cf7-153">-InputObject</span></span>
<span data-ttu-id="82cf7-154">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="82cf7-155">-LicenseType</span></span>
<span data-ttu-id="82cf7-156">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="82cf7-157">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="82cf7-158">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="82cf7-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="82cf7-159">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="82cf7-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-160">-위치</span><span class="sxs-lookup"><span data-stu-id="82cf7-160">-Location</span></span>
<span data-ttu-id="82cf7-161">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-161">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="82cf7-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="82cf7-163">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-164">-이름</span><span class="sxs-lookup"><span data-stu-id="82cf7-164">-Name</span></span>
<span data-ttu-id="82cf7-165">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="82cf7-166">-NodeCount</span></span>
<span data-ttu-id="82cf7-167">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="82cf7-168">-NodeSize</span></span>
<span data-ttu-id="82cf7-169">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="82cf7-170">-PublicIPs</span></span>
<span data-ttu-id="82cf7-171">통합 런타임에서 사용 하는 정적 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82cf7-172">-ResourceGroupName</span></span>
<span data-ttu-id="82cf7-173">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-173">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82cf7-174">-ResourceId</span></span>
<span data-ttu-id="82cf7-175">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-175">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="82cf7-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="82cf7-177">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="82cf7-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="82cf7-179">공유 자체 호스팅 통합 런타임의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-180">-서브넷</span><span class="sxs-lookup"><span data-stu-id="82cf7-180">-Subnet</span></span>
<span data-ttu-id="82cf7-181">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-182">-Type</span><span class="sxs-lookup"><span data-stu-id="82cf7-182">-Type</span></span>
<span data-ttu-id="82cf7-183">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="82cf7-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="82cf7-184">-VNetId</span></span>
<span data-ttu-id="82cf7-185">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-185">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82cf7-186">-확인</span><span class="sxs-lookup"><span data-stu-id="82cf7-186">-Confirm</span></span>
<span data-ttu-id="82cf7-187">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cf7-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cf7-188">-WhatIf</span></span>
<span data-ttu-id="82cf7-189">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="82cf7-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cf7-190">CommonParameters</span></span>
<span data-ttu-id="82cf7-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82cf7-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cf7-192">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82cf7-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cf7-193">입력</span><span class="sxs-lookup"><span data-stu-id="82cf7-193">INPUTS</span></span>

### <span data-ttu-id="82cf7-194">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82cf7-194">System.String</span></span>

### <span data-ttu-id="82cf7-195">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="82cf7-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="82cf7-196">출력</span><span class="sxs-lookup"><span data-stu-id="82cf7-196">OUTPUTS</span></span>

### <span data-ttu-id="82cf7-197">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="82cf7-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="82cf7-198">상속자</span><span class="sxs-lookup"><span data-stu-id="82cf7-198">NOTES</span></span>

## <span data-ttu-id="82cf7-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82cf7-199">RELATED LINKS</span></span>

[<span data-ttu-id="82cf7-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="82cf7-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
