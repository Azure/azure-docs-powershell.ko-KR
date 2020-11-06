---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538208"
---
# <span data-ttu-id="3b7b1-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b7b1-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3b7b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7b1-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b7b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b7b1-104">SYNTAX</span></span>

### <span data-ttu-id="3b7b1-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3b7b1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b7b1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b7b1-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b7b1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3b7b1-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="3b7b1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3b7b1-108">DESCRIPTION</span></span>
<span data-ttu-id="3b7b1-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet은 특정 매개 변수를 사용 하 여 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="3b7b1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3b7b1-110">EXAMPLES</span></span>

### <span data-ttu-id="3b7b1-111">예제 1: 통합 런타임 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="3b7b1-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="3b7b1-112">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3b7b1-113">변수</span><span class="sxs-lookup"><span data-stu-id="3b7b1-113">PARAMETERS</span></span>

### <span data-ttu-id="3b7b1-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="3b7b1-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="3b7b1-115">통합 런타임의 카탈로그 데이터베이스 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-115">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="3b7b1-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="3b7b1-116">-CatalogPricingTier</span></span>
<span data-ttu-id="3b7b1-117">통합 런타임의 카탈로그 데이터베이스 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="3b7b1-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7b1-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="3b7b1-119">통합 런타임의 카탈로그 데이터베이스 서버 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="3b7b1-120">-확인</span><span class="sxs-lookup"><span data-stu-id="3b7b1-120">-Confirm</span></span>
<span data-ttu-id="3b7b1-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b7b1-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3b7b1-122">-DataFactoryName</span></span>
<span data-ttu-id="3b7b1-123">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-123">The data factory name.</span></span>

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

### <span data-ttu-id="3b7b1-124">-설명</span><span class="sxs-lookup"><span data-stu-id="3b7b1-124">-Description</span></span>
<span data-ttu-id="3b7b1-125">통합 런타임 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="3b7b1-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3b7b1-126">-Force</span></span>
<span data-ttu-id="3b7b1-127">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3b7b1-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b7b1-128">-InputObject</span></span>
<span data-ttu-id="3b7b1-129">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-129">The integration runtime object.</span></span>

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

### <span data-ttu-id="3b7b1-130">-위치</span><span class="sxs-lookup"><span data-stu-id="3b7b1-130">-Location</span></span>
<span data-ttu-id="3b7b1-131">통합 런타임 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="3b7b1-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="3b7b1-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="3b7b1-133">관리 전용 통합 런타임에 대 한 노드당 최대 병렬 실행 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="3b7b1-134">-이름</span><span class="sxs-lookup"><span data-stu-id="3b7b1-134">-Name</span></span>
<span data-ttu-id="3b7b1-135">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-135">The integration runtime name.</span></span>

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

### <span data-ttu-id="3b7b1-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="3b7b1-136">-NodeCount</span></span>
<span data-ttu-id="3b7b1-137">통합 런타임의 대상 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-137">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="3b7b1-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="3b7b1-138">-NodeSize</span></span>
<span data-ttu-id="3b7b1-139">통합 런타임 노드 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="3b7b1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b7b1-140">-ResourceGroupName</span></span>
<span data-ttu-id="3b7b1-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-141">The resource group name.</span></span>

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

### <span data-ttu-id="3b7b1-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b7b1-142">-ResourceId</span></span>
<span data-ttu-id="3b7b1-143">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-143">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3b7b1-144">-서브넷</span><span class="sxs-lookup"><span data-stu-id="3b7b1-144">-Subnet</span></span>
<span data-ttu-id="3b7b1-145">VNet의 서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-145">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="3b7b1-146">-Type</span><span class="sxs-lookup"><span data-stu-id="3b7b1-146">-Type</span></span>
<span data-ttu-id="3b7b1-147">통합 런타임 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="3b7b1-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="3b7b1-148">-VNetId</span></span>
<span data-ttu-id="3b7b1-149">통합 런타임이 조인 하는 VNet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="3b7b1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b7b1-150">-WhatIf</span></span>
<span data-ttu-id="3b7b1-151">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="3b7b1-152">입력</span><span class="sxs-lookup"><span data-stu-id="3b7b1-152">INPUTS</span></span>

### <span data-ttu-id="3b7b1-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3b7b1-153">System.String</span></span>
<span data-ttu-id="3b7b1-154">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3b7b1-155">출력</span><span class="sxs-lookup"><span data-stu-id="3b7b1-155">OUTPUTS</span></span>

### <span data-ttu-id="3b7b1-156">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="3b7b1-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3b7b1-157">상속자</span><span class="sxs-lookup"><span data-stu-id="3b7b1-157">NOTES</span></span>

## <span data-ttu-id="3b7b1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b7b1-158">RELATED LINKS</span></span>
[<span data-ttu-id="3b7b1-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b7b1-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
