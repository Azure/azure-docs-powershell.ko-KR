---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 096ee403a0ee12c80462a1fb87db4378e3d86f01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998466"
---
# <span data-ttu-id="e8e29-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e8e29-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="e8e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8e29-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e29-103">데이터 팩터리에서 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="e8e29-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8e29-104">SYNTAX</span></span>

### <span data-ttu-id="e8e29-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8e29-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e29-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8e29-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e29-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8e29-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8e29-108">설명</span><span class="sxs-lookup"><span data-stu-id="e8e29-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e29-109">**Stop-AzDataFactoryV2PipelineRun** cmdlet은 파이프라인 실행 ID로 지정된 데이터 팩터리에서 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="e8e29-110">예제</span><span class="sxs-lookup"><span data-stu-id="e8e29-110">EXAMPLES</span></span>

### <span data-ttu-id="e8e29-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8e29-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="e8e29-112">이 명령은 공장 WikiADF에서 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd를 사용하여 파이프라인 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="e8e29-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8e29-113">PARAMETERS</span></span>

### <span data-ttu-id="e8e29-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8e29-114">-DataFactory</span></span>
<span data-ttu-id="e8e29-115">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e29-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8e29-116">-DataFactoryName</span></span>
<span data-ttu-id="e8e29-117">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e29-118">-DefaultProfile</span></span>
<span data-ttu-id="e8e29-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8e29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e29-120">-InputObject</span></span>
<span data-ttu-id="e8e29-121">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e29-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8e29-122">-PassThru</span></span>
<span data-ttu-id="e8e29-123">cmdlet 쓰기를 지정한 경우 작업이 성공하는 경우 true입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-123">If specified the cmdlet write true in case operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e29-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e8e29-124">-PipelineRunId</span></span>
<span data-ttu-id="e8e29-125">파이프라인의 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e29-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e29-126">-ResourceGroupName</span></span>
<span data-ttu-id="e8e29-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e29-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e8e29-128">-Confirm</span></span>
<span data-ttu-id="e8e29-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e29-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e29-130">-WhatIf</span></span>
<span data-ttu-id="e8e29-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8e29-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e29-133">CommonParameters</span></span>
<span data-ttu-id="e8e29-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e29-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8e29-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e29-136">입력</span><span class="sxs-lookup"><span data-stu-id="e8e29-136">INPUTS</span></span>

### <span data-ttu-id="e8e29-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e8e29-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="e8e29-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e8e29-138">System.String</span></span>

### <span data-ttu-id="e8e29-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8e29-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e8e29-140">출력</span><span class="sxs-lookup"><span data-stu-id="e8e29-140">OUTPUTS</span></span>

### <span data-ttu-id="e8e29-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8e29-141">System.Boolean</span></span>

## <span data-ttu-id="e8e29-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8e29-142">NOTES</span></span>

## <span data-ttu-id="e8e29-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8e29-143">RELATED LINKS</span></span>
