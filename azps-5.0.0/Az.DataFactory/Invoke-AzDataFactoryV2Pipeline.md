---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306218"
---
# <span data-ttu-id="a0828-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a0828-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="a0828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0828-102">SYNOPSIS</span></span>
  <span data-ttu-id="a0828-103">파이프라인을 호출 하 여 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="a0828-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0828-104">SYNTAX</span></span>

### <span data-ttu-id="a0828-105">ByFactoryNameByParameterFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0828-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0828-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0828-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0828-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="a0828-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0828-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="a0828-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0828-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a0828-109">DESCRIPTION</span></span>
<span data-ttu-id="a0828-110">**AzDataFactoryV2Pipeline** 명령은 지정 된 파이프라인에서 실행을 시작 하 고 해당 실행에 대 한 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="a0828-111">이 GUID는 **AzDataFactoryV2PipelineRun** 또는 **get-AzDataFactoryV2ActivityRun** 에 전달 되어이 실행에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="a0828-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a0828-112">EXAMPLES</span></span>

### <span data-ttu-id="a0828-113">예제 1: 파이프라인을 호출 하 여 실행 시작</span><span class="sxs-lookup"><span data-stu-id="a0828-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="a0828-114">이 명령은 "WikiADF" 팩터리에서 "DPWikisample" 파이프라인에 대 한 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="a0828-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="a0828-115">Example 2</span></span>

<span data-ttu-id="a0828-116">파이프라인을 호출 하 여 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="a0828-117">생성</span><span class="sxs-lookup"><span data-stu-id="a0828-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="a0828-118">변수</span><span class="sxs-lookup"><span data-stu-id="a0828-118">PARAMETERS</span></span>

### <span data-ttu-id="a0828-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a0828-119">-DataFactoryName</span></span>
<span data-ttu-id="a0828-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-120">The data factory name.</span></span>

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

### <span data-ttu-id="a0828-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0828-121">-DefaultProfile</span></span>
<span data-ttu-id="a0828-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0828-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0828-123">-InputObject</span></span>
<span data-ttu-id="a0828-124">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-124">The data factory object.</span></span>

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

### <span data-ttu-id="a0828-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="a0828-125">-IsRecovery</span></span>
<span data-ttu-id="a0828-126">복구 모드 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-126">Recovery mode flag.</span></span> <span data-ttu-id="a0828-127">복구 모드를 true로 설정 하면 지정 된 참조 파이프라인이 실행 되 고 새 실행이 동일한 groupId 아래 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="a0828-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a0828-128">-Parameter</span></span>
<span data-ttu-id="a0828-129">파이프라인 실행을 위한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="a0828-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="a0828-130">-ParameterFile</span></span>
<span data-ttu-id="a0828-131">파이프라인 실행을 위한 매개 변수를 사용 하는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="a0828-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a0828-132">-PipelineName</span></span>
<span data-ttu-id="a0828-133">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-133">The pipeline name.</span></span>

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

### <span data-ttu-id="a0828-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a0828-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="a0828-135">다시 실행에 대 한 파이프라인 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="a0828-136">실행 ID를 지정 하면 지정 된 실행의 매개 변수를 사용 하 여 새 실행이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="a0828-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0828-137">-ResourceGroupName</span></span>
<span data-ttu-id="a0828-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-138">The resource group name.</span></span>

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

### <span data-ttu-id="a0828-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="a0828-139">-StartActivityName</span></span>
<span data-ttu-id="a0828-140">복구 모드에서는이 작업에서 다시 실행이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="a0828-141">지정 하지 않으면 모든 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="a0828-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="a0828-142">-StartFromFailure</span></span>
<span data-ttu-id="a0828-143">실패 한 작업 플래그에서 다시 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="a0828-144">복구 모드에서 지정 된 경우 실패 한 작업에서 다시 실행이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="a0828-145">-확인</span><span class="sxs-lookup"><span data-stu-id="a0828-145">-Confirm</span></span>
<span data-ttu-id="a0828-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0828-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0828-147">-WhatIf</span></span>
<span data-ttu-id="a0828-148">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a0828-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0828-149">CommonParameters</span></span>
<span data-ttu-id="a0828-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0828-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0828-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0828-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0828-152">입력</span><span class="sxs-lookup"><span data-stu-id="a0828-152">INPUTS</span></span>

### <span data-ttu-id="a0828-153">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="a0828-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="a0828-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0828-154">System.String</span></span>

### <span data-ttu-id="a0828-155">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a0828-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0828-156">출력</span><span class="sxs-lookup"><span data-stu-id="a0828-156">OUTPUTS</span></span>

### <span data-ttu-id="a0828-157">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="a0828-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="a0828-158">상속자</span><span class="sxs-lookup"><span data-stu-id="a0828-158">NOTES</span></span>

## <span data-ttu-id="a0828-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0828-159">RELATED LINKS</span></span>

[<span data-ttu-id="a0828-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a0828-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="a0828-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="a0828-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

