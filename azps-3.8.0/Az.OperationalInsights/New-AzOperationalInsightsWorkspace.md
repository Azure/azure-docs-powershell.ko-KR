---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 22cc5c18e2c3cf21472426160d667c7890f04d4f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047295"
---
# <span data-ttu-id="2165d-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2165d-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="2165d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2165d-102">SYNOPSIS</span></span>
<span data-ttu-id="2165d-103">작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-103">Creates a workspace.</span></span>

## <span data-ttu-id="2165d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2165d-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2165d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2165d-105">DESCRIPTION</span></span>
<span data-ttu-id="2165d-106">**AzOperationalInsightsWorkspace** cmdlet은 지정 된 리소스 그룹 및 위치에 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="2165d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2165d-107">EXAMPLES</span></span>

### <span data-ttu-id="2165d-108">예제 1: 이름으로 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="2165d-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="2165d-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에 MyWorkspace 라는 표준 SKU 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="2165d-110">예제 2: 작업 영역 만들기 및 기존 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="2165d-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="2165d-111">첫 번째 명령은 Get-AzOperationalInsightsLinkTargets cmdlet을 사용 하 여 Operational Insights 계정 링크 대상을 가져오고이를 $OILinkTargets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="2165d-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $OILinkTargets의 첫 번째 계정 링크 대상을 **새 AzOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2165d-113">이 명령은 $OILinkTargets의 첫 번째 Operational Insights 계정에 연결 되는 MyWorkspace 라는 표준 SKU 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="2165d-114">변수</span><span class="sxs-lookup"><span data-stu-id="2165d-114">PARAMETERS</span></span>

### <span data-ttu-id="2165d-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="2165d-115">-CustomerId</span></span>
<span data-ttu-id="2165d-116">이 작업 영역이 연결 될 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="2165d-117">Get-AzOperationalInsightsLinkTargets cmdlet을 사용 하 여 잠재적 계정을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2165d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2165d-118">-DefaultProfile</span></span>
<span data-ttu-id="2165d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2165d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2165d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2165d-120">-Force</span></span>
<span data-ttu-id="2165d-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2165d-122">-위치</span><span class="sxs-lookup"><span data-stu-id="2165d-122">-Location</span></span>
<span data-ttu-id="2165d-123">작업 영역을 만들 위치를 지정 합니다 (예: 동부 미국 또는 서유럽).</span><span class="sxs-lookup"><span data-stu-id="2165d-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="2165d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="2165d-124">-Name</span></span>
<span data-ttu-id="2165d-125">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="2165d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2165d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2165d-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2165d-128">이 리소스 그룹에 작업 영역이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="2165d-129">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="2165d-129">-RetentionInDays</span></span>
<span data-ttu-id="2165d-130">작업 영역 데이터 보존 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-130">The workspace data retention in days.</span></span> <span data-ttu-id="2165d-131">730 일이 다른 모든 Sku에 허용 되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="2165d-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="2165d-132">-Sku</span></span>
<span data-ttu-id="2165d-133">작업 영역의 서비스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="2165d-134">사용할 값에 대 한 자세한 내용은 확인을 참조 하세요 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="2165d-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="2165d-135">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-135">Valid values are:</span></span>
- <span data-ttu-id="2165d-136">비우거나</span><span class="sxs-lookup"><span data-stu-id="2165d-136">free</span></span>
- <span data-ttu-id="2165d-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="2165d-137">pergb2018</span></span>
- <span data-ttu-id="2165d-138">pernode</span><span class="sxs-lookup"><span data-stu-id="2165d-138">pernode</span></span>
- <span data-ttu-id="2165d-139">premium</span><span class="sxs-lookup"><span data-stu-id="2165d-139">premium</span></span>
- <span data-ttu-id="2165d-140">독립</span><span class="sxs-lookup"><span data-stu-id="2165d-140">standalone</span></span>
- <span data-ttu-id="2165d-141">표준이</span><span class="sxs-lookup"><span data-stu-id="2165d-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2165d-142">태그</span><span class="sxs-lookup"><span data-stu-id="2165d-142">-Tag</span></span>
<span data-ttu-id="2165d-143">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-143">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="2165d-144">-확인</span><span class="sxs-lookup"><span data-stu-id="2165d-144">-Confirm</span></span>
<span data-ttu-id="2165d-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2165d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2165d-146">-WhatIf</span></span>
<span data-ttu-id="2165d-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2165d-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2165d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2165d-149">CommonParameters</span></span>
<span data-ttu-id="2165d-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2165d-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2165d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2165d-152">입력</span><span class="sxs-lookup"><span data-stu-id="2165d-152">INPUTS</span></span>

### <span data-ttu-id="2165d-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2165d-153">System.String</span></span>

### <span data-ttu-id="2165d-154">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2165d-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2165d-155">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2165d-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2165d-156">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="2165d-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2165d-157">출력</span><span class="sxs-lookup"><span data-stu-id="2165d-157">OUTPUTS</span></span>

### <span data-ttu-id="2165d-158">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="2165d-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="2165d-159">상속자</span><span class="sxs-lookup"><span data-stu-id="2165d-159">NOTES</span></span>

<span data-ttu-id="2165d-160">새 가격 책정 모델이 릴리스 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-160">A new pricing model has been released.</span></span> <span data-ttu-id="2165d-161">CSP 인 경우 sku에 대해 "독립 실행형"을 사용 해야 한다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="2165d-162">배후에서 sku는 pergb2018로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2165d-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="2165d-163">자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="2165d-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="2165d-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2165d-164">RELATED LINKS</span></span>

[<span data-ttu-id="2165d-165">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2165d-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
