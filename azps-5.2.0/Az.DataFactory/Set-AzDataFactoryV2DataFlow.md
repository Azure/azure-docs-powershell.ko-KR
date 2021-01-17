---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357757"
---
# <span data-ttu-id="b1582-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="b1582-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="b1582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1582-102">SYNOPSIS</span></span>
<span data-ttu-id="b1582-103">Data Factory에서 데이터 흐름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="b1582-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1582-104">SYNTAX</span></span>

### <span data-ttu-id="b1582-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1582-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1582-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1582-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1582-107">설명</span><span class="sxs-lookup"><span data-stu-id="b1582-107">DESCRIPTION</span></span>
<span data-ttu-id="b1582-108">이 Set-AzDataFactoryV2DataFlow cmdlet은 Azure Data Factory에서 데이터 흐름을 만들거나 기존 데이터 흐름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="b1582-109">예제</span><span class="sxs-lookup"><span data-stu-id="b1582-109">EXAMPLES</span></span>

### <span data-ttu-id="b1582-110">예제 1: 데이터 흐름 만들기</span><span class="sxs-lookup"><span data-stu-id="b1582-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="b1582-111">이 명령은 WikiADF라는 데이터 팩터리에 TaxiDemo1이라는 데이터 흐름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="b1582-112">이 명령은 데이터 흐름을 TaxiDemo1.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="b1582-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1582-113">PARAMETERS</span></span>

### <span data-ttu-id="b1582-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b1582-114">-DataFactoryName</span></span>
<span data-ttu-id="b1582-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-115">The data factory name.</span></span>

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

### <span data-ttu-id="b1582-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1582-116">-DefaultProfile</span></span>
<span data-ttu-id="b1582-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1582-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b1582-118">-DefinitionFile</span></span>
<span data-ttu-id="b1582-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1582-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b1582-120">-Force</span></span>
<span data-ttu-id="b1582-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b1582-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b1582-122">-Name</span></span>
<span data-ttu-id="b1582-123">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1582-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1582-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1582-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-125">The resource group name.</span></span>

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

### <span data-ttu-id="b1582-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1582-126">-ResourceId</span></span>
<span data-ttu-id="b1582-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b1582-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1582-128">-Confirm</span></span>
<span data-ttu-id="b1582-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1582-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1582-130">-WhatIf</span></span>
<span data-ttu-id="b1582-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1582-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1582-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1582-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1582-133">CommonParameters</span></span>
<span data-ttu-id="b1582-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1582-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1582-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1582-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1582-136">입력</span><span class="sxs-lookup"><span data-stu-id="b1582-136">INPUTS</span></span>

### <span data-ttu-id="b1582-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b1582-137">System.String</span></span>

## <span data-ttu-id="b1582-138">출력</span><span class="sxs-lookup"><span data-stu-id="b1582-138">OUTPUTS</span></span>

### <span data-ttu-id="b1582-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="b1582-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="b1582-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1582-140">NOTES</span></span>
<span data-ttu-id="b1582-141">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="b1582-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b1582-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1582-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1582-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="b1582-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="b1582-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="b1582-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
