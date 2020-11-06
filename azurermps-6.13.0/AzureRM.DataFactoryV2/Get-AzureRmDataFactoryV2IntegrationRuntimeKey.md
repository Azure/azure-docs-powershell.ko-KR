---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 0f57e0ac27e47272c2b6e72a3c847d9f06a568a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532054"
---
# <span data-ttu-id="d7cae-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d7cae-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="d7cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7cae-102">SYNOPSIS</span></span>
<span data-ttu-id="d7cae-103">자체 호스팅 통합 런타임의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7cae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7cae-104">SYNTAX</span></span>

### <span data-ttu-id="d7cae-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7cae-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7cae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7cae-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7cae-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d7cae-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7cae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d7cae-108">DESCRIPTION</span></span>
<span data-ttu-id="d7cae-109">통합 런타임의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="d7cae-110">키는 통합 런타임 노드를 등록 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="d7cae-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d7cae-111">EXAMPLES</span></span>

### <span data-ttu-id="d7cae-112">예제 1: 통합 런타임 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="d7cae-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="d7cae-113">Cmdlet은 ' selfhost-ir ' 이라는 통합 런타임의 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d7cae-114">변수</span><span class="sxs-lookup"><span data-stu-id="d7cae-114">PARAMETERS</span></span>

### <span data-ttu-id="d7cae-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d7cae-115">-DataFactoryName</span></span>
<span data-ttu-id="d7cae-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-116">The data factory name.</span></span>

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

### <span data-ttu-id="d7cae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7cae-117">-DefaultProfile</span></span>
<span data-ttu-id="d7cae-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7cae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7cae-119">-InputObject</span></span>
<span data-ttu-id="d7cae-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="d7cae-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d7cae-121">-Name</span></span>
<span data-ttu-id="d7cae-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="d7cae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7cae-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7cae-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-124">The resource group name.</span></span>

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

### <span data-ttu-id="d7cae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7cae-125">-ResourceId</span></span>
<span data-ttu-id="d7cae-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d7cae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7cae-127">CommonParameters</span></span>
<span data-ttu-id="d7cae-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7cae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7cae-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7cae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7cae-130">입력</span><span class="sxs-lookup"><span data-stu-id="d7cae-130">INPUTS</span></span>

### <span data-ttu-id="d7cae-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7cae-131">System.String</span></span>

### <span data-ttu-id="d7cae-132">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="d7cae-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="d7cae-133">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7cae-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d7cae-134">출력</span><span class="sxs-lookup"><span data-stu-id="d7cae-134">OUTPUTS</span></span>

### <span data-ttu-id="d7cae-135">DataFactoryV2. PSIntegrationRuntimeKeys/.</span><span class="sxs-lookup"><span data-stu-id="d7cae-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d7cae-136">상속자</span><span class="sxs-lookup"><span data-stu-id="d7cae-136">NOTES</span></span>

## <span data-ttu-id="d7cae-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7cae-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7cae-138">새로운 AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d7cae-138">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
