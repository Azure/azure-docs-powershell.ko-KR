---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358016"
---
# <span data-ttu-id="7e137-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7e137-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="7e137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e137-102">SYNOPSIS</span></span>
<span data-ttu-id="7e137-103">관리 그룹에서 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="7e137-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="7e137-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e137-104">SYNTAX</span></span>

### <span data-ttu-id="7e137-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e137-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e137-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7e137-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e137-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7e137-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7e137-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7e137-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7e137-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7e137-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7e137-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7e137-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7e137-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7e137-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e137-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7e137-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e137-117">설명</span><span class="sxs-lookup"><span data-stu-id="7e137-117">DESCRIPTION</span></span>
<span data-ttu-id="7e137-118">**New-AzManagementGroupDeployment** cmdlet은 관리 그룹에 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="7e137-119">관리 그룹에 배포를 추가하기 위해 관리 그룹, 위치 및 템플릿을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="7e137-120">위치는 배포 데이터를 저장할 위치를 Azure Resource Manager에 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="7e137-121">템플릿은 배포할 개별 리소스를 포함하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="7e137-122">템플릿에는 필수 리소스에 대한 매개 변수 자리 지정자 및 구성 가능한 속성 값(예: 이름 및 크기)이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="7e137-123">배포에 사용자 지정 템플릿을 사용하 고 *TemplateFile* 매개 변수 또는 TemplateUri 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="7e137-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="7e137-124">각 템플릿에는 구성 가능한 속성에 대한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="7e137-125">템플릿 매개 변수에 대한 값을 지정하기 위해 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="7e137-126">또는 템플릿을 지정할 때 명령에 동적으로 추가되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="7e137-127">동적 매개 변수를 사용하거나 명령 프롬프트에 입력하거나, 매개 변수를 나타내기 위해 마이너스 기호(-)를 입력하고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="7e137-128">명령 프롬프트에 입력하는 템플릿 매개 변수 값은 템플릿 매개 변수 개체 또는 파일의 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="7e137-129">리소스 그룹에 리소스를 추가하기 위해 리소스 그룹에 배포를 만드는 **New-AzResourceGroupDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="7e137-130">구독에 리소스를 추가하려면 구독 수준 리소스를 배포하는 구독 범위에서 배포를 만드는 **New-AzSubscriptionDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="7e137-131">테넌트 범위에서 리소스를 추가하기 위해 테넌트 범위에서 배포를 만드는 **New-AzTenantDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="7e137-132">예제</span><span class="sxs-lookup"><span data-stu-id="7e137-132">EXAMPLES</span></span>

### <span data-ttu-id="7e137-133">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="7e137-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="7e137-134">이 명령은 정의된 태그 매개 변수를 사용하여 사용자 지정 템플릿 및 디스크의 템플릿 파일을 사용하여 관리 그룹 "myMG"에 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="7e137-135">이 명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="7e137-136">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="7e137-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="7e137-137">이 명령은 사용자 지정 템플릿 및 메모리 내 해시테이블로 변환된 디스크의 템플릿 파일을 사용하여 관리 그룹 "myMG"에 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="7e137-138">처음 두 명령은 디스크의 템플릿 파일에 대한 텍스트를 읽고 메모리 내 해시테이블로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="7e137-139">마지막 명령은 *TemplateObject* 매개 변수를 사용하여 이 해시테이블을 지정하고 *TemplateParameterFile* 매개 변수를 사용하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="7e137-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e137-140">PARAMETERS</span></span>

### <span data-ttu-id="7e137-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e137-141">-AsJob</span></span>
<span data-ttu-id="7e137-142">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7e137-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e137-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e137-143">-DefaultProfile</span></span>
<span data-ttu-id="7e137-144">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e137-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="7e137-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="7e137-146">배포 디버그 로그 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="7e137-147">-Location</span><span class="sxs-lookup"><span data-stu-id="7e137-147">-Location</span></span>
<span data-ttu-id="7e137-148">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="7e137-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7e137-149">-ManagementGroupId</span></span>
<span data-ttu-id="7e137-150">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-150">The management group ID.</span></span>

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

### <span data-ttu-id="7e137-151">-Name</span><span class="sxs-lookup"><span data-stu-id="7e137-151">-Name</span></span>
<span data-ttu-id="7e137-152">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="7e137-153">지정하지 않으면 템플릿 파일이 제공될 때 기본적으로 템플릿 파일 이름이 지정됩니다. 기본적으로 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e137-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="7e137-154">-Pre</span></span>
<span data-ttu-id="7e137-155">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7e137-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7e137-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7e137-157">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="7e137-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7e137-158">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7e137-159">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7e137-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e137-160">-Tag</span></span>
<span data-ttu-id="7e137-161">배포에 배치할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-161">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e137-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7e137-162">-TemplateFile</span></span>
<span data-ttu-id="7e137-163">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="7e137-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="7e137-164">-TemplateObject</span></span>
<span data-ttu-id="7e137-165">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7e137-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7e137-166">-TemplateParameterFile</span></span>
<span data-ttu-id="7e137-167">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7e137-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7e137-168">-TemplateParameterObject</span></span>
<span data-ttu-id="7e137-169">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7e137-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7e137-170">-TemplateParameterUri</span></span>
<span data-ttu-id="7e137-171">템플릿 매개 변수 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7e137-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7e137-172">-TemplateUri</span></span>
<span data-ttu-id="7e137-173">템플릿 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="7e137-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="7e137-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="7e137-175">결과에서 제외할 콤마로 구분된 리소스 변경 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="7e137-176">-WhatIf 또는 -Confirm 스위치가 설정된 경우 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="7e137-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="7e137-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="7e137-178">결과 What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-178">The What-If result format.</span></span> <span data-ttu-id="7e137-179">-WhatIf 또는 -Confirm 스위치가 설정된 경우 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="7e137-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e137-180">-Confirm</span></span>
<span data-ttu-id="7e137-181">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e137-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e137-182">-WhatIf</span></span>
<span data-ttu-id="7e137-183">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e137-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e137-184">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e137-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e137-185">CommonParameters</span></span>
<span data-ttu-id="7e137-186">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e137-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e137-187">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e137-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e137-188">입력</span><span class="sxs-lookup"><span data-stu-id="7e137-188">INPUTS</span></span>

### <span data-ttu-id="7e137-189">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e137-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7e137-190">System.String</span><span class="sxs-lookup"><span data-stu-id="7e137-190">System.String</span></span>

## <span data-ttu-id="7e137-191">출력</span><span class="sxs-lookup"><span data-stu-id="7e137-191">OUTPUTS</span></span>

### <span data-ttu-id="7e137-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="7e137-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7e137-193">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e137-193">NOTES</span></span>

## <span data-ttu-id="7e137-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e137-194">RELATED LINKS</span></span>
