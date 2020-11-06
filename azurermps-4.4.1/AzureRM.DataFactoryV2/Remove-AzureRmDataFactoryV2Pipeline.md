---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538219"
---
# <span data-ttu-id="ad882-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ad882-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="ad882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad882-102">SYNOPSIS</span></span>
<span data-ttu-id="ad882-103">Data Factory에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad882-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad882-104">SYNTAX</span></span>

### <span data-ttu-id="ad882-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad882-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad882-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad882-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad882-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad882-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ad882-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ad882-108">DESCRIPTION</span></span>
<span data-ttu-id="ad882-109">Remove-AzureRmDataFactoryV2Pipeline cmdlet은 Azure Data Factory에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="ad882-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ad882-110">EXAMPLES</span></span>

### <span data-ttu-id="ad882-111">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="ad882-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="ad882-112">이 cmdlet은 WikiADF 이라는 data factory에서 DPWikisample 이라는 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="ad882-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ad882-114">변수</span><span class="sxs-lookup"><span data-stu-id="ad882-114">PARAMETERS</span></span>

### <span data-ttu-id="ad882-115">-확인</span><span class="sxs-lookup"><span data-stu-id="ad882-115">-Confirm</span></span>
<span data-ttu-id="ad882-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad882-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ad882-117">-DataFactoryName</span></span>
<span data-ttu-id="ad882-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ad882-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad882-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ad882-120">-Force</span></span>
<span data-ttu-id="ad882-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ad882-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ad882-122">-Name</span></span>
<span data-ttu-id="ad882-123">제거할 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad882-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad882-124">-InputObject</span></span>
<span data-ttu-id="ad882-125">파이프라인 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="ad882-126">이 cmdlet은이 매개 변수에서 지정 하는 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad882-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad882-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad882-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ad882-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad882-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad882-130">-ResourceId</span></span>
<span data-ttu-id="ad882-131">제거할 파이프라인의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad882-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad882-132">-WhatIf</span></span>
<span data-ttu-id="ad882-133">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad882-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="ad882-134">입력</span><span class="sxs-lookup"><span data-stu-id="ad882-134">INPUTS</span></span>

### <span data-ttu-id="ad882-135">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="ad882-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="ad882-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad882-136">System.String</span></span>


## <span data-ttu-id="ad882-137">출력</span><span class="sxs-lookup"><span data-stu-id="ad882-137">OUTPUTS</span></span>

### <span data-ttu-id="ad882-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ad882-138">System.Object</span></span>

## <span data-ttu-id="ad882-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ad882-139">NOTES</span></span>
<span data-ttu-id="ad882-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="ad882-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ad882-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad882-141">RELATED LINKS</span></span>
[<span data-ttu-id="ad882-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ad882-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ad882-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ad882-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ad882-144">AzureRmDataFactoryV2Pipeline-호출</span><span class="sxs-lookup"><span data-stu-id="ad882-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

