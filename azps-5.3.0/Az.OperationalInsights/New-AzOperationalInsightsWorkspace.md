---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492507"
---
# <span data-ttu-id="1b59a-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b59a-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1b59a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b59a-102">SYNOPSIS</span></span>
<span data-ttu-id="1b59a-103">작업 영역 또는 소프트 삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="1b59a-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="1b59a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b59a-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b59a-105">설명</span><span class="sxs-lookup"><span data-stu-id="1b59a-105">DESCRIPTION</span></span>
<span data-ttu-id="1b59a-106">**New-AzOperationalInsightsWorkspace** cmdlet은 지정된 리소스 그룹 및 위치에 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="1b59a-107">또는 소프트 삭제된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="1b59a-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="1b59a-108">예제</span><span class="sxs-lookup"><span data-stu-id="1b59a-108">EXAMPLES</span></span>

### <span data-ttu-id="1b59a-109">예제 1: 이름으로 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="1b59a-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="1b59a-110">이 명령은 ContosoResourceGroup이라는 리소스 그룹에 MyWorkspace라는 표준 SKU 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1b59a-111">예제 2: 작업 영역 만들기 및 기존 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="1b59a-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="1b59a-112">첫 번째 명령은 Get-AzOperationalInsightsLinkTargets cmdlet을 사용하여 Operational Insights 계정 링크 대상을 확인한 다음, $OILinkTargets 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="1b59a-113">두 번째 명령은 파이프라인 연산자를 사용하여 $OILinkTargets 계정 링크 대상을 **New-AzOperationalInsightsWorkspace** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1b59a-114">이 명령은 MyWorkspace라는 표준 SKU 작업 영역으로, 이 작업 영역의 첫 번째 Operational Insights 계정에 $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="1b59a-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="1b59a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b59a-115">PARAMETERS</span></span>

### <span data-ttu-id="1b59a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b59a-116">-DefaultProfile</span></span>
<span data-ttu-id="1b59a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1b59a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b59a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1b59a-118">-Force</span></span>
<span data-ttu-id="1b59a-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b59a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="1b59a-120">-Location</span></span>
<span data-ttu-id="1b59a-121">작업 영역(예: 미국 동부 또는 유럽 서부)을 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1b59a-122">-Name</span></span>
<span data-ttu-id="1b59a-123">작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-123">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="1b59a-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="1b59a-125">작업 영역 시작에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="1b59a-126">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="1b59a-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="1b59a-128">작업 영역 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="1b59a-129">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-129">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b59a-130">-ResourceGroupName</span></span>
<span data-ttu-id="1b59a-131">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b59a-132">작업 영역은 이 리소스 그룹에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-132">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1b59a-133">-RetentionInDays</span></span>
<span data-ttu-id="1b59a-134">작업 영역 데이터 보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-134">The workspace data retention in days.</span></span> <span data-ttu-id="1b59a-135">다른 모든 SKU에 대해 허용되는 최대값은 730일입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-135">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="1b59a-136">-Sku</span></span>
<span data-ttu-id="1b59a-137">작업 영역의 서비스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="1b59a-138">사용할 값에 대한 자세한 내용은 다음을 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="1b59a-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="1b59a-139">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="1b59a-139">Valid values are:</span></span>
- <span data-ttu-id="1b59a-140">무료</span><span class="sxs-lookup"><span data-stu-id="1b59a-140">free</span></span>
- <span data-ttu-id="1b59a-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="1b59a-141">pergb2018</span></span>
- <span data-ttu-id="1b59a-142">pernode</span><span class="sxs-lookup"><span data-stu-id="1b59a-142">pernode</span></span>
- <span data-ttu-id="1b59a-143">premium</span><span class="sxs-lookup"><span data-stu-id="1b59a-143">premium</span></span>
- <span data-ttu-id="1b59a-144">독립 실행형</span><span class="sxs-lookup"><span data-stu-id="1b59a-144">standalone</span></span>
- <span data-ttu-id="1b59a-145">표준</span><span class="sxs-lookup"><span data-stu-id="1b59a-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b59a-146">-Tag</span></span>
<span data-ttu-id="1b59a-147">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-147">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b59a-148">-Confirm</span></span>
<span data-ttu-id="1b59a-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b59a-150">-WhatIf</span></span>
<span data-ttu-id="1b59a-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1b59a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b59a-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b59a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b59a-153">CommonParameters</span></span>
<span data-ttu-id="1b59a-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b59a-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b59a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b59a-156">입력</span><span class="sxs-lookup"><span data-stu-id="1b59a-156">INPUTS</span></span>

### <span data-ttu-id="1b59a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1b59a-157">System.String</span></span>

### <span data-ttu-id="1b59a-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b59a-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b59a-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b59a-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1b59a-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b59a-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1b59a-161">출력</span><span class="sxs-lookup"><span data-stu-id="1b59a-161">OUTPUTS</span></span>

### <span data-ttu-id="1b59a-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b59a-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1b59a-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b59a-163">NOTES</span></span>

<span data-ttu-id="1b59a-164">새 가격 책정 모델이 릴리스되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-164">A new pricing model has been released.</span></span> <span data-ttu-id="1b59a-165">CSP인 경우 SKU에 "독립 실행형"을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="1b59a-166">SKU는 배후에서 pergb2018로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b59a-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="1b59a-167">자세한 내용은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="1b59a-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="1b59a-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b59a-168">RELATED LINKS</span></span>

[<span data-ttu-id="1b59a-169">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b59a-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="1b59a-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="1b59a-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


