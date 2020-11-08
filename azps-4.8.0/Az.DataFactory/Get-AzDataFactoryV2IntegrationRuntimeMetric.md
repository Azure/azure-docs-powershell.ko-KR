---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212528"
---
# <span data-ttu-id="6a3ff-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="6a3ff-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="6a3ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3ff-103">통합 런타임에 대 한 메트릭 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="6a3ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a3ff-104">SYNTAX</span></span>

### <span data-ttu-id="6a3ff-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a3ff-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a3ff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a3ff-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a3ff-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6a3ff-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3ff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6a3ff-108">DESCRIPTION</span></span>
<span data-ttu-id="6a3ff-109">Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet은 데이터 팩터리의 통합 런타임에 대 한 메트릭 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="6a3ff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6a3ff-110">EXAMPLES</span></span>

### <span data-ttu-id="6a3ff-111">예제 1: 통합 런타임 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="6a3ff-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="6a3ff-112">이 명령은 ' rg-test-dfv2 ' 라는 리소스 그룹에 대 한 구독에서 ' selfhost-ir ' 이라는 이름의 통합 런타임과 ' test-df-eu2 ' 이라는 데이터 팩터리에 대 한 메트릭 데이터를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="6a3ff-113">변수</span><span class="sxs-lookup"><span data-stu-id="6a3ff-113">PARAMETERS</span></span>

### <span data-ttu-id="6a3ff-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6a3ff-114">-DataFactoryName</span></span>
<span data-ttu-id="6a3ff-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-115">The data factory name.</span></span>

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

### <span data-ttu-id="6a3ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3ff-116">-DefaultProfile</span></span>
<span data-ttu-id="6a3ff-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3ff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a3ff-118">-InputObject</span></span>
<span data-ttu-id="6a3ff-119">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="6a3ff-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6a3ff-120">-Name</span></span>
<span data-ttu-id="6a3ff-121">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="6a3ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a3ff-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-123">The resource group name.</span></span>

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

### <span data-ttu-id="6a3ff-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a3ff-124">-ResourceId</span></span>
<span data-ttu-id="6a3ff-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6a3ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3ff-126">CommonParameters</span></span>
<span data-ttu-id="6a3ff-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3ff-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3ff-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3ff-129">입력</span><span class="sxs-lookup"><span data-stu-id="6a3ff-129">INPUTS</span></span>

### <span data-ttu-id="6a3ff-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6a3ff-130">System.String</span></span>

### <span data-ttu-id="6a3ff-131">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6a3ff-132">출력</span><span class="sxs-lookup"><span data-stu-id="6a3ff-132">OUTPUTS</span></span>

### <span data-ttu-id="6a3ff-133">DataFactoryV2. PSIntegrationRuntimeMetrics/.</span><span class="sxs-lookup"><span data-stu-id="6a3ff-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="6a3ff-134">상속자</span><span class="sxs-lookup"><span data-stu-id="6a3ff-134">NOTES</span></span>

## <span data-ttu-id="6a3ff-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a3ff-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a3ff-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a3ff-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

