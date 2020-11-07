---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696966"
---
# <span data-ttu-id="08b70-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="08b70-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="08b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08b70-102">SYNOPSIS</span></span>
<span data-ttu-id="08b70-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="08b70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08b70-104">SYNTAX</span></span>

### <span data-ttu-id="08b70-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="08b70-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08b70-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b70-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="08b70-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b70-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="08b70-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b70-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="08b70-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b70-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="08b70-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08b70-111">설명은</span><span class="sxs-lookup"><span data-stu-id="08b70-111">DESCRIPTION</span></span>
<span data-ttu-id="08b70-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="08b70-113">예제의</span><span class="sxs-lookup"><span data-stu-id="08b70-113">EXAMPLES</span></span>

### <span data-ttu-id="08b70-114">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="08b70-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="08b70-115">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="08b70-116">예제 2: 자체 호스팅 통합 런타임 공유</span><span class="sxs-lookup"><span data-stu-id="08b70-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="08b70-117">Cmdlet은 공유 통합 런타임을 사용 하기 위해 ADF를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="08b70-118">`-SharedIntegrationRuntimeResourceId`매개 변수를 사용 하는 경우에도이를 `-Type` 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="08b70-119">Cmdlet을 실행 하기 전에 통합 런타임을 사용할 수 있는 권한을 데이터 팩터리에 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="08b70-120">예제 3: Self-Hosted IR을 Azure에 대 한 프록시로 ADF의 SSIS IR로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="08b70-121">Cmdlet 업데이트 Azure-SSIS 통합 런타임을 통해 자체 호스팅 통합 런타임을 데이터 프록시로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="08b70-122">변수</span><span class="sxs-lookup"><span data-stu-id="08b70-122">PARAMETERS</span></span>

### <span data-ttu-id="08b70-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="08b70-123">-AuthKey</span></span>
<span data-ttu-id="08b70-124">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="08b70-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="08b70-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="08b70-126">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="08b70-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="08b70-127">-CatalogPricingTier</span></span>
<span data-ttu-id="08b70-128">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="08b70-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="08b70-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="08b70-130">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="08b70-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="08b70-131">-DataFactoryName</span></span>
<span data-ttu-id="08b70-132">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-132">The data factory name.</span></span>

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

### <span data-ttu-id="08b70-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="08b70-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="08b70-134">프록시로 사용 되는 Self-Hosted 통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="08b70-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="08b70-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="08b70-136">Self-Hosted 및 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 준비 데이터 저장소를 참조 하는 Azure Blob 저장소 연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="08b70-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="08b70-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="08b70-138">스테이징 데이터 저장소에서 Self-Hosted와 Azure-SSIS 통합 런타임 간에 데이터를 이동할 때 사용할 경로를 지정 하지 않으면 기본 컨테이너가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="08b70-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b70-139">-DefaultProfile</span></span>
<span data-ttu-id="08b70-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08b70-141">-설명</span><span class="sxs-lookup"><span data-stu-id="08b70-141">-Description</span></span>
<span data-ttu-id="08b70-142">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="08b70-143">-에디션</span><span class="sxs-lookup"><span data-stu-id="08b70-143">-Edition</span></span>
<span data-ttu-id="08b70-144">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="08b70-145">-Force</span><span class="sxs-lookup"><span data-stu-id="08b70-145">-Force</span></span>
<span data-ttu-id="08b70-146">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="08b70-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08b70-147">-InputObject</span></span>
<span data-ttu-id="08b70-148">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-148">The integration runtime object.</span></span>

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

### <span data-ttu-id="08b70-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="08b70-149">-LicenseType</span></span>
<span data-ttu-id="08b70-150">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="08b70-151">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="08b70-152">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="08b70-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="08b70-153">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="08b70-153">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="08b70-154">-위치</span><span class="sxs-lookup"><span data-stu-id="08b70-154">-Location</span></span>
<span data-ttu-id="08b70-155">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-155">The integration runtime location.</span></span>

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

### <span data-ttu-id="08b70-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="08b70-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="08b70-157">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="08b70-158">-이름</span><span class="sxs-lookup"><span data-stu-id="08b70-158">-Name</span></span>
<span data-ttu-id="08b70-159">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-159">The integration runtime name.</span></span>

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

### <span data-ttu-id="08b70-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="08b70-160">-NodeCount</span></span>
<span data-ttu-id="08b70-161">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-161">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="08b70-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="08b70-162">-NodeSize</span></span>
<span data-ttu-id="08b70-163">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-163">The integration runtime node size.</span></span>

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

### <span data-ttu-id="08b70-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b70-164">-ResourceGroupName</span></span>
<span data-ttu-id="08b70-165">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-165">The resource group name.</span></span>

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

### <span data-ttu-id="08b70-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08b70-166">-ResourceId</span></span>
<span data-ttu-id="08b70-167">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-167">The Azure resource ID.</span></span>

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

### <span data-ttu-id="08b70-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="08b70-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="08b70-169">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="08b70-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="08b70-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="08b70-171">공유 자체 호스팅 통합 런타임의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-171">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="08b70-172">-서브넷</span><span class="sxs-lookup"><span data-stu-id="08b70-172">-Subnet</span></span>
<span data-ttu-id="08b70-173">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-173">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="08b70-174">-Type</span><span class="sxs-lookup"><span data-stu-id="08b70-174">-Type</span></span>
<span data-ttu-id="08b70-175">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="08b70-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="08b70-176">-VNetId</span></span>
<span data-ttu-id="08b70-177">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-177">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="08b70-178">-확인</span><span class="sxs-lookup"><span data-stu-id="08b70-178">-Confirm</span></span>
<span data-ttu-id="08b70-179">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b70-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b70-180">-WhatIf</span></span>
<span data-ttu-id="08b70-181">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="08b70-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b70-182">CommonParameters</span></span>
<span data-ttu-id="08b70-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b70-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b70-184">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b70-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b70-185">입력</span><span class="sxs-lookup"><span data-stu-id="08b70-185">INPUTS</span></span>

### <span data-ttu-id="08b70-186">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08b70-186">System.String</span></span>

### <span data-ttu-id="08b70-187">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="08b70-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="08b70-188">출력</span><span class="sxs-lookup"><span data-stu-id="08b70-188">OUTPUTS</span></span>

### <span data-ttu-id="08b70-189">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="08b70-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="08b70-190">상속자</span><span class="sxs-lookup"><span data-stu-id="08b70-190">NOTES</span></span>

## <span data-ttu-id="08b70-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08b70-191">RELATED LINKS</span></span>

[<span data-ttu-id="08b70-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="08b70-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
