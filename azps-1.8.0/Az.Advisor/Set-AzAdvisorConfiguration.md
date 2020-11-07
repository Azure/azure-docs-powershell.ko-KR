---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689219"
---
# <span data-ttu-id="e7992-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7992-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="e7992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7992-102">SYNOPSIS</span></span>
<span data-ttu-id="e7992-103">Azure Advisor 구성을 업데이트 하거나 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="e7992-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7992-104">SYNTAX</span></span>

### <span data-ttu-id="e7992-105">InputObjectRgExcludeParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7992-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7992-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7992-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7992-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7992-107">DESCRIPTION</span></span>
<span data-ttu-id="e7992-108">Azure Advisor의 구성을 업데이트 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="e7992-109">두 가지 유형의 구성을 제공 합니다 (구독 수준 구성 및 ResourceGroup 수준 구성).</span><span class="sxs-lookup"><span data-stu-id="e7992-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="e7992-110">구독 수준 구성: 구독에 대해이 유형의 구성은 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="e7992-111">LowCpuThreshold 및 Exclude 속성은이 cmdlet을 사용 하 여 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="e7992-112">ResourceGroup 수준 구성: 각 ResourceGroup에 대해 하나의 구성만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="e7992-113">이 cmdlet을 사용 하 여 Exclude 속성만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="e7992-114">예제의</span><span class="sxs-lookup"><span data-stu-id="e7992-114">EXAMPLES</span></span>

###  <span data-ttu-id="e7992-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7992-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e7992-116">구독 수준 구성에 대 한 구성 (lowCpuThreshold)을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="e7992-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="e7992-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e7992-118">구독 수준 구성에 대 한 구성 (lowCpuThreshold, exclude)을 업데이트 하 고 권장 생성에서 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="e7992-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="e7992-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e7992-120">추천 생성에서 제외할 resourceGroupName1에 대 한 구성 (제외)을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="e7992-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="e7992-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e7992-122">파이프라인에서 전달 된 주어진 권장 구성에 대 한 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="e7992-123">변수</span><span class="sxs-lookup"><span data-stu-id="e7992-123">PARAMETERS</span></span>

### <span data-ttu-id="e7992-124">-확인</span><span class="sxs-lookup"><span data-stu-id="e7992-124">-Confirm</span></span>
<span data-ttu-id="e7992-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7992-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7992-126">-DefaultProfile</span></span>
<span data-ttu-id="e7992-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7992-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="e7992-128">-Exclude</span></span>
<span data-ttu-id="e7992-129">추천 세대에서 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="e7992-130">지정 하지 않으면 exclude 속성이 false로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="e7992-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7992-131">-InputObject</span></span>
<span data-ttu-id="e7992-132">Get-AzAdvisorConfiguration 호출에서 반환 된 powershell 개체 유형 PsAzureAdvisorConfigurationData.</span><span class="sxs-lookup"><span data-stu-id="e7992-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="e7992-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="e7992-133">-LowCpuThreshold</span></span>
<span data-ttu-id="e7992-134">낮은 Cpu 임계값에 대 한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="e7992-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7992-135">-ResourceGroupName</span></span>
<span data-ttu-id="e7992-136">구성에 대 한 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="e7992-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7992-137">-WhatIf</span></span>
<span data-ttu-id="e7992-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7992-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7992-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7992-140">CommonParameters</span></span>
<span data-ttu-id="e7992-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7992-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7992-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7992-143">입력</span><span class="sxs-lookup"><span data-stu-id="e7992-143">INPUTS</span></span>

### <span data-ttu-id="e7992-144">PsAzureAdvisorConfigurationData를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="e7992-145">출력</span><span class="sxs-lookup"><span data-stu-id="e7992-145">OUTPUTS</span></span>

### <span data-ttu-id="e7992-146">PsAzureAdvisorConfigurationData를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e7992-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="e7992-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e7992-147">NOTES</span></span>

## <span data-ttu-id="e7992-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7992-148">RELATED LINKS</span></span>
