---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: faf5d80b231b93124279f3c9bb6a347f89d988d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702021"
---
# <span data-ttu-id="c5ae9-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c5ae9-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="c5ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ae9-103">Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5ae9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5ae9-104">SYNTAX</span></span>

### <span data-ttu-id="c5ae9-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5ae9-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ae9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5ae9-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5ae9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5ae9-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ae9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c5ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="c5ae9-109">Remove-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="c5ae9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c5ae9-110">EXAMPLES</span></span>

### <span data-ttu-id="c5ae9-111">예제 1: 데이터 집합 제거</span><span class="sxs-lookup"><span data-stu-id="c5ae9-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="c5ae9-112">이 명령은 WikiADF 이라는 data factory에서 DAWikiAggregatedData 이라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="c5ae9-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="c5ae9-114">변수</span><span class="sxs-lookup"><span data-stu-id="c5ae9-114">PARAMETERS</span></span>

### <span data-ttu-id="c5ae9-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c5ae9-115">-DataFactoryName</span></span>
<span data-ttu-id="c5ae9-116">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c5ae9-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 dataset을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5ae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ae9-118">-DefaultProfile</span></span>
<span data-ttu-id="c5ae9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5ae9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c5ae9-120">-Force</span></span>
<span data-ttu-id="c5ae9-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c5ae9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5ae9-122">-InputObject</span></span>
<span data-ttu-id="c5ae9-123">제거할 데이터 집합 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="c5ae9-124">-이름</span><span class="sxs-lookup"><span data-stu-id="c5ae9-124">-Name</span></span>
<span data-ttu-id="c5ae9-125">제거할 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="c5ae9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5ae9-126">-ResourceGroupName</span></span>
<span data-ttu-id="c5ae9-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c5ae9-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5ae9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5ae9-129">-ResourceId</span></span>
<span data-ttu-id="c5ae9-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c5ae9-131">-확인</span><span class="sxs-lookup"><span data-stu-id="c5ae9-131">-Confirm</span></span>
<span data-ttu-id="c5ae9-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ae9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ae9-133">-WhatIf</span></span>
<span data-ttu-id="c5ae9-134">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c5ae9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ae9-135">CommonParameters</span></span>
<span data-ttu-id="c5ae9-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5ae9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ae9-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5ae9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ae9-138">입력</span><span class="sxs-lookup"><span data-stu-id="c5ae9-138">INPUTS</span></span>

### <span data-ttu-id="c5ae9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c5ae9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="c5ae9-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5ae9-140">System.String</span></span>

## <span data-ttu-id="c5ae9-141">출력</span><span class="sxs-lookup"><span data-stu-id="c5ae9-141">OUTPUTS</span></span>

### <span data-ttu-id="c5ae9-142">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c5ae9-142">System.Object</span></span>

## <span data-ttu-id="c5ae9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="c5ae9-143">NOTES</span></span>
<span data-ttu-id="c5ae9-144">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="c5ae9-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c5ae9-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5ae9-145">RELATED LINKS</span></span>

[<span data-ttu-id="c5ae9-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c5ae9-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="c5ae9-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c5ae9-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
