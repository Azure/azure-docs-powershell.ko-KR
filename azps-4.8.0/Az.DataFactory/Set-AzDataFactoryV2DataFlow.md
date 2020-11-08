---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204612"
---
# <span data-ttu-id="d8e9b-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="d8e9b-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="d8e9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e9b-103">데이터 팩터리에 데이터 흐름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="d8e9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8e9b-104">SYNTAX</span></span>

### <span data-ttu-id="d8e9b-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8e9b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e9b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8e9b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e9b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d8e9b-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e9b-108">Set-AzDataFactoryV2DataFlow cmdlet은 데이터 흐름을 만들거나 Azure Data Factory의 기존 데이터 흐름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="d8e9b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d8e9b-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e9b-110">예제 1: 데이터 흐름 만들기</span><span class="sxs-lookup"><span data-stu-id="d8e9b-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="d8e9b-111">이 명령은 WikiADF 이라는 data factory에 TaxiDemo1 라는 데이터 흐름을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="d8e9b-112">명령은 파일의 TaxiDemo1.js정보에 대 한 데이터 흐름을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="d8e9b-113">변수</span><span class="sxs-lookup"><span data-stu-id="d8e9b-113">PARAMETERS</span></span>

### <span data-ttu-id="d8e9b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8e9b-114">-DataFactoryName</span></span>
<span data-ttu-id="d8e9b-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-115">The data factory name.</span></span>

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

### <span data-ttu-id="d8e9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e9b-116">-DefaultProfile</span></span>
<span data-ttu-id="d8e9b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8e9b-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d8e9b-118">-DefinitionFile</span></span>
<span data-ttu-id="d8e9b-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-119">The JSON file path.</span></span>

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

### <span data-ttu-id="d8e9b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d8e9b-120">-Force</span></span>
<span data-ttu-id="d8e9b-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d8e9b-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d8e9b-122">-Name</span></span>
<span data-ttu-id="d8e9b-123">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-123">The data flow name.</span></span>

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

### <span data-ttu-id="d8e9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8e9b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-125">The resource group name.</span></span>

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

### <span data-ttu-id="d8e9b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8e9b-126">-ResourceId</span></span>
<span data-ttu-id="d8e9b-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d8e9b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d8e9b-128">-Confirm</span></span>
<span data-ttu-id="d8e9b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e9b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e9b-130">-WhatIf</span></span>
<span data-ttu-id="d8e9b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e9b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e9b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e9b-133">CommonParameters</span></span>
<span data-ttu-id="d8e9b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e9b-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8e9b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e9b-136">입력</span><span class="sxs-lookup"><span data-stu-id="d8e9b-136">INPUTS</span></span>

### <span data-ttu-id="d8e9b-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8e9b-137">System.String</span></span>

## <span data-ttu-id="d8e9b-138">출력</span><span class="sxs-lookup"><span data-stu-id="d8e9b-138">OUTPUTS</span></span>

### <span data-ttu-id="d8e9b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="d8e9b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="d8e9b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d8e9b-140">NOTES</span></span>
<span data-ttu-id="d8e9b-141">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d8e9b-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d8e9b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8e9b-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8e9b-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="d8e9b-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="d8e9b-144">제거-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="d8e9b-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
