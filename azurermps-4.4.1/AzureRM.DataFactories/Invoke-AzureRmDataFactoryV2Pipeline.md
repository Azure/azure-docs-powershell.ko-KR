---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: a7486c3fc50e5c6517022190e05d099329fc6001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530794"
---
# <span data-ttu-id="383b6-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="383b6-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="383b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="383b6-102">SYNOPSIS</span></span>
  <span data-ttu-id="383b6-103">파이프라인을 호출 하 여 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="383b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="383b6-104">SYNTAX</span></span>

### <span data-ttu-id="383b6-105">ByFactoryNameByParameterFile (기본값)</span><span class="sxs-lookup"><span data-stu-id="383b6-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383b6-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="383b6-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383b6-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="383b6-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383b6-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="383b6-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="383b6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="383b6-109">DESCRIPTION</span></span>
<span data-ttu-id="383b6-110">**AzureRmDataFactoryV2Pipeline** 명령은 지정 된 파이프라인에서 실행을 시작 하 고 해당 실행에 대 한 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="383b6-111">이 GUID는 **AzureRmDataFactoryV2PipelineRun** 또는 **get-AzureRmDataFactoryV2ActivityRun** 에 전달 되어이 실행에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="383b6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="383b6-112">EXAMPLES</span></span>

### <span data-ttu-id="383b6-113">예제 1: 파이프라인을 호출 하 여 실행 시작</span><span class="sxs-lookup"><span data-stu-id="383b6-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="383b6-114">이 명령은 "WikiADF" 팩터리에서 "DPWikisample" 파이프라인에 대 한 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="383b6-115">변수</span><span class="sxs-lookup"><span data-stu-id="383b6-115">PARAMETERS</span></span>

### <span data-ttu-id="383b6-116">-확인</span><span class="sxs-lookup"><span data-stu-id="383b6-116">-Confirm</span></span>
<span data-ttu-id="383b6-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="383b6-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="383b6-118">-DataFactoryName</span></span>
<span data-ttu-id="383b6-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-119">The data factory name.</span></span>

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

### <span data-ttu-id="383b6-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="383b6-120">-ParameterFile</span></span>
<span data-ttu-id="383b6-121">파이프라인 실행을 위한 매개 변수를 사용 하는 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-121">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="383b6-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="383b6-122">-Parameter</span></span>
<span data-ttu-id="383b6-123">파이프라인 실행을 위한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="383b6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="383b6-124">-InputObject</span></span>
<span data-ttu-id="383b6-125">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-125">The data factory object.</span></span>

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

### <span data-ttu-id="383b6-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="383b6-126">-PipelineName</span></span>
<span data-ttu-id="383b6-127">파이프라인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-127">The pipeline name.</span></span>

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

### <span data-ttu-id="383b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="383b6-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-129">The resource group name.</span></span>

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

### <span data-ttu-id="383b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="383b6-130">-WhatIf</span></span>
<span data-ttu-id="383b6-131">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="383b6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383b6-132">-DefaultProfile</span></span>
<span data-ttu-id="383b6-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="383b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383b6-134">CommonParameters</span></span>
<span data-ttu-id="383b6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="383b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383b6-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="383b6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383b6-137">입력</span><span class="sxs-lookup"><span data-stu-id="383b6-137">INPUTS</span></span>

### <span data-ttu-id="383b6-138">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="383b6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="383b6-139">System.webserver. 컬렉션 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="383b6-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="383b6-140">출력</span><span class="sxs-lookup"><span data-stu-id="383b6-140">OUTPUTS</span></span>

### <span data-ttu-id="383b6-141">DataFactoryV2. PSPipeline/.</span><span class="sxs-lookup"><span data-stu-id="383b6-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="383b6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="383b6-142">NOTES</span></span>

## <span data-ttu-id="383b6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="383b6-143">RELATED LINKS</span></span>

[<span data-ttu-id="383b6-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="383b6-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="383b6-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="383b6-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()
