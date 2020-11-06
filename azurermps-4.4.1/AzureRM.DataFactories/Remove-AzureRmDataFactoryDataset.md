---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 85e9e96db366adcb30494ac22e7d1b73bbff9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527671"
---
# <span data-ttu-id="81a10-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="81a10-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="81a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81a10-102">SYNOPSIS</span></span>
<span data-ttu-id="81a10-103">Azure Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81a10-104">SYNTAX</span></span>

### <span data-ttu-id="81a10-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="81a10-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81a10-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81a10-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81a10-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81a10-107">DESCRIPTION</span></span>
<span data-ttu-id="81a10-108">**AzureRmDataFactoryDataset** Cmdlet은 Azure Data Factory에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="81a10-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81a10-109">EXAMPLES</span></span>

### <span data-ttu-id="81a10-110">예제 1: 데이터 집합 제거</span><span class="sxs-lookup"><span data-stu-id="81a10-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="81a10-111">이 명령은 WikiADF 이라는 data factory에서 DAWikiAggregatedData 이라는 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="81a10-112">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="81a10-113">변수</span><span class="sxs-lookup"><span data-stu-id="81a10-113">PARAMETERS</span></span>

### <span data-ttu-id="81a10-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="81a10-114">-DataFactory</span></span>
<span data-ttu-id="81a10-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="81a10-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 dataset을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="81a10-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81a10-117">-DataFactoryName</span></span>
<span data-ttu-id="81a10-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="81a10-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 dataset을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="81a10-120">-Force</span><span class="sxs-lookup"><span data-stu-id="81a10-120">-Force</span></span>
<span data-ttu-id="81a10-121">이 cmdlet이 확인을 묻지 않고 데이터 집합을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-121">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="81a10-122">-이름</span><span class="sxs-lookup"><span data-stu-id="81a10-122">-Name</span></span>
<span data-ttu-id="81a10-123">제거할 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-123">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="81a10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a10-124">-ResourceGroupName</span></span>
<span data-ttu-id="81a10-125">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="81a10-126">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-126">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="81a10-127">-확인</span><span class="sxs-lookup"><span data-stu-id="81a10-127">-Confirm</span></span>
<span data-ttu-id="81a10-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a10-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a10-129">-WhatIf</span></span>
<span data-ttu-id="81a10-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a10-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a10-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a10-132">-DefaultProfile</span></span>
<span data-ttu-id="81a10-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a10-134">CommonParameters</span></span>
<span data-ttu-id="81a10-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81a10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a10-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a10-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a10-137">입력</span><span class="sxs-lookup"><span data-stu-id="81a10-137">INPUTS</span></span>

## <span data-ttu-id="81a10-138">출력</span><span class="sxs-lookup"><span data-stu-id="81a10-138">OUTPUTS</span></span>

### <span data-ttu-id="81a10-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="81a10-139">System.Boolean</span></span>

## <span data-ttu-id="81a10-140">상속자</span><span class="sxs-lookup"><span data-stu-id="81a10-140">NOTES</span></span>
* <span data-ttu-id="81a10-141">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="81a10-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="81a10-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81a10-142">RELATED LINKS</span></span>

[<span data-ttu-id="81a10-143">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="81a10-143">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="81a10-144">새로운 AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="81a10-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


