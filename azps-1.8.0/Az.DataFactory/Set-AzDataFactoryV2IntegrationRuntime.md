---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868682"
---
# <span data-ttu-id="ef6d5-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ef6d5-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ef6d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6d5-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="ef6d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef6d5-104">SYNTAX</span></span>

### <span data-ttu-id="ef6d5-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ef6d5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6d5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6d5-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6d5-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6d5-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6d5-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ef6d5-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6d5-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ef6d5-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6d5-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ef6d5-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef6d5-111">설명은</span><span class="sxs-lookup"><span data-stu-id="ef6d5-111">DESCRIPTION</span></span>
<span data-ttu-id="ef6d5-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="ef6d5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ef6d5-113">EXAMPLES</span></span>

### <span data-ttu-id="ef6d5-114">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="ef6d5-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="ef6d5-115">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="ef6d5-116">예제 2: 자체 호스팅 통합 런타임 공유</span><span class="sxs-lookup"><span data-stu-id="ef6d5-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="ef6d5-117">Cmdlet은 공유 통합 런타임을 사용 하기 위해 ADF를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="ef6d5-118">`-SharedIntegrationRuntimeResourceId`매개 변수를 사용 하는 경우에도이를 `-Type` 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="ef6d5-119">Cmdlet을 실행 하기 전에 통합 런타임을 사용할 수 있는 권한을 데이터 팩터리에 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="ef6d5-120">변수</span><span class="sxs-lookup"><span data-stu-id="ef6d5-120">PARAMETERS</span></span>

### <span data-ttu-id="ef6d5-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="ef6d5-121">-AuthKey</span></span>
<span data-ttu-id="ef6d5-122">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="ef6d5-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="ef6d5-124">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="ef6d5-125">-CatalogPricingTier</span></span>
<span data-ttu-id="ef6d5-126">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef6d5-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="ef6d5-128">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ef6d5-129">-DataFactoryName</span></span>
<span data-ttu-id="ef6d5-130">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-130">The data factory name.</span></span>

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

### <span data-ttu-id="ef6d5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6d5-131">-DefaultProfile</span></span>
<span data-ttu-id="ef6d5-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef6d5-133">-설명</span><span class="sxs-lookup"><span data-stu-id="ef6d5-133">-Description</span></span>
<span data-ttu-id="ef6d5-134">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="ef6d5-135">-에디션</span><span class="sxs-lookup"><span data-stu-id="ef6d5-135">-Edition</span></span>
<span data-ttu-id="ef6d5-136">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="ef6d5-137">-Force</span><span class="sxs-lookup"><span data-stu-id="ef6d5-137">-Force</span></span>
<span data-ttu-id="ef6d5-138">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ef6d5-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef6d5-139">-InputObject</span></span>
<span data-ttu-id="ef6d5-140">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="ef6d5-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ef6d5-141">-LicenseType</span></span>
<span data-ttu-id="ef6d5-142">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="ef6d5-143">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="ef6d5-144">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="ef6d5-145">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="ef6d5-146">-위치</span><span class="sxs-lookup"><span data-stu-id="ef6d5-146">-Location</span></span>
<span data-ttu-id="ef6d5-147">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="ef6d5-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="ef6d5-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="ef6d5-149">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-150">-이름</span><span class="sxs-lookup"><span data-stu-id="ef6d5-150">-Name</span></span>
<span data-ttu-id="ef6d5-151">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="ef6d5-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ef6d5-152">-NodeCount</span></span>
<span data-ttu-id="ef6d5-153">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="ef6d5-154">-NodeSize</span></span>
<span data-ttu-id="ef6d5-155">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="ef6d5-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6d5-156">-ResourceGroupName</span></span>
<span data-ttu-id="ef6d5-157">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-157">The resource group name.</span></span>

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

### <span data-ttu-id="ef6d5-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6d5-158">-ResourceId</span></span>
<span data-ttu-id="ef6d5-159">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ef6d5-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="ef6d5-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="ef6d5-161">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="ef6d5-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6d5-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="ef6d5-163">공유 자체 호스팅 통합 런타임의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="ef6d5-164">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ef6d5-164">-Subnet</span></span>
<span data-ttu-id="ef6d5-165">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="ef6d5-166">-Type</span><span class="sxs-lookup"><span data-stu-id="ef6d5-166">-Type</span></span>
<span data-ttu-id="ef6d5-167">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="ef6d5-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="ef6d5-168">-VNetId</span></span>
<span data-ttu-id="ef6d5-169">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="ef6d5-170">-확인</span><span class="sxs-lookup"><span data-stu-id="ef6d5-170">-Confirm</span></span>
<span data-ttu-id="ef6d5-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6d5-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6d5-172">-WhatIf</span></span>
<span data-ttu-id="ef6d5-173">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ef6d5-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6d5-174">CommonParameters</span></span>
<span data-ttu-id="ef6d5-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6d5-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6d5-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6d5-177">입력</span><span class="sxs-lookup"><span data-stu-id="ef6d5-177">INPUTS</span></span>

### <span data-ttu-id="ef6d5-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef6d5-178">System.String</span></span>

### <span data-ttu-id="ef6d5-179">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ef6d5-180">출력</span><span class="sxs-lookup"><span data-stu-id="ef6d5-180">OUTPUTS</span></span>

### <span data-ttu-id="ef6d5-181">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="ef6d5-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ef6d5-182">상속자</span><span class="sxs-lookup"><span data-stu-id="ef6d5-182">NOTES</span></span>

## <span data-ttu-id="ef6d5-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef6d5-183">RELATED LINKS</span></span>

[<span data-ttu-id="ef6d5-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ef6d5-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
