---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 020a492ddab075d121025623f5c731bdc71c440b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879369"
---
# <span data-ttu-id="e5898-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5898-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e5898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5898-102">SYNOPSIS</span></span>
<span data-ttu-id="e5898-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="e5898-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5898-104">SYNTAX</span></span>

### <span data-ttu-id="e5898-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e5898-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] 
 [-PublicIPs <String[]>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
 [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="e5898-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5898-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>] [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="e5898-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="e5898-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5898-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e5898-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5898-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e5898-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
 [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="e5898-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e5898-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5898-111">설명은</span><span class="sxs-lookup"><span data-stu-id="e5898-111">DESCRIPTION</span></span>
<span data-ttu-id="e5898-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="e5898-113">예제의</span><span class="sxs-lookup"><span data-stu-id="e5898-113">EXAMPLES</span></span>

### <span data-ttu-id="e5898-114">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="e5898-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="e5898-115">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="e5898-116">예제 2: 자체 호스팅 통합 런타임 공유</span><span class="sxs-lookup"><span data-stu-id="e5898-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="e5898-117">Cmdlet은 공유 통합 런타임을 사용 하기 위해 ADF를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="e5898-118">`-SharedIntegrationRuntimeResourceId`매개 변수를 사용 하는 경우에도이를 `-Type` 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="e5898-119">Cmdlet을 실행 하기 전에 통합 런타임을 사용할 수 있는 권한을 데이터 팩터리에 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="e5898-120">예제 3: Self-Hosted IR을 Azure에 대 한 프록시로 ADF의 SSIS IR로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="e5898-121">Cmdlet 업데이트 Azure-SSIS 통합 런타임을 통해 자체 호스팅 통합 런타임을 데이터 프록시로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="e5898-122">변수</span><span class="sxs-lookup"><span data-stu-id="e5898-122">PARAMETERS</span></span>

### <span data-ttu-id="e5898-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="e5898-123">-AuthKey</span></span>
<span data-ttu-id="e5898-124">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="e5898-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="e5898-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="e5898-126">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="e5898-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="e5898-127">-CatalogPricingTier</span></span>
<span data-ttu-id="e5898-128">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="e5898-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5898-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="e5898-130">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="e5898-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e5898-131">-DataFactoryName</span></span>
<span data-ttu-id="e5898-132">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-132">The data factory name.</span></span>

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

### <span data-ttu-id="e5898-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e5898-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="e5898-134">프록시로 사용 되는 Self-Hosted 통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="e5898-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="e5898-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="e5898-136">Self-Hosted 및 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 준비 데이터 저장소를 참조 하는 Azure Blob 저장소 연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="e5898-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="e5898-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="e5898-138">스테이징 데이터 저장소에서 Self-Hosted와 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 경로를 지정 하지 않으면 기본 컨테이너가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="e5898-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5898-139">-DefaultProfile</span></span>
<span data-ttu-id="e5898-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5898-141">-설명</span><span class="sxs-lookup"><span data-stu-id="e5898-141">-Description</span></span>
<span data-ttu-id="e5898-142">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="e5898-143">-에디션</span><span class="sxs-lookup"><span data-stu-id="e5898-143">-Edition</span></span>
<span data-ttu-id="e5898-144">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="e5898-145">-Force</span><span class="sxs-lookup"><span data-stu-id="e5898-145">-Force</span></span>
<span data-ttu-id="e5898-146">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e5898-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5898-147">-InputObject</span></span>
<span data-ttu-id="e5898-148">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-148">The integration runtime object.</span></span>

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

### <span data-ttu-id="e5898-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e5898-149">-LicenseType</span></span>
<span data-ttu-id="e5898-150">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="e5898-151">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="e5898-152">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5898-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="e5898-153">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5898-153">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="e5898-154">-위치</span><span class="sxs-lookup"><span data-stu-id="e5898-154">-Location</span></span>
<span data-ttu-id="e5898-155">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-155">The integration runtime location.</span></span>

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

### <span data-ttu-id="e5898-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="e5898-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="e5898-157">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="e5898-158">-이름</span><span class="sxs-lookup"><span data-stu-id="e5898-158">-Name</span></span>
<span data-ttu-id="e5898-159">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-159">The integration runtime name.</span></span>

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

### <span data-ttu-id="e5898-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e5898-160">-NodeCount</span></span>
<span data-ttu-id="e5898-161">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-161">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="e5898-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="e5898-162">-NodeSize</span></span>
<span data-ttu-id="e5898-163">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-163">The integration runtime node size.</span></span>

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

### <span data-ttu-id="e5898-164">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="e5898-164">-PublicIPs</span></span>
<span data-ttu-id="e5898-165">통합 런타임에서 사용 하는 정적 공용 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-165">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="e5898-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5898-166">-ResourceGroupName</span></span>
<span data-ttu-id="e5898-167">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-167">The resource group name.</span></span>

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

### <span data-ttu-id="e5898-168">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5898-168">-ResourceId</span></span>
<span data-ttu-id="e5898-169">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-169">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e5898-170">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="e5898-170">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="e5898-171">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-171">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="e5898-172">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="e5898-172">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="e5898-173">공유 자체 호스팅 통합 런타임의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-173">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="e5898-174">-서브넷</span><span class="sxs-lookup"><span data-stu-id="e5898-174">-Subnet</span></span>
<span data-ttu-id="e5898-175">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-175">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="e5898-176">-Type</span><span class="sxs-lookup"><span data-stu-id="e5898-176">-Type</span></span>
<span data-ttu-id="e5898-177">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-177">The integration runtime type.</span></span>

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

### <span data-ttu-id="e5898-178">-VNetId</span><span class="sxs-lookup"><span data-stu-id="e5898-178">-VNetId</span></span>
<span data-ttu-id="e5898-179">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-179">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="e5898-180">-확인</span><span class="sxs-lookup"><span data-stu-id="e5898-180">-Confirm</span></span>
<span data-ttu-id="e5898-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5898-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5898-182">-WhatIf</span></span>
<span data-ttu-id="e5898-183">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-183">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e5898-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5898-184">CommonParameters</span></span>
<span data-ttu-id="e5898-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5898-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5898-186">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5898-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5898-187">입력</span><span class="sxs-lookup"><span data-stu-id="e5898-187">INPUTS</span></span>

### <span data-ttu-id="e5898-188">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5898-188">System.String</span></span>

### <span data-ttu-id="e5898-189">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="e5898-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e5898-190">출력</span><span class="sxs-lookup"><span data-stu-id="e5898-190">OUTPUTS</span></span>

### <span data-ttu-id="e5898-191">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="e5898-191">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e5898-192">상속자</span><span class="sxs-lookup"><span data-stu-id="e5898-192">NOTES</span></span>

## <span data-ttu-id="e5898-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5898-193">RELATED LINKS</span></span>

[<span data-ttu-id="e5898-194">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e5898-194">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
