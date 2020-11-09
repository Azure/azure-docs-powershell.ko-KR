---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306296"
---
# <span data-ttu-id="611cd-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="611cd-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="611cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611cd-102">SYNOPSIS</span></span>
<span data-ttu-id="611cd-103">Data Factory의 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="611cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="611cd-104">SYNTAX</span></span>

### <span data-ttu-id="611cd-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="611cd-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="611cd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="611cd-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="611cd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="611cd-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="611cd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="611cd-108">DESCRIPTION</span></span>
<span data-ttu-id="611cd-109">Get-AzDataFactoryV2DataFlow cmdlet은 Azure Data Factory의 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="611cd-110">데이터 흐름의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="611cd-111">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="611cd-112">예제의</span><span class="sxs-lookup"><span data-stu-id="611cd-112">EXAMPLES</span></span>
### <span data-ttu-id="611cd-113">예제 1: 모든 데이터 흐름에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="611cd-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="611cd-114">이 명령은 WikiADF 이라는 data factory의 모든 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="611cd-115">예제 2: 특정 데이터 흐름에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="611cd-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="611cd-116">이 명령은 WikiADF 이라는 data factory에서 dataflow1 라는 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="611cd-117">변수</span><span class="sxs-lookup"><span data-stu-id="611cd-117">PARAMETERS</span></span>

### <span data-ttu-id="611cd-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="611cd-118">-DataFactory</span></span>
<span data-ttu-id="611cd-119">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-119">The data factory object.</span></span>

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

### <span data-ttu-id="611cd-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="611cd-120">-DataFactoryName</span></span>
<span data-ttu-id="611cd-121">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-121">The data factory name.</span></span>

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

### <span data-ttu-id="611cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611cd-122">-DefaultProfile</span></span>
<span data-ttu-id="611cd-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="611cd-124">-이름</span><span class="sxs-lookup"><span data-stu-id="611cd-124">-Name</span></span>
<span data-ttu-id="611cd-125">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-125">The data flow name.</span></span>

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

### <span data-ttu-id="611cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="611cd-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-127">The resource group name.</span></span>

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

### <span data-ttu-id="611cd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="611cd-128">-ResourceId</span></span>
<span data-ttu-id="611cd-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="611cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611cd-130">CommonParameters</span></span>
<span data-ttu-id="611cd-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="611cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611cd-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="611cd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611cd-133">입력</span><span class="sxs-lookup"><span data-stu-id="611cd-133">INPUTS</span></span>

### <span data-ttu-id="611cd-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="611cd-134">System.String</span></span>

### <span data-ttu-id="611cd-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="611cd-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="611cd-136">출력</span><span class="sxs-lookup"><span data-stu-id="611cd-136">OUTPUTS</span></span>

### <span data-ttu-id="611cd-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="611cd-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="611cd-138">상속자</span><span class="sxs-lookup"><span data-stu-id="611cd-138">NOTES</span></span>
<span data-ttu-id="611cd-139">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="611cd-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="611cd-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="611cd-140">RELATED LINKS</span></span>

[<span data-ttu-id="611cd-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="611cd-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="611cd-142">제거-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="611cd-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)