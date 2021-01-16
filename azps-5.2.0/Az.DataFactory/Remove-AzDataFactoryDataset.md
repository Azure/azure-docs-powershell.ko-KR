---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327312"
---
# <span data-ttu-id="305c5-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="305c5-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="305c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305c5-102">SYNOPSIS</span></span>
<span data-ttu-id="305c5-103">Azure Data Factory에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="305c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="305c5-104">SYNTAX</span></span>

### <span data-ttu-id="305c5-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="305c5-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="305c5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="305c5-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="305c5-107">설명</span><span class="sxs-lookup"><span data-stu-id="305c5-107">DESCRIPTION</span></span>
<span data-ttu-id="305c5-108">**Remove-AzDataFactoryDataset** cmdlet은 Azure Data Factory에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="305c5-109">예제</span><span class="sxs-lookup"><span data-stu-id="305c5-109">EXAMPLES</span></span>

### <span data-ttu-id="305c5-110">예제 1: 데이터 세트 제거</span><span class="sxs-lookup"><span data-stu-id="305c5-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="305c5-111">이 명령은 WikiADF라는 데이터 팩터리에서 DAWikiAggregatedData라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="305c5-112">이 명령은 10진수의 $True.</span><span class="sxs-lookup"><span data-stu-id="305c5-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="305c5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305c5-113">PARAMETERS</span></span>

### <span data-ttu-id="305c5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="305c5-114">-DataFactory</span></span>
<span data-ttu-id="305c5-115">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="305c5-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="305c5-116">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305c5-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="305c5-117">-DataFactoryName</span></span>
<span data-ttu-id="305c5-118">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="305c5-119">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="305c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305c5-120">-DefaultProfile</span></span>
<span data-ttu-id="305c5-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="305c5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="305c5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="305c5-122">-Force</span></span>
<span data-ttu-id="305c5-123">이 cmdlet이 확인을 요청하지 않고 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="305c5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="305c5-124">-Name</span></span>
<span data-ttu-id="305c5-125">제거할 데이터 세트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="305c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="305c5-127">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="305c5-128">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="305c5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="305c5-129">-Confirm</span></span>
<span data-ttu-id="305c5-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="305c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="305c5-131">-WhatIf</span></span>
<span data-ttu-id="305c5-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="305c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305c5-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="305c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305c5-134">CommonParameters</span></span>
<span data-ttu-id="305c5-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="305c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305c5-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="305c5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305c5-137">입력</span><span class="sxs-lookup"><span data-stu-id="305c5-137">INPUTS</span></span>

### <span data-ttu-id="305c5-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="305c5-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="305c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="305c5-139">System.String</span></span>

## <span data-ttu-id="305c5-140">출력</span><span class="sxs-lookup"><span data-stu-id="305c5-140">OUTPUTS</span></span>

### <span data-ttu-id="305c5-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="305c5-141">System.Void</span></span>

## <span data-ttu-id="305c5-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="305c5-142">NOTES</span></span>
* <span data-ttu-id="305c5-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="305c5-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="305c5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="305c5-144">RELATED LINKS</span></span>

[<span data-ttu-id="305c5-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="305c5-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="305c5-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="305c5-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


