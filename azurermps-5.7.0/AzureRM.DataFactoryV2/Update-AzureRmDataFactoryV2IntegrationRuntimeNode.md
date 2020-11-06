---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 3ca08f32cbb9f9608c7886b92110e87c2422d554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531732"
---
# <span data-ttu-id="f29bb-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f29bb-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="f29bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f29bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f29bb-103">자체 호스팅 통합 런타임 노드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-103">Updates self-hosted integration runtime node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f29bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f29bb-104">SYNTAX</span></span>

### <span data-ttu-id="f29bb-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f29bb-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29bb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f29bb-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29bb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f29bb-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f29bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f29bb-108">DESCRIPTION</span></span>
<span data-ttu-id="f29bb-109">**AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet은 데이터 팩터리에 자체 호스팅된 통합 런타임 노드의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-109">The **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="f29bb-110">현재 ' ConcurrentJobsLimit ' 업데이트만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="f29bb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f29bb-111">EXAMPLES</span></span>

### <span data-ttu-id="f29bb-112">예제 1: 자체 호스트 된 통합 런타임 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="f29bb-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="f29bb-113">자체 호스팅된 통합 런타임 ' test-selfhost-ir '의 노드 ' Node_1 '에 대해 cmdlet이 ' ConcurrentJobsLimit '를 3으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f29bb-114">변수</span><span class="sxs-lookup"><span data-stu-id="f29bb-114">PARAMETERS</span></span>

### <span data-ttu-id="f29bb-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="f29bb-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="f29bb-116">통합 런타임 노드에서 실행할 수 있는 동시 작업의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="f29bb-117">1에서 maxConcurrentJobs 사이의 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29bb-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f29bb-118">-DataFactoryName</span></span>
<span data-ttu-id="f29bb-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-119">The data factory name.</span></span>

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

### <span data-ttu-id="f29bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29bb-120">-DefaultProfile</span></span>
<span data-ttu-id="f29bb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29bb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f29bb-122">-InputObject</span></span>
<span data-ttu-id="f29bb-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="f29bb-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f29bb-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f29bb-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-125">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f29bb-126">-이름</span><span class="sxs-lookup"><span data-stu-id="f29bb-126">-Name</span></span>
<span data-ttu-id="f29bb-127">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-127">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29bb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29bb-128">-ResourceGroupName</span></span>
<span data-ttu-id="f29bb-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-129">The resource group name.</span></span>

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

### <span data-ttu-id="f29bb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f29bb-130">-ResourceId</span></span>
<span data-ttu-id="f29bb-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f29bb-132">-확인</span><span class="sxs-lookup"><span data-stu-id="f29bb-132">-Confirm</span></span>
<span data-ttu-id="f29bb-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29bb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29bb-134">-WhatIf</span></span>
<span data-ttu-id="f29bb-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29bb-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29bb-137">CommonParameters</span></span>
<span data-ttu-id="f29bb-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f29bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29bb-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29bb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29bb-140">입력</span><span class="sxs-lookup"><span data-stu-id="f29bb-140">INPUTS</span></span>

### <span data-ttu-id="f29bb-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f29bb-141">System.String</span></span>
<span data-ttu-id="f29bb-142">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="f29bb-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f29bb-143">출력</span><span class="sxs-lookup"><span data-stu-id="f29bb-143">OUTPUTS</span></span>

### <span data-ttu-id="f29bb-144">DataFactoryV2. PSSelfHostedIntegrationRuntimeNode/.</span><span class="sxs-lookup"><span data-stu-id="f29bb-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f29bb-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f29bb-145">NOTES</span></span>
<span data-ttu-id="f29bb-146">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="f29bb-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f29bb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f29bb-147">RELATED LINKS</span></span>

<span data-ttu-id="f29bb-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="f29bb-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

