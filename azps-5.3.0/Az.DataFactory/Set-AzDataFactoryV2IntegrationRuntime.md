---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493509"
---
# <span data-ttu-id="27a41-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27a41-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="27a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a41-102">SYNOPSIS</span></span>
<span data-ttu-id="27a41-103">통합 런타임 업데이트</span><span class="sxs-lookup"><span data-stu-id="27a41-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="27a41-104">구문</span><span class="sxs-lookup"><span data-stu-id="27a41-104">SYNTAX</span></span>

### <span data-ttu-id="27a41-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="27a41-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="27a41-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27a41-106">ByResourceId</span></span>
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

### <span data-ttu-id="27a41-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="27a41-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a41-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="27a41-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a41-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="27a41-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="27a41-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="27a41-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a41-111">설명</span><span class="sxs-lookup"><span data-stu-id="27a41-111">DESCRIPTION</span></span>
<span data-ttu-id="27a41-112">이 Set-AzDataFactoryV2IntegrationRuntime cmdlet은 통합 런타임에 특정 매개 변수를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="27a41-113">예제</span><span class="sxs-lookup"><span data-stu-id="27a41-113">EXAMPLES</span></span>

### <span data-ttu-id="27a41-114">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="27a41-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="27a41-115">cmdlet은 'test-selfhost-ir'이라는 통합 런타임에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="27a41-116">예제 2: 자체 호스팅 통합 런타임 공유</span><span class="sxs-lookup"><span data-stu-id="27a41-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="27a41-117">이 cmdlet은 공유 통합 런타임 사용에 ADF를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="27a41-118">매개 `-SharedIntegrationRuntimeResourceId` 변수를 사용하는 경우 `-Type` 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="27a41-119">cmdlet을 실행하기 전에 통합 런타임 사용 권한을 데이터 팩터리에 부여해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="27a41-120">예제 3: ADF에서 Self-Hosted AZURE-SSIS IR에 대한 프록시로 IR을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="27a41-121">cmdlet은 자체 호스팅 통합 런타임을 데이터 프록시로 사용하기 위해 Azure-SSIS 통합 런타임을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="27a41-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27a41-122">PARAMETERS</span></span>

### <span data-ttu-id="27a41-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="27a41-123">-AuthKey</span></span>
<span data-ttu-id="27a41-124">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="27a41-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="27a41-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="27a41-126">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="27a41-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="27a41-127">-CatalogPricingTier</span></span>
<span data-ttu-id="27a41-128">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="27a41-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="27a41-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="27a41-130">통합 런타임의 카탈로그 데이터베이스 서버 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="27a41-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="27a41-131">-DataFactoryName</span></span>
<span data-ttu-id="27a41-132">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-132">The data factory name.</span></span>

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

### <span data-ttu-id="27a41-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="27a41-133">-DataFlowComputeType</span></span>
<span data-ttu-id="27a41-134">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 계산 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="27a41-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="27a41-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="27a41-136">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 코어 수입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="27a41-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="27a41-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="27a41-138">데이터 흐름 작업을 실행할 데이터 흐름 클러스터의 Time to Live(분) 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="27a41-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="27a41-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="27a41-140">프록시로 Self-Hosted 통합 런타임 이름</span><span class="sxs-lookup"><span data-stu-id="27a41-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="27a41-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="27a41-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="27a41-142">Azure와 Azure-SSIS Integration Runtime 간에 데이터를 이동하는 경우 사용할 스테이징 데이터 저장소를 Self-Hosted Azure Blob Storage 연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="27a41-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="27a41-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="27a41-144">스테이징 데이터 저장소의 경로는 Self-Hosted Azure-SSIS Integration Runtime 간에 데이터를 이동하는 경우 사용할 경로입니다. 지정하지 않은 경우 기본 컨테이너가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="27a41-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a41-145">-DefaultProfile</span></span>
<span data-ttu-id="27a41-146">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27a41-147">-Description</span><span class="sxs-lookup"><span data-stu-id="27a41-147">-Description</span></span>
<span data-ttu-id="27a41-148">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="27a41-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="27a41-149">-Edition</span></span>
<span data-ttu-id="27a41-150">표준 또는 엔터프라이즈일 수 있는 SSIS 통합 런타임 버전은 지정되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="27a41-151">-Force</span><span class="sxs-lookup"><span data-stu-id="27a41-151">-Force</span></span>
<span data-ttu-id="27a41-152">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="27a41-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27a41-153">-InputObject</span></span>
<span data-ttu-id="27a41-154">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="27a41-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="27a41-155">-LicenseType</span></span>
<span data-ttu-id="27a41-156">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="27a41-157">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="27a41-158">AHUB(Azure 하이브리드 사용 혜택) 가격 책정 자격이 있는 경우 BasePrice를 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="27a41-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="27a41-159">그렇지 않은 경우 LicenseIncluded를 선택해 주세요.</span><span class="sxs-lookup"><span data-stu-id="27a41-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="27a41-160">-Location</span><span class="sxs-lookup"><span data-stu-id="27a41-160">-Location</span></span>
<span data-ttu-id="27a41-161">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="27a41-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="27a41-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="27a41-163">관리되는 전용 통합 런타임에 대한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="27a41-164">-Name</span><span class="sxs-lookup"><span data-stu-id="27a41-164">-Name</span></span>
<span data-ttu-id="27a41-165">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="27a41-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="27a41-166">-NodeCount</span></span>
<span data-ttu-id="27a41-167">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="27a41-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="27a41-168">-NodeSize</span></span>
<span data-ttu-id="27a41-169">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="27a41-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="27a41-170">-PublicIPs</span></span>
<span data-ttu-id="27a41-171">통합 런타임에서 사용할 고정 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="27a41-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a41-172">-ResourceGroupName</span></span>
<span data-ttu-id="27a41-173">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-173">The resource group name.</span></span>

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

### <span data-ttu-id="27a41-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27a41-174">-ResourceId</span></span>
<span data-ttu-id="27a41-175">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="27a41-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="27a41-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="27a41-177">사용자 지정 설치 스크립트를 포함하는 Azure Blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="27a41-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="27a41-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="27a41-179">공유 자체 호스팅 통합 런타임의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="27a41-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="27a41-180">-Subnet</span></span>
<span data-ttu-id="27a41-181">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="27a41-182">-Type</span><span class="sxs-lookup"><span data-stu-id="27a41-182">-Type</span></span>
<span data-ttu-id="27a41-183">통합 런타임 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="27a41-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="27a41-184">-VNetId</span></span>
<span data-ttu-id="27a41-185">통합 런타임이 조인하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="27a41-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27a41-186">-Confirm</span></span>
<span data-ttu-id="27a41-187">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a41-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a41-188">-WhatIf</span></span>
<span data-ttu-id="27a41-189">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="27a41-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a41-190">CommonParameters</span></span>
<span data-ttu-id="27a41-191">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27a41-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a41-192">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27a41-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a41-193">입력</span><span class="sxs-lookup"><span data-stu-id="27a41-193">INPUTS</span></span>

### <span data-ttu-id="27a41-194">System.String</span><span class="sxs-lookup"><span data-stu-id="27a41-194">System.String</span></span>

### <span data-ttu-id="27a41-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27a41-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="27a41-196">출력</span><span class="sxs-lookup"><span data-stu-id="27a41-196">OUTPUTS</span></span>

### <span data-ttu-id="27a41-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27a41-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="27a41-198">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27a41-198">NOTES</span></span>

## <span data-ttu-id="27a41-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27a41-199">RELATED LINKS</span></span>

[<span data-ttu-id="27a41-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="27a41-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
