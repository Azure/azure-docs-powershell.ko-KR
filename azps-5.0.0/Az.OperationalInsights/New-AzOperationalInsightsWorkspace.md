---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310682"
---
# <span data-ttu-id="08415-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="08415-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="08415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08415-102">SYNOPSIS</span></span>
<span data-ttu-id="08415-103">작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08415-103">Creates a workspace.</span></span>

## <span data-ttu-id="08415-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08415-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08415-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08415-105">DESCRIPTION</span></span>
<span data-ttu-id="08415-106">**AzOperationalInsightsWorkspace** cmdlet은 지정 된 리소스 그룹 및 위치에 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08415-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="08415-107">예제의</span><span class="sxs-lookup"><span data-stu-id="08415-107">EXAMPLES</span></span>

### <span data-ttu-id="08415-108">예제 1: 이름으로 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="08415-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="08415-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에 MyWorkspace 라는 표준 SKU 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08415-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="08415-110">예제 2: 작업 영역 만들기 및 기존 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="08415-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="08415-111">첫 번째 명령은 Get-AzOperationalInsightsLinkTargets cmdlet을 사용 하 여 Operational Insights 계정 링크 대상을 가져오고이를 $OILinkTargets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="08415-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $OILinkTargets의 첫 번째 계정 링크 대상을 **새 AzOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="08415-113">이 명령은 $OILinkTargets의 첫 번째 Operational Insights 계정에 연결 되는 MyWorkspace 라는 표준 SKU 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08415-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="08415-114">변수</span><span class="sxs-lookup"><span data-stu-id="08415-114">PARAMETERS</span></span>

### <span data-ttu-id="08415-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08415-115">-DefaultProfile</span></span>
<span data-ttu-id="08415-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08415-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08415-117">-Force</span><span class="sxs-lookup"><span data-stu-id="08415-117">-Force</span></span>
<span data-ttu-id="08415-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08415-119">-위치</span><span class="sxs-lookup"><span data-stu-id="08415-119">-Location</span></span>
<span data-ttu-id="08415-120">작업 영역을 만들 위치를 지정 합니다 (예: 동부 미국 또는 서유럽).</span><span class="sxs-lookup"><span data-stu-id="08415-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="08415-121">-이름</span><span class="sxs-lookup"><span data-stu-id="08415-121">-Name</span></span>
<span data-ttu-id="08415-122">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="08415-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="08415-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="08415-124">작업 영역 수집에 액세스 하는 데 사용 되는 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="08415-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="08415-125">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="08415-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="08415-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="08415-127">작업 영역 쿼리에 액세스 하는 데 사용 되는 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="08415-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="08415-128">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="08415-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08415-129">-ResourceGroupName</span></span>
<span data-ttu-id="08415-130">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="08415-131">이 리소스 그룹에 작업 영역이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="08415-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="08415-132">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="08415-132">-RetentionInDays</span></span>
<span data-ttu-id="08415-133">작업 영역 데이터 보존 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="08415-133">The workspace data retention in days.</span></span> <span data-ttu-id="08415-134">730 일이 다른 모든 Sku에 허용 되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="08415-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="08415-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="08415-135">-Sku</span></span>
<span data-ttu-id="08415-136">작업 영역의 서비스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="08415-137">사용할 값에 대 한 자세한 내용은 확인을 참조 하세요 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="08415-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="08415-138">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="08415-138">Valid values are:</span></span>
- <span data-ttu-id="08415-139">비우거나</span><span class="sxs-lookup"><span data-stu-id="08415-139">free</span></span>
- <span data-ttu-id="08415-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="08415-140">pergb2018</span></span>
- <span data-ttu-id="08415-141">pernode</span><span class="sxs-lookup"><span data-stu-id="08415-141">pernode</span></span>
- <span data-ttu-id="08415-142">premium</span><span class="sxs-lookup"><span data-stu-id="08415-142">premium</span></span>
- <span data-ttu-id="08415-143">독립</span><span class="sxs-lookup"><span data-stu-id="08415-143">standalone</span></span>
- <span data-ttu-id="08415-144">표준이</span><span class="sxs-lookup"><span data-stu-id="08415-144">standard</span></span>

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

### <span data-ttu-id="08415-145">태그</span><span class="sxs-lookup"><span data-stu-id="08415-145">-Tag</span></span>
<span data-ttu-id="08415-146">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="08415-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="08415-147">-확인</span><span class="sxs-lookup"><span data-stu-id="08415-147">-Confirm</span></span>
<span data-ttu-id="08415-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08415-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08415-149">-WhatIf</span></span>
<span data-ttu-id="08415-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08415-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08415-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08415-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08415-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08415-152">CommonParameters</span></span>
<span data-ttu-id="08415-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08415-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08415-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08415-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08415-155">입력</span><span class="sxs-lookup"><span data-stu-id="08415-155">INPUTS</span></span>

### <span data-ttu-id="08415-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08415-156">System.String</span></span>

### <span data-ttu-id="08415-157">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08415-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08415-158">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="08415-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="08415-159">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="08415-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="08415-160">출력</span><span class="sxs-lookup"><span data-stu-id="08415-160">OUTPUTS</span></span>

### <span data-ttu-id="08415-161">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="08415-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="08415-162">상속자</span><span class="sxs-lookup"><span data-stu-id="08415-162">NOTES</span></span>

<span data-ttu-id="08415-163">새 가격 책정 모델이 릴리스 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="08415-163">A new pricing model has been released.</span></span> <span data-ttu-id="08415-164">CSP 인 경우 sku에 대해 "독립 실행형"을 사용 해야 한다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="08415-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="08415-165">배후에서 sku는 pergb2018로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08415-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="08415-166">자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="08415-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="08415-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08415-167">RELATED LINKS</span></span>

[<span data-ttu-id="08415-168">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08415-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="08415-169">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="08415-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


