---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711593"
---
# <span data-ttu-id="cf1a6-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf1a6-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="cf1a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1a6-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf1a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf1a6-104">SYNTAX</span></span>

### <span data-ttu-id="cf1a6-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf1a6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf1a6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1a6-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1a6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cf1a6-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf1a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cf1a6-108">DESCRIPTION</span></span>
<span data-ttu-id="cf1a6-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="cf1a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cf1a6-110">EXAMPLES</span></span>

### <span data-ttu-id="cf1a6-111">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="cf1a6-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="cf1a6-112">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cf1a6-113">변수</span><span class="sxs-lookup"><span data-stu-id="cf1a6-113">PARAMETERS</span></span>

### <span data-ttu-id="cf1a6-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="cf1a6-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="cf1a6-115">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="cf1a6-116">-CatalogPricingTier</span></span>
<span data-ttu-id="cf1a6-117">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="cf1a6-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf1a6-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="cf1a6-119">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="cf1a6-120">-확인</span><span class="sxs-lookup"><span data-stu-id="cf1a6-120">-Confirm</span></span>
<span data-ttu-id="cf1a6-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf1a6-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf1a6-122">-DataFactoryName</span></span>
<span data-ttu-id="cf1a6-123">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-124">-설명</span><span class="sxs-lookup"><span data-stu-id="cf1a6-124">-Description</span></span>
<span data-ttu-id="cf1a6-125">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="cf1a6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cf1a6-126">-Force</span></span>
<span data-ttu-id="cf1a6-127">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cf1a6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf1a6-128">-InputObject</span></span>
<span data-ttu-id="cf1a6-129">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-130">-위치</span><span class="sxs-lookup"><span data-stu-id="cf1a6-130">-Location</span></span>
<span data-ttu-id="cf1a6-131">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="cf1a6-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="cf1a6-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="cf1a6-133">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-134">-이름</span><span class="sxs-lookup"><span data-stu-id="cf1a6-134">-Name</span></span>
<span data-ttu-id="cf1a6-135">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="cf1a6-136">-NodeCount</span></span>
<span data-ttu-id="cf1a6-137">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="cf1a6-138">-NodeSize</span></span>
<span data-ttu-id="cf1a6-139">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="cf1a6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1a6-140">-ResourceGroupName</span></span>
<span data-ttu-id="cf1a6-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1a6-142">-ResourceId</span></span>
<span data-ttu-id="cf1a6-143">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-144">-서브넷</span><span class="sxs-lookup"><span data-stu-id="cf1a6-144">-Subnet</span></span>
<span data-ttu-id="cf1a6-145">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1a6-146">-Type</span><span class="sxs-lookup"><span data-stu-id="cf1a6-146">-Type</span></span>
<span data-ttu-id="cf1a6-147">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="cf1a6-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="cf1a6-148">-VNetId</span></span>
<span data-ttu-id="cf1a6-149">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="cf1a6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf1a6-150">-WhatIf</span></span>
<span data-ttu-id="cf1a6-151">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cf1a6-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1a6-152">-DefaultProfile</span></span>
<span data-ttu-id="cf1a6-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf1a6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1a6-154">CommonParameters</span></span>
<span data-ttu-id="cf1a6-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1a6-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1a6-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1a6-157">입력</span><span class="sxs-lookup"><span data-stu-id="cf1a6-157">INPUTS</span></span>

### <span data-ttu-id="cf1a6-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf1a6-158">System.String</span></span>
<span data-ttu-id="cf1a6-159">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cf1a6-160">출력</span><span class="sxs-lookup"><span data-stu-id="cf1a6-160">OUTPUTS</span></span>

### <span data-ttu-id="cf1a6-161">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="cf1a6-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cf1a6-162">상속자</span><span class="sxs-lookup"><span data-stu-id="cf1a6-162">NOTES</span></span>

## <span data-ttu-id="cf1a6-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf1a6-163">RELATED LINKS</span></span>

[<span data-ttu-id="cf1a6-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf1a6-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
