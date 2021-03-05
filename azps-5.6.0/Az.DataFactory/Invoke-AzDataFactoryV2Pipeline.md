---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: a8e75d6ef44453891660a7d5d35216dace346cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975088"
---
# <span data-ttu-id="8db1c-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8db1c-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8db1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db1c-102">SYNOPSIS</span></span>
  <span data-ttu-id="8db1c-103">파이프라인을 호출하여 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="8db1c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8db1c-104">SYNTAX</span></span>

### <span data-ttu-id="8db1c-105">ByFactoryNameByParameterFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="8db1c-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db1c-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="8db1c-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db1c-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="8db1c-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8db1c-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="8db1c-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db1c-109">설명</span><span class="sxs-lookup"><span data-stu-id="8db1c-109">DESCRIPTION</span></span>
<span data-ttu-id="8db1c-110">**Invoke-AzDataFactoryV2Pipeline** 명령은 지정된 파이프라인에서 실행을 시작하고 이 실행에 대한 ID를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="8db1c-111">이 GUID는 **Get-AzDataFactoryV2PipelineRun** 또는 **Get-AzDataFactoryV2ActivityRun에** 전달하여 이 실행에 대한 자세한 내용을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="8db1c-112">예제</span><span class="sxs-lookup"><span data-stu-id="8db1c-112">EXAMPLES</span></span>

### <span data-ttu-id="8db1c-113">예제 1: 실행을 시작하기 위해 파이프라인을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="8db1c-114">이 명령은 "WikiADF" 팩터리에서 "DPWikisample" 파이프라인에 대한 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="8db1c-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="8db1c-115">Example 2</span></span>

<span data-ttu-id="8db1c-116">파이프라인을 호출하여 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="8db1c-117">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="8db1c-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="8db1c-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8db1c-118">PARAMETERS</span></span>

### <span data-ttu-id="8db1c-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8db1c-119">-DataFactoryName</span></span>
<span data-ttu-id="8db1c-120">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-120">The data factory name.</span></span>

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

### <span data-ttu-id="8db1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db1c-121">-DefaultProfile</span></span>
<span data-ttu-id="8db1c-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db1c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8db1c-123">-InputObject</span></span>
<span data-ttu-id="8db1c-124">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-124">The data factory object.</span></span>

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

### <span data-ttu-id="8db1c-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="8db1c-125">-IsRecovery</span></span>
<span data-ttu-id="8db1c-126">복구 모드 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-126">Recovery mode flag.</span></span> <span data-ttu-id="8db1c-127">복구 모드가 true로 설정되어 있는 경우 지정된 참조 파이프라인 실행 및 새 실행은 동일한 그룹Id 아래에 그룹화됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="8db1c-128">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="8db1c-128">-Parameter</span></span>
<span data-ttu-id="8db1c-129">파이프라인 실행에 대한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="8db1c-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="8db1c-130">-ParameterFile</span></span>
<span data-ttu-id="8db1c-131">파이프라인 실행에 대한 매개 변수가 있는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="8db1c-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8db1c-132">-PipelineName</span></span>
<span data-ttu-id="8db1c-133">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-133">The pipeline name.</span></span>

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

### <span data-ttu-id="8db1c-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="8db1c-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="8db1c-135">파이프라인 실행 ID를 다시 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="8db1c-136">실행 ID가 지정되어 있는 경우 지정된 실행의 매개 변수가 새 실행을 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="8db1c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db1c-137">-ResourceGroupName</span></span>
<span data-ttu-id="8db1c-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-138">The resource group name.</span></span>

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

### <span data-ttu-id="8db1c-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="8db1c-139">-StartActivityName</span></span>
<span data-ttu-id="8db1c-140">복구 모드에서 다시 시작은 이 활동에서 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="8db1c-141">지정하지 않으면 모든 활동이 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="8db1c-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="8db1c-142">-StartFromFailure</span></span>
<span data-ttu-id="8db1c-143">실패한 활동 플래그에서 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="8db1c-144">복구 모드에서 지정한 경우 다시 실행이 실패한 작업에서 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="8db1c-145">-확인</span><span class="sxs-lookup"><span data-stu-id="8db1c-145">-Confirm</span></span>
<span data-ttu-id="8db1c-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db1c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db1c-147">-WhatIf</span></span>
<span data-ttu-id="8db1c-148">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8db1c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db1c-149">CommonParameters</span></span>
<span data-ttu-id="8db1c-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8db1c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db1c-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8db1c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db1c-152">입력</span><span class="sxs-lookup"><span data-stu-id="8db1c-152">INPUTS</span></span>

### <span data-ttu-id="8db1c-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8db1c-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="8db1c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8db1c-154">System.String</span></span>

### <span data-ttu-id="8db1c-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8db1c-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8db1c-156">출력</span><span class="sxs-lookup"><span data-stu-id="8db1c-156">OUTPUTS</span></span>

### <span data-ttu-id="8db1c-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8db1c-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="8db1c-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8db1c-158">NOTES</span></span>

## <span data-ttu-id="8db1c-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8db1c-159">RELATED LINKS</span></span>

[<span data-ttu-id="8db1c-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8db1c-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="8db1c-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="8db1c-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

