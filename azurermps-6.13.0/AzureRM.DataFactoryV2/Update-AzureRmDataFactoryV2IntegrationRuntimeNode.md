---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a69e051fb8f2cba30fba8419a818346e044f8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530355"
---
# <span data-ttu-id="047b9-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="047b9-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="047b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047b9-102">SYNOPSIS</span></span>
<span data-ttu-id="047b9-103">자체 호스팅 통합 런타임 노드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-103">Updates self-hosted integration runtime node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="047b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="047b9-104">SYNTAX</span></span>

### <span data-ttu-id="047b9-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="047b9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="047b9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="047b9-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="047b9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="047b9-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="047b9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="047b9-108">DESCRIPTION</span></span>
<span data-ttu-id="047b9-109">**AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet은 데이터 팩터리에 자체 호스팅된 통합 런타임 노드의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-109">The **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="047b9-110">현재 ' ConcurrentJobsLimit ' 업데이트만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="047b9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="047b9-111">EXAMPLES</span></span>

### <span data-ttu-id="047b9-112">예제 1: 자체 호스트 된 통합 런타임 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="047b9-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="047b9-113">자체 호스팅된 통합 런타임 ' test-selfhost-ir '의 노드 ' Node_1 '에 대해 cmdlet이 ' ConcurrentJobsLimit '를 3으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="047b9-114">변수</span><span class="sxs-lookup"><span data-stu-id="047b9-114">PARAMETERS</span></span>

### <span data-ttu-id="047b9-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="047b9-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="047b9-116">통합 런타임 노드에서 실행할 수 있는 동시 작업의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="047b9-117">1에서 maxConcurrentJobs 사이의 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b9-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="047b9-118">-DataFactoryName</span></span>
<span data-ttu-id="047b9-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-119">The data factory name.</span></span>

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

### <span data-ttu-id="047b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047b9-120">-DefaultProfile</span></span>
<span data-ttu-id="047b9-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="047b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="047b9-122">-InputObject</span></span>
<span data-ttu-id="047b9-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="047b9-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="047b9-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="047b9-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047b9-126">-이름</span><span class="sxs-lookup"><span data-stu-id="047b9-126">-Name</span></span>
<span data-ttu-id="047b9-127">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="047b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="047b9-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-129">The resource group name.</span></span>

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

### <span data-ttu-id="047b9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="047b9-130">-ResourceId</span></span>
<span data-ttu-id="047b9-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="047b9-132">-확인</span><span class="sxs-lookup"><span data-stu-id="047b9-132">-Confirm</span></span>
<span data-ttu-id="047b9-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="047b9-134">-WhatIf</span></span>
<span data-ttu-id="047b9-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="047b9-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047b9-137">CommonParameters</span></span>
<span data-ttu-id="047b9-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="047b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047b9-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047b9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047b9-140">입력</span><span class="sxs-lookup"><span data-stu-id="047b9-140">INPUTS</span></span>

### <span data-ttu-id="047b9-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="047b9-141">System.String</span></span>

### <span data-ttu-id="047b9-142">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="047b9-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="047b9-143">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="047b9-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="047b9-144">출력</span><span class="sxs-lookup"><span data-stu-id="047b9-144">OUTPUTS</span></span>

### <span data-ttu-id="047b9-145">DataFactoryV2. PSSelfHostedIntegrationRuntimeNode/.</span><span class="sxs-lookup"><span data-stu-id="047b9-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="047b9-146">상속자</span><span class="sxs-lookup"><span data-stu-id="047b9-146">NOTES</span></span>
<span data-ttu-id="047b9-147">키워드: azure, azurerm, arm, resource, management, manager, data, 팩토리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="047b9-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="047b9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="047b9-148">RELATED LINKS</span></span>

<span data-ttu-id="047b9-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="047b9-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

