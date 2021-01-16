---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333717"
---
# <span data-ttu-id="162cd-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="162cd-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="162cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="162cd-102">SYNOPSIS</span></span>
<span data-ttu-id="162cd-103">자체 호스팅 통합 런타임에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="162cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="162cd-104">SYNTAX</span></span>

### <span data-ttu-id="162cd-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="162cd-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="162cd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="162cd-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="162cd-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="162cd-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="162cd-108">설명</span><span class="sxs-lookup"><span data-stu-id="162cd-108">DESCRIPTION</span></span>
<span data-ttu-id="162cd-109">통합 런타임에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="162cd-110">키는 통합 런타임 노드를 등록하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="162cd-111">예제</span><span class="sxs-lookup"><span data-stu-id="162cd-111">EXAMPLES</span></span>

### <span data-ttu-id="162cd-112">예제 1: 통합 런타임 키 얻기</span><span class="sxs-lookup"><span data-stu-id="162cd-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="162cd-113">cmdlet은 'test-selfhost-ir'이라는 통합 런타임에 대한 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="162cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="162cd-114">PARAMETERS</span></span>

### <span data-ttu-id="162cd-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="162cd-115">-DataFactoryName</span></span>
<span data-ttu-id="162cd-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-116">The data factory name.</span></span>

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

### <span data-ttu-id="162cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162cd-117">-DefaultProfile</span></span>
<span data-ttu-id="162cd-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="162cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="162cd-119">-InputObject</span></span>
<span data-ttu-id="162cd-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="162cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="162cd-121">-Name</span></span>
<span data-ttu-id="162cd-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="162cd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162cd-123">-ResourceGroupName</span></span>
<span data-ttu-id="162cd-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-124">The resource group name.</span></span>

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

### <span data-ttu-id="162cd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="162cd-125">-ResourceId</span></span>
<span data-ttu-id="162cd-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="162cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162cd-127">CommonParameters</span></span>
<span data-ttu-id="162cd-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="162cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162cd-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="162cd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162cd-130">입력</span><span class="sxs-lookup"><span data-stu-id="162cd-130">INPUTS</span></span>

### <span data-ttu-id="162cd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="162cd-131">System.String</span></span>

### <span data-ttu-id="162cd-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="162cd-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="162cd-133">출력</span><span class="sxs-lookup"><span data-stu-id="162cd-133">OUTPUTS</span></span>

### <span data-ttu-id="162cd-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="162cd-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="162cd-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="162cd-135">NOTES</span></span>

## <span data-ttu-id="162cd-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="162cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="162cd-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="162cd-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
