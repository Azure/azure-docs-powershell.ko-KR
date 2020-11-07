---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711912"
---
# <span data-ttu-id="58ab9-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="58ab9-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="58ab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="58ab9-103">통합 런타임에 대 한 메트릭 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ab9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58ab9-104">SYNTAX</span></span>

### <span data-ttu-id="58ab9-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="58ab9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="58ab9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58ab9-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="58ab9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="58ab9-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="58ab9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="58ab9-108">DESCRIPTION</span></span>
<span data-ttu-id="58ab9-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet은 데이터 팩터리의 통합 런타임에 대 한 메트릭 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="58ab9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="58ab9-110">EXAMPLES</span></span>

### <span data-ttu-id="58ab9-111">예제 1: 통합 런타임 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="58ab9-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="58ab9-112">이 명령은 ' rg-test-dfv2 ' 라는 리소스 그룹에 대 한 구독에서 ' selfhost-ir ' 이라는 이름의 통합 런타임과 ' test-df-eu2 ' 이라는 데이터 팩터리에 대 한 메트릭 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="58ab9-113">변수</span><span class="sxs-lookup"><span data-stu-id="58ab9-113">PARAMETERS</span></span>

### <span data-ttu-id="58ab9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58ab9-114">-DataFactoryName</span></span>
<span data-ttu-id="58ab9-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ab9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58ab9-116">-InputObject</span></span>
<span data-ttu-id="58ab9-117">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58ab9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="58ab9-118">-Name</span></span>
<span data-ttu-id="58ab9-119">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ab9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ab9-120">-ResourceGroupName</span></span>
<span data-ttu-id="58ab9-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ab9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ab9-122">-ResourceId</span></span>
<span data-ttu-id="58ab9-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="58ab9-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="58ab9-124">입력</span><span class="sxs-lookup"><span data-stu-id="58ab9-124">INPUTS</span></span>

### <span data-ttu-id="58ab9-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58ab9-125">System.String</span></span>
<span data-ttu-id="58ab9-126">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="58ab9-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="58ab9-127">출력</span><span class="sxs-lookup"><span data-stu-id="58ab9-127">OUTPUTS</span></span>

### <span data-ttu-id="58ab9-128">DataFactoryV2. PSIntegrationRuntimeMetrics/.</span><span class="sxs-lookup"><span data-stu-id="58ab9-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="58ab9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="58ab9-129">NOTES</span></span>

## <span data-ttu-id="58ab9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58ab9-130">RELATED LINKS</span></span>
[<span data-ttu-id="58ab9-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="58ab9-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

