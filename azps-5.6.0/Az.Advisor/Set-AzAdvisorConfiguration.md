---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 550b9d11cd2f5b0cadb13d76809faa2ac34dc426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966992"
---
# <span data-ttu-id="c2c31-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2c31-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="c2c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c31-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c31-103">Azure Advisor 구성을 업데이트하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="c2c31-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2c31-104">SYNTAX</span></span>

### <span data-ttu-id="c2c31-105">InputObjectRgExcludeParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c2c31-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c31-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c31-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c31-107">설명</span><span class="sxs-lookup"><span data-stu-id="c2c31-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c31-108">Azure Advisor의 구성을 업데이트하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="c2c31-109">구성에는 구독 수준 구성 및 ResourceGroup 수준 구성의 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="c2c31-110">구독 수준 구성: 구독에 대해 이 형식에 대해 하나의 구성만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="c2c31-111">LowCpuThreshold 및 제외 속성은 이 cmdlet을 사용하여 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="c2c31-112">ResourceGroup 수준 구성: 각 ResourceGroup에 대해 하나의 구성만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="c2c31-113">이 cmdlet을 사용하여 제외 속성만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="c2c31-114">예제</span><span class="sxs-lookup"><span data-stu-id="c2c31-114">EXAMPLES</span></span>

###  <span data-ttu-id="c2c31-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2c31-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="c2c31-116">구독 수준 구성에 대한 구성(lowCpuThreshold)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="c2c31-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="c2c31-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="c2c31-118">구독 수준 구성에 대한 구성(lowCpuThreshold, 제외)을 업데이트하고 권장 생성에서 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="c2c31-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="c2c31-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="c2c31-120">권장 생성에서 제외될 resourceGroupName1에 대한 구성(제외)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="c2c31-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="c2c31-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="c2c31-122">파이프라인에서 전달된 권장에 대한 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="c2c31-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2c31-123">PARAMETERS</span></span>

### <span data-ttu-id="c2c31-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c2c31-124">-Confirm</span></span>
<span data-ttu-id="c2c31-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c31-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c31-126">-DefaultProfile</span></span>
<span data-ttu-id="c2c31-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2c31-128">-제외</span><span class="sxs-lookup"><span data-stu-id="c2c31-128">-Exclude</span></span>
<span data-ttu-id="c2c31-129">권장 생성에서 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="c2c31-130">지정되지 않은 경우 제외 속성은 false로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c31-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2c31-131">-InputObject</span></span>
<span data-ttu-id="c2c31-132">powershell 개체 형식 PsAzureAdvisorConfigurationData는 호출에서 Get-AzAdvisorConfiguration 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c31-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="c2c31-133">-LowCpuThreshold</span></span>
<span data-ttu-id="c2c31-134">낮은 Cpu 임계값의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c31-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c31-135">-ResourceGroupName</span></span>
<span data-ttu-id="c2c31-136">구성에 대한 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c31-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c31-137">-WhatIf</span></span>
<span data-ttu-id="c2c31-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c31-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c31-140">CommonParameters</span></span>
<span data-ttu-id="c2c31-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c2c31-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2c31-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c31-143">입력</span><span class="sxs-lookup"><span data-stu-id="c2c31-143">INPUTS</span></span>

### <span data-ttu-id="c2c31-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="c2c31-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="c2c31-145">출력</span><span class="sxs-lookup"><span data-stu-id="c2c31-145">OUTPUTS</span></span>

### <span data-ttu-id="c2c31-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="c2c31-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="c2c31-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2c31-147">NOTES</span></span>

## <span data-ttu-id="c2c31-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2c31-148">RELATED LINKS</span></span>
