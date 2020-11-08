---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: aa011c7a858f08e3528fb2cdd7d67bcff37d76d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204444"
---
# <span data-ttu-id="ed628-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="ed628-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="ed628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed628-102">SYNOPSIS</span></span>
<span data-ttu-id="ed628-103">리소스 그룹 범위에서 배포에 대 한 결과를 What-If 팔 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="ed628-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed628-104">SYNTAX</span></span>

### <span data-ttu-id="ed628-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed628-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed628-106">By서식 Objectandparameterobject</span><span class="sxs-lookup"><span data-stu-id="ed628-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-107">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="ed628-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-108">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="ed628-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-109">By서식 Objectandparameterfile</span><span class="sxs-lookup"><span data-stu-id="ed628-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-110">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="ed628-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-111">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="ed628-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-112">By서식 Objectandparameteruri</span><span class="sxs-lookup"><span data-stu-id="ed628-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-113">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="ed628-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-114">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="ed628-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed628-115">By서식 Objectwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="ed628-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed628-116">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="ed628-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed628-117">설명은</span><span class="sxs-lookup"><span data-stu-id="ed628-117">DESCRIPTION</span></span>
<span data-ttu-id="ed628-118">**AzResourceGroupDeploymentWhatIfResult** cmdlet은 지정 된 리소스 그룹 범위에서 템플릿 배포에 대 한 결과 What-If 팔 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="ed628-119">이 메서드는 실제 리소스를 변경 하지 않고 배포를 적용 한 경우 업데이트 되는 리소스를 표시 하는 변경 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="ed628-120">반환 되는 결과의 형식을 지정 하려면 *Resultformat* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="ed628-121">예제의</span><span class="sxs-lookup"><span data-stu-id="ed628-121">EXAMPLES</span></span>

### <span data-ttu-id="ed628-122">예제 1: 리소스 그룹 범위에서 What-If 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="ed628-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="ed628-123">이 명령은 사용자 지정 템플릿 파일과 디스크의 매개 변수 파일을 사용 하 여 지정 된 리소스 그룹 범위에서 What-If 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="ed628-124">이 명령은 *ResourceGroupName* 매개 변수를 사용 하 여 템플릿이 배포 될 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="ed628-125">이 명령은 template 파일 *매개 변수* 를 사용 하 여 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="ed628-126">이 명령은 서식 파일 매개 변수 파일을 지정 *하는 데* 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="ed628-127">명령에서 *Resultformat* 매개 변수를 사용 하 여 전체 리소스 페이로드를 포함 하도록 What-If 결과를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="ed628-128">예제 2: ResourceIdOnly를 사용 하 여 리소스 그룹 범위에서 What-If 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="ed628-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="ed628-129">이 명령은 사용자 지정 템플릿 파일과 디스크의 매개 변수 파일을 사용 하 여 지정 된 리소스 그룹 범위에서 What-If 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="ed628-130">이 명령은 *ResourceGroupName* 매개 변수를 사용 하 여 템플릿이 배포 될 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="ed628-131">이 명령은 template 파일 *매개 변수* 를 사용 하 여 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="ed628-132">이 명령은 서식 파일 매개 변수 파일을 지정 *하는 데* 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="ed628-133">명령에서 *Resultformat* 매개 변수를 사용 하 여 What-If 결과를 리소스 id만 포함 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="ed628-134">변수</span><span class="sxs-lookup"><span data-stu-id="ed628-134">PARAMETERS</span></span>

### <span data-ttu-id="ed628-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed628-135">-ApiVersion</span></span>
<span data-ttu-id="ed628-136">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ed628-137">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-137">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed628-138">-DefaultProfile</span></span>
<span data-ttu-id="ed628-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed628-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="ed628-140">-ExcludeChangeType</span></span>
<span data-ttu-id="ed628-141">What-If 결과에서 제외할 쉼표로 구분 된 리소스 변경 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-141">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-142">-모드</span><span class="sxs-lookup"><span data-stu-id="ed628-142">-Mode</span></span>
<span data-ttu-id="ed628-143">배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-143">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-144">-이름</span><span class="sxs-lookup"><span data-stu-id="ed628-144">-Name</span></span>
<span data-ttu-id="ed628-145">만들려는 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="ed628-146">지정 하지 않으면 템플릿 파일이 제공 될 때 기본적으로 템플릿 파일 이름이 만들어집니다. 템플릿 개체가 제공 되는 현재 시간을 기본값으로 설정 합니다 (예: "20131223140835").</span><span class="sxs-lookup"><span data-stu-id="ed628-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="ed628-147">-Pre</span></span>
<span data-ttu-id="ed628-148">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ed628-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed628-149">-ResourceGroupName</span></span>
<span data-ttu-id="ed628-150">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-150">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-151">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="ed628-151">-ResultFormat</span></span>
<span data-ttu-id="ed628-152">What-If 결과 서식입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-152">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-153">-Skip서식 Parameterprompt</span><span class="sxs-lookup"><span data-stu-id="ed628-153">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ed628-154">제공 된 템플릿 매개 변수에 템플릿에서 사용 되는 필요한 모든 매개 변수가 포함 되어 있는지 확인 하는 PowerShell 동적 매개 변수 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-154">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="ed628-155">이 검사는 누락 된 매개 변수에 대해 사용자에 게 값을 제공 하 라는 메시지를 표시 하지만-Skiptemplate Parameterprompt는이 프롬프트를 무시 하 고 매개 변수를 템플릿에 바인딩하지 않은 경우 즉시 오류를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-155">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="ed628-156">비 대화형 스크립트의 경우-Skip비템플릿 Parameterprompt를 제공 하 여 필요한 모든 매개 변수가 충족 되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-156">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ed628-157">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="ed628-157">-TemplateFile</span></span>
<span data-ttu-id="ed628-158">서식 파일에 대 한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-158">Local path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-159">-서식 개체</span><span class="sxs-lookup"><span data-stu-id="ed628-159">-TemplateObject</span></span>
<span data-ttu-id="ed628-160">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-160">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-161">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="ed628-161">-TemplateParameterFile</span></span>
<span data-ttu-id="ed628-162">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-162">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-163">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="ed628-163">-TemplateParameterObject</span></span>
<span data-ttu-id="ed628-164">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-164">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-165">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="ed628-165">-TemplateParameterUri</span></span>
<span data-ttu-id="ed628-166">Template 매개 변수 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-166">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-167">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="ed628-167">-TemplateUri</span></span>
<span data-ttu-id="ed628-168">템플릿 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-168">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed628-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed628-169">CommonParameters</span></span>
<span data-ttu-id="ed628-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed628-171">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ed628-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed628-172">입력</span><span class="sxs-lookup"><span data-stu-id="ed628-172">INPUTS</span></span>

### <span data-ttu-id="ed628-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed628-173">System.String</span></span>

### <span data-ttu-id="ed628-174">DeploymentMode를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-174">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="ed628-175">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ed628-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ed628-176">출력</span><span class="sxs-lookup"><span data-stu-id="ed628-176">OUTPUTS</span></span>

### <span data-ttu-id="ed628-177">SdkModels. PSWhatIfOperationResult를 함께 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed628-177">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="ed628-178">상속자</span><span class="sxs-lookup"><span data-stu-id="ed628-178">NOTES</span></span>

## <span data-ttu-id="ed628-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed628-179">RELATED LINKS</span></span>
