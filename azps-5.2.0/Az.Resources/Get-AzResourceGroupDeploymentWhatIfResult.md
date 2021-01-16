---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340497"
---
# <span data-ttu-id="efee5-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="efee5-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="efee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efee5-102">SYNOPSIS</span></span>
<span data-ttu-id="efee5-103">리소스 ARM 배포에 What-If 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="efee5-104">구문</span><span class="sxs-lookup"><span data-stu-id="efee5-104">SYNTAX</span></span>

### <span data-ttu-id="efee5-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="efee5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efee5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="efee5-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="efee5-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="efee5-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="efee5-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="efee5-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="efee5-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="efee5-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="efee5-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="efee5-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efee5-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="efee5-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efee5-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="efee5-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efee5-117">설명</span><span class="sxs-lookup"><span data-stu-id="efee5-117">DESCRIPTION</span></span>
<span data-ttu-id="efee5-118">**Get-AzResourceGroupDeploymentWhatIfResult** cmdlet은 지정된 리소스 그룹 범위에서 ARM 배포하기 위한 What-If 템플릿 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="efee5-119">실제 리소스를 변경하지 않고 배포가 적용될 경우 업데이트될 리소스를 나타내는 변경 내용 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="efee5-120">반환 결과에 대한 형식을 지정하기 위해 *ResultFormat* 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="efee5-121">예제</span><span class="sxs-lookup"><span data-stu-id="efee5-121">EXAMPLES</span></span>

### <span data-ttu-id="efee5-122">예제 1: 리소스 What-If 결과 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="efee5-123">이 명령은 What-If 템플릿 파일 및 디스크의 매개 변수 파일을 사용하여 지정된 리소스 그룹 범위에서 새 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="efee5-124">이 명령은 *ResourceGroupName* 매개 변수를 사용하여 템플릿을 배포할 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="efee5-125">이 명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="efee5-126">이 명령은 *TemplateParameterFile* 매개 변수를 사용하여 템플릿 매개 변수 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="efee5-127">이 명령은 *ResultFormat* 매개 변수를 사용하여 전체 리소스 페이로드를 What-If 결과를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="efee5-128">예제 2: ResourceIdOnly를 What-If 리소스 그룹 범위에서 결과 얻음</span><span class="sxs-lookup"><span data-stu-id="efee5-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="efee5-129">이 명령은 What-If 템플릿 파일 및 디스크의 매개 변수 파일을 사용하여 지정된 리소스 그룹 범위에서 새 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="efee5-130">이 명령은 *ResourceGroupName* 매개 변수를 사용하여 템플릿을 배포할 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="efee5-131">이 명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="efee5-132">이 명령은 *TemplateParameterFile* 매개 변수를 사용하여 템플릿 매개 변수 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="efee5-133">이 명령은 *ResultFormat* 매개 변수를 사용하여 리소스 What-If 수만 포함하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="efee5-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efee5-134">PARAMETERS</span></span>

### <span data-ttu-id="efee5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efee5-135">-DefaultProfile</span></span>
<span data-ttu-id="efee5-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efee5-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="efee5-137">-ExcludeChangeType</span></span>
<span data-ttu-id="efee5-138">결과에서 제외할 콤마로 구분된 리소스 변경 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="efee5-139">-Mode</span><span class="sxs-lookup"><span data-stu-id="efee5-139">-Mode</span></span>
<span data-ttu-id="efee5-140">배포 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-140">The deployment mode.</span></span>

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

### <span data-ttu-id="efee5-141">-Name</span><span class="sxs-lookup"><span data-stu-id="efee5-141">-Name</span></span>
<span data-ttu-id="efee5-142">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="efee5-143">지정하지 않으면 템플릿 파일이 제공될 때 기본적으로 템플릿 파일 이름이 지정됩니다. 기본적으로 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="efee5-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="efee5-144">-Pre</span></span>
<span data-ttu-id="efee5-145">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="efee5-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efee5-146">-ResourceGroupName</span></span>
<span data-ttu-id="efee5-147">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-147">The resource group name.</span></span>

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

### <span data-ttu-id="efee5-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="efee5-148">-ResultFormat</span></span>
<span data-ttu-id="efee5-149">결과 What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-149">The What-If result format.</span></span>

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

### <span data-ttu-id="efee5-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="efee5-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="efee5-151">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="efee5-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="efee5-152">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="efee5-153">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="efee5-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="efee5-154">-TemplateFile</span></span>
<span data-ttu-id="efee5-155">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="efee5-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="efee5-156">-TemplateObject</span></span>
<span data-ttu-id="efee5-157">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-157">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="efee5-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="efee5-158">-TemplateParameterFile</span></span>
<span data-ttu-id="efee5-159">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-159">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="efee5-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="efee5-160">-TemplateParameterObject</span></span>
<span data-ttu-id="efee5-161">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-161">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="efee5-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="efee5-162">-TemplateParameterUri</span></span>
<span data-ttu-id="efee5-163">템플릿 매개 변수 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-163">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="efee5-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="efee5-164">-TemplateUri</span></span>
<span data-ttu-id="efee5-165">템플릿 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-165">Uri to the template file.</span></span>

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

### <span data-ttu-id="efee5-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efee5-166">CommonParameters</span></span>
<span data-ttu-id="efee5-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efee5-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efee5-168">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="efee5-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efee5-169">입력</span><span class="sxs-lookup"><span data-stu-id="efee5-169">INPUTS</span></span>

### <span data-ttu-id="efee5-170">System.String</span><span class="sxs-lookup"><span data-stu-id="efee5-170">System.String</span></span>

### <span data-ttu-id="efee5-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="efee5-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="efee5-172">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="efee5-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="efee5-173">출력</span><span class="sxs-lookup"><span data-stu-id="efee5-173">OUTPUTS</span></span>

### <span data-ttu-id="efee5-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="efee5-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="efee5-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efee5-175">NOTES</span></span>

## <span data-ttu-id="efee5-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efee5-176">RELATED LINKS</span></span>
