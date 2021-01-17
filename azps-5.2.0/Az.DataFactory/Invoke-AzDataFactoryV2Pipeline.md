---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336350"
---
# <span data-ttu-id="78f38-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="78f38-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="78f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f38-102">SYNOPSIS</span></span>
  <span data-ttu-id="78f38-103">파이프라인을 호출하여 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="78f38-104">구문</span><span class="sxs-lookup"><span data-stu-id="78f38-104">SYNTAX</span></span>

### <span data-ttu-id="78f38-105">ByFactoryNameByParameterFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="78f38-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f38-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="78f38-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f38-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="78f38-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f38-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="78f38-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f38-109">설명</span><span class="sxs-lookup"><span data-stu-id="78f38-109">DESCRIPTION</span></span>
<span data-ttu-id="78f38-110">**Invoke-AzDataFactoryV2Pipeline** 명령은 지정된 파이프라인에서 실행을 시작하고 이 실행에 대한 ID를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="78f38-111">이 GUID는 **Get-AzDataFactoryV2PipelineRun** 또는 **Get-AzDataFactoryV2ActivityRun에** 전달하여 이 실행에 대한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="78f38-112">예제</span><span class="sxs-lookup"><span data-stu-id="78f38-112">EXAMPLES</span></span>

### <span data-ttu-id="78f38-113">예제 1: 파이프라인을 호출하여 실행 시작</span><span class="sxs-lookup"><span data-stu-id="78f38-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="78f38-114">이 명령은 "WikiADF" 팩터리에서 "DPWikisample" 파이프라인에 대한 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="78f38-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="78f38-115">Example 2</span></span>

<span data-ttu-id="78f38-116">파이프라인을 호출하여 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="78f38-117">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="78f38-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="78f38-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78f38-118">PARAMETERS</span></span>

### <span data-ttu-id="78f38-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78f38-119">-DataFactoryName</span></span>
<span data-ttu-id="78f38-120">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f38-121">-DefaultProfile</span></span>
<span data-ttu-id="78f38-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78f38-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f38-123">-InputObject</span></span>
<span data-ttu-id="78f38-124">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-124">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="78f38-125">-IsRecovery</span></span>
<span data-ttu-id="78f38-126">복구 모드 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-126">Recovery mode flag.</span></span> <span data-ttu-id="78f38-127">복구 모드가 true로 설정된 경우 지정된 참조된 파이프라인 실행 및 새 실행이 동일한 groupId 아래에 그룹화됩니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="78f38-128">-Parameter</span></span>
<span data-ttu-id="78f38-129">파이프라인 실행에 대한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="78f38-130">-ParameterFile</span></span>
<span data-ttu-id="78f38-131">파이프라인 실행에 대한 매개 변수가 있는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="78f38-132">-PipelineName</span></span>
<span data-ttu-id="78f38-133">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="78f38-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="78f38-135">다시 실행에 대한 파이프라인 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="78f38-136">실행 ID를 지정하면 지정된 실행의 매개 변수를 사용하여 새 실행을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f38-137">-ResourceGroupName</span></span>
<span data-ttu-id="78f38-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="78f38-139">-StartActivityName</span></span>
<span data-ttu-id="78f38-140">복구 모드에서 다시 시작은 이 작업에서 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="78f38-141">지정하지 않으면 모든 활동이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="78f38-142">-StartFromFailure</span></span>
<span data-ttu-id="78f38-143">실패한 활동 플래그에서 다시 시작</span><span class="sxs-lookup"><span data-stu-id="78f38-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="78f38-144">복구 모드에서 지정된 경우 다시 실행은 실패한 활동에서 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f38-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78f38-145">-Confirm</span></span>
<span data-ttu-id="78f38-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f38-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f38-147">-WhatIf</span></span>
<span data-ttu-id="78f38-148">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="78f38-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f38-149">CommonParameters</span></span>
<span data-ttu-id="78f38-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78f38-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f38-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78f38-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f38-152">입력</span><span class="sxs-lookup"><span data-stu-id="78f38-152">INPUTS</span></span>

### <span data-ttu-id="78f38-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="78f38-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="78f38-154">System.String</span><span class="sxs-lookup"><span data-stu-id="78f38-154">System.String</span></span>

### <span data-ttu-id="78f38-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="78f38-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="78f38-156">출력</span><span class="sxs-lookup"><span data-stu-id="78f38-156">OUTPUTS</span></span>

### <span data-ttu-id="78f38-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="78f38-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="78f38-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78f38-158">NOTES</span></span>

## <span data-ttu-id="78f38-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78f38-159">RELATED LINKS</span></span>

[<span data-ttu-id="78f38-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="78f38-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="78f38-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="78f38-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

