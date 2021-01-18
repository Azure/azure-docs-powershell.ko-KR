---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495617"
---
# <span data-ttu-id="69c09-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="69c09-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="69c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c09-102">SYNOPSIS</span></span>
<span data-ttu-id="69c09-103">Data Factory에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="69c09-104">구문</span><span class="sxs-lookup"><span data-stu-id="69c09-104">SYNTAX</span></span>

### <span data-ttu-id="69c09-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="69c09-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c09-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="69c09-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c09-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="69c09-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c09-108">설명</span><span class="sxs-lookup"><span data-stu-id="69c09-108">DESCRIPTION</span></span>
<span data-ttu-id="69c09-109">Remove-AzDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="69c09-110">예제</span><span class="sxs-lookup"><span data-stu-id="69c09-110">EXAMPLES</span></span>

### <span data-ttu-id="69c09-111">예제 1: 데이터 세트 제거</span><span class="sxs-lookup"><span data-stu-id="69c09-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="69c09-112">이 명령은 WikiADF라는 데이터 팩터리에서 DAWikiAggregatedData라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="69c09-113">이 명령은 10진수의 $True.</span><span class="sxs-lookup"><span data-stu-id="69c09-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="69c09-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69c09-114">PARAMETERS</span></span>

### <span data-ttu-id="69c09-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="69c09-115">-DataFactoryName</span></span>
<span data-ttu-id="69c09-116">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="69c09-117">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c09-118">-DefaultProfile</span></span>
<span data-ttu-id="69c09-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c09-120">-Force</span><span class="sxs-lookup"><span data-stu-id="69c09-120">-Force</span></span>
<span data-ttu-id="69c09-121">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="69c09-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69c09-122">-InputObject</span></span>
<span data-ttu-id="69c09-123">제거할 데이터 세트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-124">-Name</span><span class="sxs-lookup"><span data-stu-id="69c09-124">-Name</span></span>
<span data-ttu-id="69c09-125">제거할 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c09-126">-ResourceGroupName</span></span>
<span data-ttu-id="69c09-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="69c09-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69c09-129">-ResourceId</span></span>
<span data-ttu-id="69c09-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69c09-131">-Confirm</span></span>
<span data-ttu-id="69c09-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c09-133">-WhatIf</span></span>
<span data-ttu-id="69c09-134">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c09-135">CommonParameters</span></span>
<span data-ttu-id="69c09-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69c09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c09-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="69c09-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c09-138">입력</span><span class="sxs-lookup"><span data-stu-id="69c09-138">INPUTS</span></span>

### <span data-ttu-id="69c09-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="69c09-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="69c09-140">System.String</span><span class="sxs-lookup"><span data-stu-id="69c09-140">System.String</span></span>

## <span data-ttu-id="69c09-141">출력</span><span class="sxs-lookup"><span data-stu-id="69c09-141">OUTPUTS</span></span>

### <span data-ttu-id="69c09-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="69c09-142">System.Void</span></span>

## <span data-ttu-id="69c09-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69c09-143">NOTES</span></span>
<span data-ttu-id="69c09-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="69c09-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="69c09-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69c09-145">RELATED LINKS</span></span>

[<span data-ttu-id="69c09-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="69c09-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="69c09-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="69c09-147">Set-AzDataFactoryV2Dataset</span></span>]()
