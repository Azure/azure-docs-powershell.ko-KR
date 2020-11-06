---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537331"
---
# <span data-ttu-id="822a6-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="822a6-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="822a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="822a6-102">SYNOPSIS</span></span>
<span data-ttu-id="822a6-103">자체 호스팅 통합 런타임의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="822a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="822a6-104">SYNTAX</span></span>

### <span data-ttu-id="822a6-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="822a6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="822a6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="822a6-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="822a6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="822a6-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="822a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="822a6-108">DESCRIPTION</span></span>
<span data-ttu-id="822a6-109">통합 런타임의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="822a6-110">키는 통합 런타임 노드를 등록 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="822a6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="822a6-111">EXAMPLES</span></span>

### <span data-ttu-id="822a6-112">예제 1: 통합 런타임 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="822a6-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="822a6-113">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="822a6-114">변수</span><span class="sxs-lookup"><span data-stu-id="822a6-114">PARAMETERS</span></span>

### <span data-ttu-id="822a6-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="822a6-115">-DataFactoryName</span></span>
<span data-ttu-id="822a6-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-116">The data factory name.</span></span>

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

### <span data-ttu-id="822a6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="822a6-117">-InputObject</span></span>
<span data-ttu-id="822a6-118">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="822a6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="822a6-119">-Name</span></span>
<span data-ttu-id="822a6-120">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="822a6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822a6-121">-ResourceGroupName</span></span>
<span data-ttu-id="822a6-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-122">The resource group name.</span></span>

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

### <span data-ttu-id="822a6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="822a6-123">-ResourceId</span></span>
<span data-ttu-id="822a6-124">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="822a6-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="822a6-125">입력</span><span class="sxs-lookup"><span data-stu-id="822a6-125">INPUTS</span></span>

### <span data-ttu-id="822a6-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="822a6-126">System.String</span></span>
<span data-ttu-id="822a6-127">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="822a6-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="822a6-128">출력</span><span class="sxs-lookup"><span data-stu-id="822a6-128">OUTPUTS</span></span>

### <span data-ttu-id="822a6-129">DataFactoryV2. PSIntegrationRuntimeKeys/.</span><span class="sxs-lookup"><span data-stu-id="822a6-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="822a6-130">상속자</span><span class="sxs-lookup"><span data-stu-id="822a6-130">NOTES</span></span>

## <span data-ttu-id="822a6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="822a6-131">RELATED LINKS</span></span>
[<span data-ttu-id="822a6-132">새로운 AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="822a6-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
