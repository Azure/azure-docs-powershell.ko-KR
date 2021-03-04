---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 4838ba48d12fa3a4b1fd7d129e63e0a643357a78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975291"
---
# <span data-ttu-id="d6762-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="d6762-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="d6762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6762-102">SYNOPSIS</span></span>
<span data-ttu-id="d6762-103">Data Factory에서 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="d6762-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6762-104">SYNTAX</span></span>

### <span data-ttu-id="d6762-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d6762-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6762-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d6762-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6762-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6762-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6762-108">설명</span><span class="sxs-lookup"><span data-stu-id="d6762-108">DESCRIPTION</span></span>
<span data-ttu-id="d6762-109">Get-AzDataFactoryV2DataFlow cmdlet은 Azure Data Factory의 데이터 흐름에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="d6762-110">데이터 흐름의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="d6762-111">이름을 지정하지 않으면 이 cmdlet은 데이터 팩터리의 모든 데이터 흐름에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="d6762-112">예제</span><span class="sxs-lookup"><span data-stu-id="d6762-112">EXAMPLES</span></span>
### <span data-ttu-id="d6762-113">예제 1: 모든 데이터 흐름에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="d6762-114">이 명령은 WikiADF라는 데이터 팩터리의 모든 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="d6762-115">예제 2: 특정 데이터 흐름에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="d6762-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="d6762-116">이 명령은 WikiADF라는 데이터 팩터리에서 dataflow1이라는 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="d6762-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6762-117">PARAMETERS</span></span>

### <span data-ttu-id="d6762-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6762-118">-DataFactory</span></span>
<span data-ttu-id="d6762-119">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6762-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d6762-120">-DataFactoryName</span></span>
<span data-ttu-id="d6762-121">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-121">The data factory name.</span></span>

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

### <span data-ttu-id="d6762-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6762-122">-DefaultProfile</span></span>
<span data-ttu-id="d6762-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6762-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d6762-124">-Name</span></span>
<span data-ttu-id="d6762-125">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6762-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6762-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6762-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-127">The resource group name.</span></span>

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

### <span data-ttu-id="d6762-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6762-128">-ResourceId</span></span>
<span data-ttu-id="d6762-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d6762-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6762-130">CommonParameters</span></span>
<span data-ttu-id="d6762-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6762-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6762-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6762-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6762-133">입력</span><span class="sxs-lookup"><span data-stu-id="d6762-133">INPUTS</span></span>

### <span data-ttu-id="d6762-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d6762-134">System.String</span></span>

### <span data-ttu-id="d6762-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d6762-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d6762-136">출력</span><span class="sxs-lookup"><span data-stu-id="d6762-136">OUTPUTS</span></span>

### <span data-ttu-id="d6762-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="d6762-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="d6762-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6762-138">NOTES</span></span>
<span data-ttu-id="d6762-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="d6762-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d6762-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6762-140">RELATED LINKS</span></span>

[<span data-ttu-id="d6762-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="d6762-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="d6762-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="d6762-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)