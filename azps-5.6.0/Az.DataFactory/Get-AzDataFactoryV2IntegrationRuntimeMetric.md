---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975248"
---
# <span data-ttu-id="bfc64-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="bfc64-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="bfc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc64-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc64-103">통합 런타임에 대한 메트릭 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="bfc64-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfc64-104">SYNTAX</span></span>

### <span data-ttu-id="bfc64-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bfc64-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfc64-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc64-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfc64-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="bfc64-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc64-108">설명</span><span class="sxs-lookup"><span data-stu-id="bfc64-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc64-109">Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet은 데이터 팩터리의 통합 런타임에 대한 메트릭 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="bfc64-110">예제</span><span class="sxs-lookup"><span data-stu-id="bfc64-110">EXAMPLES</span></span>

### <span data-ttu-id="bfc64-111">예제 1: 통합 런타임 메트릭 사용</span><span class="sxs-lookup"><span data-stu-id="bfc64-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="bfc64-112">이 명령은 'rg-test-dfv2'라는 리소스 그룹에 대한 구독에서 'test-selfhost-ir'이라는 통합 런타임 및 'test-df-eu2'라는 데이터 팩터리에 대한 메트릭 데이터를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="bfc64-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bfc64-113">PARAMETERS</span></span>

### <span data-ttu-id="bfc64-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bfc64-114">-DataFactoryName</span></span>
<span data-ttu-id="bfc64-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc64-116">-DefaultProfile</span></span>
<span data-ttu-id="bfc64-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc64-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfc64-118">-InputObject</span></span>
<span data-ttu-id="bfc64-119">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc64-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc64-120">-Name</span></span>
<span data-ttu-id="bfc64-121">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc64-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfc64-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc64-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc64-124">-ResourceId</span></span>
<span data-ttu-id="bfc64-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc64-126">CommonParameters</span></span>
<span data-ttu-id="bfc64-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc64-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bfc64-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc64-129">입력</span><span class="sxs-lookup"><span data-stu-id="bfc64-129">INPUTS</span></span>

### <span data-ttu-id="bfc64-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bfc64-130">System.String</span></span>

### <span data-ttu-id="bfc64-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bfc64-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="bfc64-132">출력</span><span class="sxs-lookup"><span data-stu-id="bfc64-132">OUTPUTS</span></span>

### <span data-ttu-id="bfc64-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="bfc64-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="bfc64-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfc64-134">NOTES</span></span>

## <span data-ttu-id="bfc64-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfc64-135">RELATED LINKS</span></span>

[<span data-ttu-id="bfc64-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bfc64-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

