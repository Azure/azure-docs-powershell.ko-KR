---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534983"
---
# <span data-ttu-id="286f1-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="286f1-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="286f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286f1-102">SYNOPSIS</span></span>
<span data-ttu-id="286f1-103">Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="286f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="286f1-104">SYNTAX</span></span>

### <span data-ttu-id="286f1-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="286f1-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="286f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="286f1-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="286f1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="286f1-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="286f1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="286f1-108">DESCRIPTION</span></span>
<span data-ttu-id="286f1-109">Remove-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="286f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="286f1-110">EXAMPLES</span></span>

### <span data-ttu-id="286f1-111">예제 1: 데이터 집합 제거</span><span class="sxs-lookup"><span data-stu-id="286f1-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="286f1-112">이 명령은 WikiADF 이라는 data factory에서 DAWikiAggregatedData 이라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="286f1-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="286f1-114">변수</span><span class="sxs-lookup"><span data-stu-id="286f1-114">PARAMETERS</span></span>

### <span data-ttu-id="286f1-115">-확인</span><span class="sxs-lookup"><span data-stu-id="286f1-115">-Confirm</span></span>
<span data-ttu-id="286f1-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286f1-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="286f1-117">-DataFactoryName</span></span>
<span data-ttu-id="286f1-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="286f1-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 dataset을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="286f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="286f1-120">-InputObject</span></span>
<span data-ttu-id="286f1-121">제거할 데이터 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="286f1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="286f1-122">-Force</span></span>
<span data-ttu-id="286f1-123">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="286f1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="286f1-124">-Name</span></span>
<span data-ttu-id="286f1-125">제거할 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="286f1-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="286f1-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="286f1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="286f1-129">-ResourceId</span></span>
<span data-ttu-id="286f1-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="286f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286f1-131">-WhatIf</span></span>
<span data-ttu-id="286f1-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="286f1-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="286f1-133">입력</span><span class="sxs-lookup"><span data-stu-id="286f1-133">INPUTS</span></span>

### <span data-ttu-id="286f1-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="286f1-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="286f1-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="286f1-135">System.String</span></span>


## <span data-ttu-id="286f1-136">출력</span><span class="sxs-lookup"><span data-stu-id="286f1-136">OUTPUTS</span></span>

### <span data-ttu-id="286f1-137">System. 개체</span><span class="sxs-lookup"><span data-stu-id="286f1-137">System.Object</span></span>

## <span data-ttu-id="286f1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="286f1-138">NOTES</span></span>
<span data-ttu-id="286f1-139">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="286f1-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="286f1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="286f1-140">RELATED LINKS</span></span>
[<span data-ttu-id="286f1-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="286f1-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="286f1-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="286f1-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
