---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204405"
---
# <span data-ttu-id="f0519-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f0519-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="f0519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0519-102">SYNOPSIS</span></span>
<span data-ttu-id="f0519-103">자체 호스팅 통합 런타임 노드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="f0519-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0519-104">SYNTAX</span></span>

### <span data-ttu-id="f0519-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f0519-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0519-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0519-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0519-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f0519-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0519-108">설명</span><span class="sxs-lookup"><span data-stu-id="f0519-108">DESCRIPTION</span></span>
<span data-ttu-id="f0519-109">**Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet은 데이터 팩터리에서 자체 호스팅 통합 런타임 노드의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="f0519-110">현재는 'ConcurrentJobsLimit' 업데이트만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="f0519-111">예제</span><span class="sxs-lookup"><span data-stu-id="f0519-111">EXAMPLES</span></span>

### <span data-ttu-id="f0519-112">예제 1: 자체 호스팅 통합 런타임 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="f0519-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="f0519-113">cmdlet은 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 노드 'Node_1'에 대해 'ConcurrentJobsLimit'를 3으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f0519-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0519-114">PARAMETERS</span></span>

### <span data-ttu-id="f0519-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="f0519-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="f0519-116">통합 런타임 노드에서 실행될 수 있는 동시 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="f0519-117">1과 maxConcurrentJobs 사이의 값은 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="f0519-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f0519-118">-DataFactoryName</span></span>
<span data-ttu-id="f0519-119">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-119">The data factory name.</span></span>

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

### <span data-ttu-id="f0519-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0519-120">-DefaultProfile</span></span>
<span data-ttu-id="f0519-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0519-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0519-122">-InputObject</span></span>
<span data-ttu-id="f0519-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="f0519-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f0519-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f0519-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="f0519-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f0519-126">-Name</span></span>
<span data-ttu-id="f0519-127">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="f0519-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0519-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0519-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-129">The resource group name.</span></span>

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

### <span data-ttu-id="f0519-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0519-130">-ResourceId</span></span>
<span data-ttu-id="f0519-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f0519-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0519-132">-Confirm</span></span>
<span data-ttu-id="f0519-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0519-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0519-134">-WhatIf</span></span>
<span data-ttu-id="f0519-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f0519-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0519-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0519-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0519-137">CommonParameters</span></span>
<span data-ttu-id="f0519-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0519-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0519-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0519-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0519-140">입력</span><span class="sxs-lookup"><span data-stu-id="f0519-140">INPUTS</span></span>

### <span data-ttu-id="f0519-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f0519-141">System.String</span></span>

### <span data-ttu-id="f0519-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f0519-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f0519-143">출력</span><span class="sxs-lookup"><span data-stu-id="f0519-143">OUTPUTS</span></span>

### <span data-ttu-id="f0519-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f0519-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f0519-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0519-145">NOTES</span></span>
<span data-ttu-id="f0519-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리, 복사, 활동, 통합 런타임</span><span class="sxs-lookup"><span data-stu-id="f0519-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f0519-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0519-147">RELATED LINKS</span></span>

<span data-ttu-id="f0519-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="f0519-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

