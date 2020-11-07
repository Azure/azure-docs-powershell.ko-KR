---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704074"
---
# <span data-ttu-id="f572b-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f572b-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f572b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f572b-102">SYNOPSIS</span></span>
  <span data-ttu-id="f572b-103">파이프라인을 호출 하 여 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f572b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f572b-104">SYNTAX</span></span>

### <span data-ttu-id="f572b-105">ByFactoryNameByParameterFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="f572b-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f572b-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="f572b-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f572b-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="f572b-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f572b-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="f572b-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f572b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f572b-109">DESCRIPTION</span></span>
<span data-ttu-id="f572b-110">**AzureRmDataFactoryV2Pipeline** 명령은 지정 된 파이프라인에서 실행을 시작 하 고 해당 실행에 대 한 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="f572b-111">이 GUID는 **AzureRmDataFactoryV2PipelineRun** 또는 **get-AzureRmDataFactoryV2ActivityRun** 에 전달 되어이 실행에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="f572b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f572b-112">EXAMPLES</span></span>

### <span data-ttu-id="f572b-113">예제 1: 파이프라인을 호출 하 여 실행 시작</span><span class="sxs-lookup"><span data-stu-id="f572b-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="f572b-114">이 명령은 "WikiADF" 팩터리에서 "DPWikisample" 파이프라인에 대 한 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="f572b-115">변수</span><span class="sxs-lookup"><span data-stu-id="f572b-115">PARAMETERS</span></span>

### <span data-ttu-id="f572b-116">-확인</span><span class="sxs-lookup"><span data-stu-id="f572b-116">-Confirm</span></span>
<span data-ttu-id="f572b-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f572b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f572b-118">-DataFactoryName</span></span>
<span data-ttu-id="f572b-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f572b-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="f572b-120">-ParameterFile</span></span>
<span data-ttu-id="f572b-121">파이프라인 실행을 위한 매개 변수를 사용 하는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f572b-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f572b-122">-Parameter</span></span>
<span data-ttu-id="f572b-123">파이프라인 실행을 위한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f572b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f572b-124">-InputObject</span></span>
<span data-ttu-id="f572b-125">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f572b-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f572b-126">-PipelineName</span></span>
<span data-ttu-id="f572b-127">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f572b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f572b-128">-ResourceGroupName</span></span>
<span data-ttu-id="f572b-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f572b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f572b-130">-WhatIf</span></span>
<span data-ttu-id="f572b-131">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f572b-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f572b-132">입력</span><span class="sxs-lookup"><span data-stu-id="f572b-132">INPUTS</span></span>

### <span data-ttu-id="f572b-133">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="f572b-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="f572b-134">System.webserver. 컬렉션 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="f572b-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="f572b-135">출력</span><span class="sxs-lookup"><span data-stu-id="f572b-135">OUTPUTS</span></span>

### <span data-ttu-id="f572b-136">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="f572b-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="f572b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f572b-137">NOTES</span></span>

## <span data-ttu-id="f572b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f572b-138">RELATED LINKS</span></span>
[<span data-ttu-id="f572b-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f572b-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="f572b-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="f572b-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

