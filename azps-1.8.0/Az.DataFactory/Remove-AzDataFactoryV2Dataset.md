---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 8d1a4dfcaaa101a87fc687e78b8086823be7caab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701128"
---
# <span data-ttu-id="3c79f-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3c79f-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="3c79f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c79f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c79f-103">Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="3c79f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c79f-104">SYNTAX</span></span>

### <span data-ttu-id="3c79f-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3c79f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c79f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c79f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c79f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c79f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c79f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3c79f-108">DESCRIPTION</span></span>
<span data-ttu-id="3c79f-109">Remove-AzDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="3c79f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3c79f-110">EXAMPLES</span></span>

### <span data-ttu-id="3c79f-111">예제 1: 데이터 집합 제거</span><span class="sxs-lookup"><span data-stu-id="3c79f-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="3c79f-112">이 명령은 WikiADF 이라는 data factory에서 DAWikiAggregatedData 이라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="3c79f-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="3c79f-114">변수</span><span class="sxs-lookup"><span data-stu-id="3c79f-114">PARAMETERS</span></span>

### <span data-ttu-id="3c79f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3c79f-115">-DataFactoryName</span></span>
<span data-ttu-id="3c79f-116">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3c79f-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 dataset을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c79f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c79f-118">-DefaultProfile</span></span>
<span data-ttu-id="3c79f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c79f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3c79f-120">-Force</span></span>
<span data-ttu-id="3c79f-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3c79f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c79f-122">-InputObject</span></span>
<span data-ttu-id="3c79f-123">제거할 데이터 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="3c79f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="3c79f-124">-Name</span></span>
<span data-ttu-id="3c79f-125">제거할 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="3c79f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c79f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c79f-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3c79f-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c79f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c79f-129">-ResourceId</span></span>
<span data-ttu-id="3c79f-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3c79f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="3c79f-131">-Confirm</span></span>
<span data-ttu-id="3c79f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c79f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c79f-133">-WhatIf</span></span>
<span data-ttu-id="3c79f-134">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3c79f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c79f-135">CommonParameters</span></span>
<span data-ttu-id="3c79f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c79f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c79f-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c79f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c79f-138">입력</span><span class="sxs-lookup"><span data-stu-id="3c79f-138">INPUTS</span></span>

### <span data-ttu-id="3c79f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3c79f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="3c79f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c79f-140">System.String</span></span>

## <span data-ttu-id="3c79f-141">출력</span><span class="sxs-lookup"><span data-stu-id="3c79f-141">OUTPUTS</span></span>

### <span data-ttu-id="3c79f-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="3c79f-142">System.Void</span></span>

## <span data-ttu-id="3c79f-143">상속자</span><span class="sxs-lookup"><span data-stu-id="3c79f-143">NOTES</span></span>
<span data-ttu-id="3c79f-144">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="3c79f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3c79f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c79f-145">RELATED LINKS</span></span>

[<span data-ttu-id="3c79f-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3c79f-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="3c79f-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3c79f-147">Set-AzDataFactoryV2Dataset</span></span>]()
