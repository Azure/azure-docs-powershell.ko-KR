---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 1b45c08f2906f3b1bec827a7f870d2c901bbb2b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963803"
---
# <span data-ttu-id="f45be-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f45be-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="f45be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45be-102">SYNOPSIS</span></span>
<span data-ttu-id="f45be-103">리소스 그룹 What-If 배포에 대한 템플릿 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-103">Gets a template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="f45be-104">구문</span><span class="sxs-lookup"><span data-stu-id="f45be-104">SYNTAX</span></span>

### <span data-ttu-id="f45be-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="f45be-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f45be-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f45be-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f45be-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f45be-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f45be-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f45be-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f45be-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f45be-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f45be-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f45be-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45be-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f45be-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f45be-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f45be-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45be-117">설명</span><span class="sxs-lookup"><span data-stu-id="f45be-117">DESCRIPTION</span></span>
<span data-ttu-id="f45be-118">**Get-AzResourceGroupDeploymentWhatIfResult** cmdlet은 지정된 리소스 그룹 범위에서 ARM What-If 템플릿 배포 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="f45be-119">실제 리소스를 변경하지 않고 배포가 적용될 경우 업데이트될 리소스를 나타내는 변경 내용 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="f45be-120">반환 결과에 대한 형식을 지정하기 위해 *ResultFormat* 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="f45be-121">예제</span><span class="sxs-lookup"><span data-stu-id="f45be-121">EXAMPLES</span></span>

### <span data-ttu-id="f45be-122">예제 1: 리소스 What-If 범위에서 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="f45be-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="f45be-123">이 명령은 What-If 템플릿 파일 및 디스크의 매개 변수 파일을 사용하여 지정된 리소스 그룹 범위에 대한 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="f45be-124">명령은 *ResourceGroupName* 매개 변수를 사용하여 템플릿이 배포될 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="f45be-125">명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="f45be-126">명령은 *TemplateParameterFile* 매개 변수를 사용하여 템플릿 매개 변수 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="f45be-127">명령은 *ResultFormat* 매개 변수를 사용하여 전체 리소스 페이로드를 What-If 결과를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="f45be-128">예제 2: ResourceIdOnly를 What-If 그룹 범위에서 결과 얻음</span><span class="sxs-lookup"><span data-stu-id="f45be-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="f45be-129">이 명령은 What-If 템플릿 파일 및 디스크의 매개 변수 파일을 사용하여 지정된 리소스 그룹 범위에 대한 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="f45be-130">명령은 *ResourceGroupName* 매개 변수를 사용하여 템플릿이 배포될 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="f45be-131">명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="f45be-132">명령은 *TemplateParameterFile* 매개 변수를 사용하여 템플릿 매개 변수 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="f45be-133">명령은 *ResultFormat* 매개 변수를 사용하여 What-If 결과만 포함하게 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="f45be-134">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f45be-134">PARAMETERS</span></span>

### <span data-ttu-id="f45be-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45be-135">-DefaultProfile</span></span>
<span data-ttu-id="f45be-136">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45be-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="f45be-137">-ExcludeChangeType</span></span>
<span data-ttu-id="f45be-138">결과에서 제외할 콤마로 구분된 리소스 변경 형식을 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="f45be-139">-Mode</span><span class="sxs-lookup"><span data-stu-id="f45be-139">-Mode</span></span>
<span data-ttu-id="f45be-140">배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-140">The deployment mode.</span></span>

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

### <span data-ttu-id="f45be-141">-Name</span><span class="sxs-lookup"><span data-stu-id="f45be-141">-Name</span></span>
<span data-ttu-id="f45be-142">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="f45be-143">지정하지 않으면 템플릿 파일이 제공될 때 템플릿 파일 이름을 기본값으로 지정합니다. 기본값은 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="f45be-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="f45be-144">-Pre</span></span>
<span data-ttu-id="f45be-145">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f45be-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45be-146">-ResourceGroupName</span></span>
<span data-ttu-id="f45be-147">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-147">The resource group name.</span></span>

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

### <span data-ttu-id="f45be-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="f45be-148">-ResultFormat</span></span>
<span data-ttu-id="f45be-149">What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-149">The What-If result format.</span></span>

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

### <span data-ttu-id="f45be-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f45be-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f45be-151">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필요한 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="f45be-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="f45be-152">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 경우 즉시 이 프롬프트와 오류를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="f45be-153">대화형이 아닌 스크립트의 경우 -SkipTemplateParameterPrompt를 제공하여 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f45be-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f45be-154">-TemplateFile</span></span>
<span data-ttu-id="f45be-155">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-155">Local path to the template file.</span></span> <span data-ttu-id="f45be-156">지원되는 템플릿 파일 형식: json 및 bicep입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-156">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="f45be-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f45be-157">-TemplateObject</span></span>
<span data-ttu-id="f45be-158">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-158">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f45be-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f45be-159">-TemplateParameterFile</span></span>
<span data-ttu-id="f45be-160">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-160">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f45be-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f45be-161">-TemplateParameterObject</span></span>
<span data-ttu-id="f45be-162">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-162">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f45be-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f45be-163">-TemplateParameterUri</span></span>
<span data-ttu-id="f45be-164">템플릿 매개 변수 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-164">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f45be-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f45be-165">-TemplateUri</span></span>
<span data-ttu-id="f45be-166">템플릿 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-166">Uri to the template file.</span></span>

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

### <span data-ttu-id="f45be-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45be-167">CommonParameters</span></span>
<span data-ttu-id="f45be-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f45be-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45be-169">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f45be-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45be-170">입력</span><span class="sxs-lookup"><span data-stu-id="f45be-170">INPUTS</span></span>

### <span data-ttu-id="f45be-171">System.String</span><span class="sxs-lookup"><span data-stu-id="f45be-171">System.String</span></span>

### <span data-ttu-id="f45be-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="f45be-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="f45be-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f45be-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f45be-174">출력</span><span class="sxs-lookup"><span data-stu-id="f45be-174">OUTPUTS</span></span>

### <span data-ttu-id="f45be-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="f45be-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="f45be-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f45be-176">NOTES</span></span>

## <span data-ttu-id="f45be-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f45be-177">RELATED LINKS</span></span>
