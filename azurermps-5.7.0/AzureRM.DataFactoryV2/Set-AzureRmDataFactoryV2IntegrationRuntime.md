---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529883"
---
# <span data-ttu-id="bc5f1-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bc5f1-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="bc5f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5f1-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc5f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc5f1-104">SYNTAX</span></span>

### <span data-ttu-id="bc5f1-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc5f1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc5f1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc5f1-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc5f1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="bc5f1-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5f1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bc5f1-108">DESCRIPTION</span></span>
<span data-ttu-id="bc5f1-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="bc5f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bc5f1-110">EXAMPLES</span></span>

### <span data-ttu-id="bc5f1-111">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="bc5f1-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="bc5f1-112">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="bc5f1-113">변수</span><span class="sxs-lookup"><span data-stu-id="bc5f1-113">PARAMETERS</span></span>

### <span data-ttu-id="bc5f1-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="bc5f1-114">-AuthKey</span></span>
<span data-ttu-id="bc5f1-115">자체 호스팅 통합 런타임의 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="bc5f1-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="bc5f1-117">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="bc5f1-118">-CatalogPricingTier</span></span>
<span data-ttu-id="bc5f1-119">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-119">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="bc5f1-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc5f1-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="bc5f1-121">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-121">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="bc5f1-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bc5f1-122">-DataFactoryName</span></span>
<span data-ttu-id="bc5f1-123">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5f1-124">-DefaultProfile</span></span>
<span data-ttu-id="bc5f1-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5f1-126">-설명</span><span class="sxs-lookup"><span data-stu-id="bc5f1-126">-Description</span></span>
<span data-ttu-id="bc5f1-127">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-127">The integration runtime description.</span></span>

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

### <span data-ttu-id="bc5f1-128">-에디션</span><span class="sxs-lookup"><span data-stu-id="bc5f1-128">-Edition</span></span>
<span data-ttu-id="bc5f1-129">표준 또는 엔터프라이즈 일 수 있는 SSIS 통합 런타임의 edition이 지정 되지 않은 경우 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-130">-Force</span><span class="sxs-lookup"><span data-stu-id="bc5f1-130">-Force</span></span>
<span data-ttu-id="bc5f1-131">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="bc5f1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc5f1-132">-InputObject</span></span>
<span data-ttu-id="bc5f1-133">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bc5f1-134">-LicenseType</span></span>
<span data-ttu-id="bc5f1-135">SSIS IR에 대해 선택할 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="bc5f1-136">LicenseIncluded 또는 BasePrice의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="bc5f1-137">Azure 하이브리드 사용 혜택 (AHUB) 가격 책정에 대해 자격이 있는 경우 BasePrice를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="bc5f1-138">그렇지 않은 경우에는 LicenseIncluded를 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-139">-위치</span><span class="sxs-lookup"><span data-stu-id="bc5f1-139">-Location</span></span>
<span data-ttu-id="bc5f1-140">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-140">The integration runtime location.</span></span>

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

### <span data-ttu-id="bc5f1-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="bc5f1-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="bc5f1-142">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="bc5f1-143">-이름</span><span class="sxs-lookup"><span data-stu-id="bc5f1-143">-Name</span></span>
<span data-ttu-id="bc5f1-144">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="bc5f1-145">-NodeCount</span></span>
<span data-ttu-id="bc5f1-146">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-146">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="bc5f1-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="bc5f1-147">-NodeSize</span></span>
<span data-ttu-id="bc5f1-148">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-148">The integration runtime node size.</span></span>

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

### <span data-ttu-id="bc5f1-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc5f1-149">-ResourceGroupName</span></span>
<span data-ttu-id="bc5f1-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc5f1-151">-ResourceId</span></span>
<span data-ttu-id="bc5f1-152">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="bc5f1-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="bc5f1-154">사용자 지정 설치 스크립트를 포함 하는 Azure blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="bc5f1-155">-서브넷</span><span class="sxs-lookup"><span data-stu-id="bc5f1-155">-Subnet</span></span>
<span data-ttu-id="bc5f1-156">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-157">-Type</span><span class="sxs-lookup"><span data-stu-id="bc5f1-157">-Type</span></span>
<span data-ttu-id="bc5f1-158">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5f1-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="bc5f1-159">-VNetId</span></span>
<span data-ttu-id="bc5f1-160">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-160">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="bc5f1-161">-확인</span><span class="sxs-lookup"><span data-stu-id="bc5f1-161">-Confirm</span></span>
<span data-ttu-id="bc5f1-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5f1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5f1-163">-WhatIf</span></span>
<span data-ttu-id="bc5f1-164">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="bc5f1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5f1-165">CommonParameters</span></span>
<span data-ttu-id="bc5f1-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5f1-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5f1-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5f1-168">입력</span><span class="sxs-lookup"><span data-stu-id="bc5f1-168">INPUTS</span></span>

### <span data-ttu-id="bc5f1-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc5f1-169">System.String</span></span>
<span data-ttu-id="bc5f1-170">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="bc5f1-171">출력</span><span class="sxs-lookup"><span data-stu-id="bc5f1-171">OUTPUTS</span></span>

### <span data-ttu-id="bc5f1-172">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="bc5f1-173">상속자</span><span class="sxs-lookup"><span data-stu-id="bc5f1-173">NOTES</span></span>

## <span data-ttu-id="bc5f1-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc5f1-174">RELATED LINKS</span></span>

[<span data-ttu-id="bc5f1-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bc5f1-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
