---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: fc47b71b1546fe351f9d535da4ef9942af66f19e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975259"
---
# <span data-ttu-id="6dece-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6dece-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="6dece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dece-102">SYNOPSIS</span></span>
<span data-ttu-id="6dece-103">자체 호스팅 통합 런타임에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="6dece-104">구문</span><span class="sxs-lookup"><span data-stu-id="6dece-104">SYNTAX</span></span>

### <span data-ttu-id="6dece-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6dece-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dece-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6dece-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dece-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6dece-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dece-108">설명</span><span class="sxs-lookup"><span data-stu-id="6dece-108">DESCRIPTION</span></span>
<span data-ttu-id="6dece-109">통합 런타임에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="6dece-110">키는 통합 런타임 노드를 등록하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="6dece-111">예제</span><span class="sxs-lookup"><span data-stu-id="6dece-111">EXAMPLES</span></span>

### <span data-ttu-id="6dece-112">예제 1: 통합 런타임 키 사용</span><span class="sxs-lookup"><span data-stu-id="6dece-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="6dece-113">cmdlet은 'test-selfhost-ir'이라는 통합 런타임에 대한 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6dece-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6dece-114">PARAMETERS</span></span>

### <span data-ttu-id="6dece-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6dece-115">-DataFactoryName</span></span>
<span data-ttu-id="6dece-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-116">The data factory name.</span></span>

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

### <span data-ttu-id="6dece-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dece-117">-DefaultProfile</span></span>
<span data-ttu-id="6dece-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dece-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dece-119">-InputObject</span></span>
<span data-ttu-id="6dece-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="6dece-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6dece-121">-Name</span></span>
<span data-ttu-id="6dece-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="6dece-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dece-123">-ResourceGroupName</span></span>
<span data-ttu-id="6dece-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-124">The resource group name.</span></span>

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

### <span data-ttu-id="6dece-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dece-125">-ResourceId</span></span>
<span data-ttu-id="6dece-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6dece-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dece-127">CommonParameters</span></span>
<span data-ttu-id="6dece-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6dece-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dece-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6dece-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dece-130">입력</span><span class="sxs-lookup"><span data-stu-id="6dece-130">INPUTS</span></span>

### <span data-ttu-id="6dece-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6dece-131">System.String</span></span>

### <span data-ttu-id="6dece-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6dece-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6dece-133">출력</span><span class="sxs-lookup"><span data-stu-id="6dece-133">OUTPUTS</span></span>

### <span data-ttu-id="6dece-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6dece-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="6dece-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6dece-135">NOTES</span></span>

## <span data-ttu-id="6dece-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6dece-136">RELATED LINKS</span></span>

[<span data-ttu-id="6dece-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6dece-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
