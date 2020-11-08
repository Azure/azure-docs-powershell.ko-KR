---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214172"
---
# <span data-ttu-id="33e8b-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="33e8b-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="33e8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="33e8b-103">Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="33e8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33e8b-104">SYNTAX</span></span>

### <span data-ttu-id="33e8b-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="33e8b-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33e8b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33e8b-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33e8b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33e8b-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33e8b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="33e8b-108">DESCRIPTION</span></span>
<span data-ttu-id="33e8b-109">Remove-AzDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="33e8b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="33e8b-110">EXAMPLES</span></span>

### <span data-ttu-id="33e8b-111">예제 1: 데이터 집합 제거</span><span class="sxs-lookup"><span data-stu-id="33e8b-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="33e8b-112">이 명령은 WikiADF 이라는 data factory에서 DAWikiAggregatedData 이라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="33e8b-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="33e8b-114">변수</span><span class="sxs-lookup"><span data-stu-id="33e8b-114">PARAMETERS</span></span>

### <span data-ttu-id="33e8b-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33e8b-115">-DataFactoryName</span></span>
<span data-ttu-id="33e8b-116">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="33e8b-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 dataset을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="33e8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e8b-118">-DefaultProfile</span></span>
<span data-ttu-id="33e8b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e8b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="33e8b-120">-Force</span></span>
<span data-ttu-id="33e8b-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="33e8b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33e8b-122">-InputObject</span></span>
<span data-ttu-id="33e8b-123">제거할 데이터 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="33e8b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="33e8b-124">-Name</span></span>
<span data-ttu-id="33e8b-125">제거할 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="33e8b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e8b-126">-ResourceGroupName</span></span>
<span data-ttu-id="33e8b-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="33e8b-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="33e8b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33e8b-129">-ResourceId</span></span>
<span data-ttu-id="33e8b-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="33e8b-131">-확인</span><span class="sxs-lookup"><span data-stu-id="33e8b-131">-Confirm</span></span>
<span data-ttu-id="33e8b-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33e8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33e8b-133">-WhatIf</span></span>
<span data-ttu-id="33e8b-134">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="33e8b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e8b-135">CommonParameters</span></span>
<span data-ttu-id="33e8b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33e8b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e8b-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e8b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e8b-138">입력</span><span class="sxs-lookup"><span data-stu-id="33e8b-138">INPUTS</span></span>

### <span data-ttu-id="33e8b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="33e8b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="33e8b-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33e8b-140">System.String</span></span>

## <span data-ttu-id="33e8b-141">출력</span><span class="sxs-lookup"><span data-stu-id="33e8b-141">OUTPUTS</span></span>

### <span data-ttu-id="33e8b-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="33e8b-142">System.Void</span></span>

## <span data-ttu-id="33e8b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="33e8b-143">NOTES</span></span>
<span data-ttu-id="33e8b-144">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="33e8b-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="33e8b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33e8b-145">RELATED LINKS</span></span>

[<span data-ttu-id="33e8b-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="33e8b-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="33e8b-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="33e8b-147">Set-AzDataFactoryV2Dataset</span></span>]()
