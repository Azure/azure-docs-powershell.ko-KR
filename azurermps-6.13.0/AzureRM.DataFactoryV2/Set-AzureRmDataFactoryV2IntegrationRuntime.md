---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aae3b830a55b5a2a7683aa1608d15eb4a49a49fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536672"
---
# <span data-ttu-id="0139b-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0139b-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="0139b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0139b-102">SYNOPSIS</span></span>
<span data-ttu-id="0139b-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0139b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0139b-104">SYNTAX</span></span>

### <span data-ttu-id="0139b-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0139b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0139b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0139b-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0139b-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="0139b-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0139b-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0139b-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0139b-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0139b-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0139b-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0139b-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0139b-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0139b-111">DESCRIPTION</span></span>
<span data-ttu-id="0139b-112">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-112">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="0139b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0139b-113">EXAMPLES</span></span>

### <span data-ttu-id="0139b-114">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="0139b-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="0139b-115">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="0139b-116">예제 2: 자체 호스팅 통합 런타임 공유</span><span class="sxs-lookup"><span data-stu-id="0139b-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="0139b-117">Cmdlet은 공유 통합 런타임을 사용 하기 위해 ADF를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="0139b-118">`-SharedIntegrationRuntimeResourceId`매개 변수를 사용 하는 경우에도이를 `-Type` 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="0139b-119">Cmdlet을 실행 하기 전에 통합 런타임을 사용할 수 있는 권한을 데이터 팩터리에 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="0139b-120">변수</span><span class="sxs-lookup"><span data-stu-id="0139b-120">PARAMETERS</span></span>

### <span data-ttu-id="0139b-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="0139b-121">-AuthKey</span></span>
<span data-ttu-id="0139b-122">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="0139b-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="0139b-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="0139b-124">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="0139b-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="0139b-125">-CatalogPricingTier</span></span>
<span data-ttu-id="0139b-126">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="0139b-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0139b-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="0139b-128">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="0139b-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0139b-129">-DataFactoryName</span></span>
<span data-ttu-id="0139b-130">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-130">The data factory name.</span></span>

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

### <span data-ttu-id="0139b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0139b-131">-DefaultProfile</span></span>
<span data-ttu-id="0139b-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0139b-133">-설명</span><span class="sxs-lookup"><span data-stu-id="0139b-133">-Description</span></span>
<span data-ttu-id="0139b-134">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="0139b-135">-에디션</span><span class="sxs-lookup"><span data-stu-id="0139b-135">-Edition</span></span>
<span data-ttu-id="0139b-136">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="0139b-137">-Force</span><span class="sxs-lookup"><span data-stu-id="0139b-137">-Force</span></span>
<span data-ttu-id="0139b-138">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0139b-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0139b-139">-InputObject</span></span>
<span data-ttu-id="0139b-140">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="0139b-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0139b-141">-LicenseType</span></span>
<span data-ttu-id="0139b-142">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="0139b-143">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="0139b-144">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="0139b-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="0139b-145">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="0139b-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="0139b-146">-위치</span><span class="sxs-lookup"><span data-stu-id="0139b-146">-Location</span></span>
<span data-ttu-id="0139b-147">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="0139b-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="0139b-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="0139b-149">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="0139b-150">-이름</span><span class="sxs-lookup"><span data-stu-id="0139b-150">-Name</span></span>
<span data-ttu-id="0139b-151">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="0139b-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="0139b-152">-NodeCount</span></span>
<span data-ttu-id="0139b-153">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="0139b-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="0139b-154">-NodeSize</span></span>
<span data-ttu-id="0139b-155">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="0139b-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0139b-156">-ResourceGroupName</span></span>
<span data-ttu-id="0139b-157">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-157">The resource group name.</span></span>

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

### <span data-ttu-id="0139b-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0139b-158">-ResourceId</span></span>
<span data-ttu-id="0139b-159">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0139b-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="0139b-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="0139b-161">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="0139b-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="0139b-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="0139b-163">공유 자체 호스팅 통합 런타임의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="0139b-164">-서브넷</span><span class="sxs-lookup"><span data-stu-id="0139b-164">-Subnet</span></span>
<span data-ttu-id="0139b-165">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="0139b-166">-Type</span><span class="sxs-lookup"><span data-stu-id="0139b-166">-Type</span></span>
<span data-ttu-id="0139b-167">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="0139b-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="0139b-168">-VNetId</span></span>
<span data-ttu-id="0139b-169">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="0139b-170">-확인</span><span class="sxs-lookup"><span data-stu-id="0139b-170">-Confirm</span></span>
<span data-ttu-id="0139b-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0139b-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0139b-172">-WhatIf</span></span>
<span data-ttu-id="0139b-173">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0139b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0139b-174">CommonParameters</span></span>
<span data-ttu-id="0139b-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0139b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0139b-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0139b-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0139b-177">입력</span><span class="sxs-lookup"><span data-stu-id="0139b-177">INPUTS</span></span>

### <span data-ttu-id="0139b-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0139b-178">System.String</span></span>

### <span data-ttu-id="0139b-179">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="0139b-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0139b-180">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0139b-180">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0139b-181">출력</span><span class="sxs-lookup"><span data-stu-id="0139b-181">OUTPUTS</span></span>

### <span data-ttu-id="0139b-182">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="0139b-182">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0139b-183">상속자</span><span class="sxs-lookup"><span data-stu-id="0139b-183">NOTES</span></span>

## <span data-ttu-id="0139b-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0139b-184">RELATED LINKS</span></span>

[<span data-ttu-id="0139b-185">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0139b-185">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
