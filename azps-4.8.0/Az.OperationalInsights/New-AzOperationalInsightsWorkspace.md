---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8515bf4085fcd03d87aa15c3da649fe318b94966
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405009"
---
# <span data-ttu-id="ee5de-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ee5de-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="ee5de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee5de-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5de-103">작업 영역 생성</span><span class="sxs-lookup"><span data-stu-id="ee5de-103">Creates a workspace.</span></span>

## <span data-ttu-id="ee5de-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee5de-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee5de-105">설명</span><span class="sxs-lookup"><span data-stu-id="ee5de-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5de-106">**New-AzOperationalInsightsWorkspace** cmdlet은 지정된 리소스 그룹 및 위치에 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="ee5de-107">예제</span><span class="sxs-lookup"><span data-stu-id="ee5de-107">EXAMPLES</span></span>

### <span data-ttu-id="ee5de-108">예제 1: 이름으로 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="ee5de-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="ee5de-109">이 명령은 ContosoResourceGroup이라는 리소스 그룹에 MyWorkspace라는 표준 SKU 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee5de-110">예제 2: 작업 영역 만들기 및 기존 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="ee5de-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="ee5de-111">첫 번째 명령은 Get-AzOperationalInsightsLinkTargets cmdlet을 사용하여 Operational Insights 계정 링크 대상을 확인한 다음, $OILinkTargets 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="ee5de-112">두 번째 명령은 파이프라인 연산자를 사용하여 $OILinkTargets 계정 링크 대상을 **New-AzOperationalInsightsWorkspace** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ee5de-113">이 명령은 MyWorkspace라는 표준 SKU 작업 영역으로, 이 작업 영역의 첫 번째 Operational Insights 계정에 $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="ee5de-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="ee5de-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee5de-114">PARAMETERS</span></span>

### <span data-ttu-id="ee5de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5de-115">-DefaultProfile</span></span>
<span data-ttu-id="ee5de-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ee5de-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee5de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ee5de-117">-Force</span></span>
<span data-ttu-id="ee5de-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee5de-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ee5de-119">-Location</span></span>
<span data-ttu-id="ee5de-120">작업 영역(예: 미국 동부 또는 유럽 서부)을 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="ee5de-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ee5de-121">-Name</span></span>
<span data-ttu-id="ee5de-122">작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="ee5de-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="ee5de-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="ee5de-124">작업 영역 시작에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="ee5de-125">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="ee5de-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="ee5de-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="ee5de-127">작업 영역 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="ee5de-128">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="ee5de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5de-129">-ResourceGroupName</span></span>
<span data-ttu-id="ee5de-130">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee5de-131">작업 영역은 이 리소스 그룹에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="ee5de-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ee5de-132">-RetentionInDays</span></span>
<span data-ttu-id="ee5de-133">작업 영역 데이터 보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-133">The workspace data retention in days.</span></span> <span data-ttu-id="ee5de-134">730일은 다른 모든 SKU에 허용되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="ee5de-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="ee5de-135">-Sku</span></span>
<span data-ttu-id="ee5de-136">작업 영역의 서비스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="ee5de-137">사용할 값에 대한 자세한 내용은 다음을 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="ee5de-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="ee5de-138">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="ee5de-138">Valid values are:</span></span>
- <span data-ttu-id="ee5de-139">무료</span><span class="sxs-lookup"><span data-stu-id="ee5de-139">free</span></span>
- <span data-ttu-id="ee5de-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="ee5de-140">pergb2018</span></span>
- <span data-ttu-id="ee5de-141">pernode</span><span class="sxs-lookup"><span data-stu-id="ee5de-141">pernode</span></span>
- <span data-ttu-id="ee5de-142">premium</span><span class="sxs-lookup"><span data-stu-id="ee5de-142">premium</span></span>
- <span data-ttu-id="ee5de-143">독립 실행형</span><span class="sxs-lookup"><span data-stu-id="ee5de-143">standalone</span></span>
- <span data-ttu-id="ee5de-144">표준</span><span class="sxs-lookup"><span data-stu-id="ee5de-144">standard</span></span>

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

### <span data-ttu-id="ee5de-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee5de-145">-Tag</span></span>
<span data-ttu-id="ee5de-146">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="ee5de-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee5de-147">-Confirm</span></span>
<span data-ttu-id="ee5de-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5de-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5de-149">-WhatIf</span></span>
<span data-ttu-id="ee5de-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ee5de-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5de-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5de-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5de-152">CommonParameters</span></span>
<span data-ttu-id="ee5de-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5de-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee5de-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5de-155">입력</span><span class="sxs-lookup"><span data-stu-id="ee5de-155">INPUTS</span></span>

### <span data-ttu-id="ee5de-156">System.String</span><span class="sxs-lookup"><span data-stu-id="ee5de-156">System.String</span></span>

### <span data-ttu-id="ee5de-157">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ee5de-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ee5de-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ee5de-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ee5de-159">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ee5de-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ee5de-160">출력</span><span class="sxs-lookup"><span data-stu-id="ee5de-160">OUTPUTS</span></span>

### <span data-ttu-id="ee5de-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ee5de-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="ee5de-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee5de-162">NOTES</span></span>

<span data-ttu-id="ee5de-163">새 가격 책정 모델이 릴리스되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-163">A new pricing model has been released.</span></span> <span data-ttu-id="ee5de-164">CSP인 경우 SKU에 "독립 실행형"을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="ee5de-165">SKU는 배후에서 pergb2018로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee5de-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="ee5de-166">자세한 내용은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="ee5de-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="ee5de-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee5de-167">RELATED LINKS</span></span>

[<span data-ttu-id="ee5de-168">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ee5de-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



