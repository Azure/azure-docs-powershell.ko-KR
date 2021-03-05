---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: ecc68d6f87728f3bccb2d7fe1947c293e6b670d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989632"
---
# <span data-ttu-id="bd8f2-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd8f2-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="bd8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8f2-103">작업 영역이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-103">Updates a workspace.</span></span>

## <span data-ttu-id="bd8f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd8f2-104">SYNTAX</span></span>

### <span data-ttu-id="bd8f2-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd8f2-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd8f2-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="bd8f2-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd8f2-107">설명</span><span class="sxs-lookup"><span data-stu-id="bd8f2-107">DESCRIPTION</span></span>
<span data-ttu-id="bd8f2-108">**Set-AzOperationalInsightsWorkspace** cmdlet은 작업 영역의 구성을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="bd8f2-109">예제</span><span class="sxs-lookup"><span data-stu-id="bd8f2-109">EXAMPLES</span></span>

### <span data-ttu-id="bd8f2-110">예제 1: 이름에 따라 작업 영역 수정</span><span class="sxs-lookup"><span data-stu-id="bd8f2-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="bd8f2-111">이 명령은 ContosoResourceGroup이라는 리소스 그룹의 MyWorkspace라는 작업 영역의 SKU 및 태그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd8f2-112">예제 2: 파이프라인을 사용하여 작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd8f2-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="bd8f2-113">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkSpace라는 작업 영역이 있는 다음 파이프라인 연산자를 사용하여 **Set-AzOperationalInsightsWorkspace** cmdlet에 전달하여 SKU를 Premium으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="bd8f2-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd8f2-114">PARAMETERS</span></span>

### <span data-ttu-id="bd8f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8f2-115">-DefaultProfile</span></span>
<span data-ttu-id="bd8f2-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd8f2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd8f2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bd8f2-117">-Name</span></span>
<span data-ttu-id="bd8f2-118">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f2-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="bd8f2-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="bd8f2-120">작업 영역 섭취에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="bd8f2-121">값은 '사용' 또는 '사용 안 되어' 입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="bd8f2-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="bd8f2-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="bd8f2-123">작업 영역 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="bd8f2-124">값은 '사용' 또는 '사용 안 되어' 입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="bd8f2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd8f2-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd8f2-126">Azure 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f2-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bd8f2-127">-RetentionInDays</span></span>
<span data-ttu-id="bd8f2-128">작업 영역 데이터 보존 기간은 며칠입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-128">The workspace data retention in days.</span></span> <span data-ttu-id="bd8f2-129">730일은 다른 모든 Sku에 대해 허용되는 최대 일입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-129">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f2-130">-Sku</span><span class="sxs-lookup"><span data-stu-id="bd8f2-130">-Sku</span></span>
<span data-ttu-id="bd8f2-131">작업 영역의 서비스 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="bd8f2-132">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="bd8f2-132">Valid values are:</span></span> 
- <span data-ttu-id="bd8f2-133">무료</span><span class="sxs-lookup"><span data-stu-id="bd8f2-133">free</span></span>
- <span data-ttu-id="bd8f2-134">표준</span><span class="sxs-lookup"><span data-stu-id="bd8f2-134">standard</span></span>
- <span data-ttu-id="bd8f2-135">premium</span><span class="sxs-lookup"><span data-stu-id="bd8f2-135">premium</span></span>
- <span data-ttu-id="bd8f2-136">pernode</span><span class="sxs-lookup"><span data-stu-id="bd8f2-136">pernode</span></span>
- <span data-ttu-id="bd8f2-137">독립 실행형</span><span class="sxs-lookup"><span data-stu-id="bd8f2-137">standalone</span></span>
- <span data-ttu-id="bd8f2-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="bd8f2-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f2-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd8f2-139">-Tag</span></span>
<span data-ttu-id="bd8f2-140">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f2-141">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="bd8f2-141">-Workspace</span></span>
<span data-ttu-id="bd8f2-142">업데이트할 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd8f2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8f2-143">CommonParameters</span></span>
<span data-ttu-id="bd8f2-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8f2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8f2-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd8f2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8f2-146">입력</span><span class="sxs-lookup"><span data-stu-id="bd8f2-146">INPUTS</span></span>

### <span data-ttu-id="bd8f2-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd8f2-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bd8f2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bd8f2-148">System.String</span></span>

### <span data-ttu-id="bd8f2-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd8f2-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bd8f2-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd8f2-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bd8f2-151">출력</span><span class="sxs-lookup"><span data-stu-id="bd8f2-151">OUTPUTS</span></span>

### <span data-ttu-id="bd8f2-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd8f2-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="bd8f2-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd8f2-153">NOTES</span></span>

## <span data-ttu-id="bd8f2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd8f2-154">RELATED LINKS</span></span>

[<span data-ttu-id="bd8f2-155">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bd8f2-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="bd8f2-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd8f2-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


