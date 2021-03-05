---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: da2a2bc6d7c35f6d7f092123dce08496f491655b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003120"
---
# <span data-ttu-id="e82a1-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e82a1-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="e82a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e82a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e82a1-103">관리 그룹에서 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="e82a1-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="e82a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="e82a1-104">SYNTAX</span></span>

### <span data-ttu-id="e82a1-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="e82a1-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e82a1-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e82a1-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e82a1-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e82a1-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="e82a1-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e82a1-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e82a1-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e82a1-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="e82a1-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e82a1-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e82a1-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e82a1-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="e82a1-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e82a1-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e82a1-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e82a1-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e82a1-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e82a1-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="e82a1-120">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e82a1-121">설명</span><span class="sxs-lookup"><span data-stu-id="e82a1-121">DESCRIPTION</span></span>
<span data-ttu-id="e82a1-122">**New-AzManagementGroupDeployment** cmdlet은 관리 그룹에 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-122">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="e82a1-123">관리 그룹에 배포를 추가하기 위해 관리 그룹, 위치 및 템플릿을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-123">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="e82a1-124">위치는 배포 데이터를 저장할 위치를 Azure Resource Manager에 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="e82a1-125">템플릿은 배포할 개별 리소스를 포함하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="e82a1-126">템플릿에는 필수 리소스 및 구성 가능한 속성 값(예: 이름 및 크기)에 대한 매개 변수 자리 를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="e82a1-127">배포에 사용자 지정 템플릿을 사용하 는 *템플릿File* 매개 변수 또는 *TemplateUri 매개 변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="e82a1-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="e82a1-128">각 템플릿에는 구성 가능한 속성에 대한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="e82a1-129">템플릿 매개 변수에 대한 값을 지정하기 위해 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e82a1-130">또는 템플릿을 지정할 때 명령에 동적으로 추가되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e82a1-131">동적 매개 변수를 사용하거나 명령 프롬프트에 입력하거나 마이너스 기호(-)를 입력하여 매개 변수를 나타내고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="e82a1-132">명령 프롬프트에 입력하는 템플릿 매개 변수 값은 템플릿 매개 변수 개체 또는 파일의 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="e82a1-133">리소스 그룹에 리소스를 추가하기 위해 리소스 그룹에 배포를 만드는 **New-AzResourceGroupDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="e82a1-134">구독에 리소스를 추가하려면 구독 수준 리소스를 배포하는 구독 범위에 배포를 만드는 **New-AzSubscriptionDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="e82a1-135">테넌트 범위에서 리소스를 추가하기 위해 테넌트 범위에서 배포를 만드는 **New-AzTenantDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-135">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="e82a1-136">예제</span><span class="sxs-lookup"><span data-stu-id="e82a1-136">EXAMPLES</span></span>

### <span data-ttu-id="e82a1-137">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="e82a1-138">이 명령은 정의된 태그 매개 변수를 사용하여 디스크의 사용자 지정 템플릿 및 템플릿 파일을 사용하여 관리 그룹 "myMG"에 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-138">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="e82a1-139">명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="e82a1-140">예제 2: uri 및 SAS 토큰을 사용하여 공용 저장소 계정이 아닌 저장소 계정에 저장된 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="e82a1-140">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="e82a1-141">이 명령은 공용이 아니며 QueryString 매개 변수를 사용하여 제공되는 액세스하려면 토큰 매개 변수가 필요한 TemplateUri의 템플릿을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-141">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="e82a1-142">이 명령을 실행하면 URL을 사용하여 템플릿에 효과적으로 https://example.com/example.json?foo 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-142">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="e82a1-143">SAS 토큰을 QueryString으로 제공하여 저장소 계정에서 템플릿을 사용하려는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-143">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="e82a1-144">예제 3: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-144">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="e82a1-145">이 명령은 메모리 내 해시테이블로 변환된 디스크의 사용자 지정 템플릿 및 템플릿 파일을 사용하여 관리 그룹 "myMG"에 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-145">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="e82a1-146">처음 두 명령은 디스크의 템플릿 파일에 대한 텍스트를 읽고 메모리 내 해시테이블로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-146">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="e82a1-147">마지막 명령은 *TemplateObject* 매개 변수를 사용하여 이 해시테이블 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-147">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="e82a1-148">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e82a1-148">PARAMETERS</span></span>

### <span data-ttu-id="e82a1-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e82a1-149">-AsJob</span></span>
<span data-ttu-id="e82a1-150">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e82a1-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e82a1-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82a1-151">-DefaultProfile</span></span>
<span data-ttu-id="e82a1-152">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e82a1-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="e82a1-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="e82a1-154">배포 로그 수준을 디버그합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="e82a1-155">-Location</span><span class="sxs-lookup"><span data-stu-id="e82a1-155">-Location</span></span>
<span data-ttu-id="e82a1-156">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="e82a1-157">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e82a1-157">-ManagementGroupId</span></span>
<span data-ttu-id="e82a1-158">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-158">The management group ID.</span></span>

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

### <span data-ttu-id="e82a1-159">-Name</span><span class="sxs-lookup"><span data-stu-id="e82a1-159">-Name</span></span>
<span data-ttu-id="e82a1-160">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-160">The name of the deployment it's going to create.</span></span> <span data-ttu-id="e82a1-161">지정하지 않으면 템플릿 파일이 제공될 때 템플릿 파일 이름을 기본값으로 지정합니다. 기본값은 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-161">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="e82a1-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="e82a1-162">-Pre</span></span>
<span data-ttu-id="e82a1-163">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-163">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e82a1-164">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e82a1-164">-QueryString</span></span>
<span data-ttu-id="e82a1-165">TemplateUri 매개 변수와 함께 사용할 쿼리 문자열(예: SAS 토큰)입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-165">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="e82a1-166">연결된 템플릿의 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-166">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="e82a1-167">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e82a1-167">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e82a1-168">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필요한 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="e82a1-168">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="e82a1-169">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 경우 즉시 이 프롬프트와 오류를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-169">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="e82a1-170">대화형이 아닌 스크립트의 경우 -SkipTemplateParameterPrompt를 제공하여 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-170">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e82a1-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="e82a1-171">-Tag</span></span>
<span data-ttu-id="e82a1-172">배포에 넣을 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-172">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="e82a1-173">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e82a1-173">-TemplateFile</span></span>
<span data-ttu-id="e82a1-174">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-174">Local path to the template file.</span></span> <span data-ttu-id="e82a1-175">지원되는 템플릿 파일 형식: json 및 bicep입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-175">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="e82a1-176">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e82a1-176">-TemplateObject</span></span>
<span data-ttu-id="e82a1-177">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-177">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e82a1-178">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e82a1-178">-TemplateParameterFile</span></span>
<span data-ttu-id="e82a1-179">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-179">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a1-180">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e82a1-180">-TemplateParameterObject</span></span>
<span data-ttu-id="e82a1-181">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-181">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a1-182">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e82a1-182">-TemplateParameterUri</span></span>
<span data-ttu-id="e82a1-183">템플릿 매개 변수 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-183">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a1-184">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="e82a1-184">-TemplateSpecId</span></span>
<span data-ttu-id="e82a1-185">배포할 템플릿Spec의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-185">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a1-186">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e82a1-186">-TemplateUri</span></span>
<span data-ttu-id="e82a1-187">템플릿 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-187">Uri to the template file.</span></span>

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

### <span data-ttu-id="e82a1-188">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="e82a1-188">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="e82a1-189">결과에서 제외할 콤마로 구분된 리소스 변경 형식을 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-189">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="e82a1-190">-WhatIf 또는 -Confirm 스위치가 설정된 경우 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-190">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="e82a1-191">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="e82a1-191">-WhatIfResultFormat</span></span>
<span data-ttu-id="e82a1-192">What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-192">The What-If result format.</span></span> <span data-ttu-id="e82a1-193">-WhatIf 또는 -Confirm 스위치가 설정된 경우 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="e82a1-194">-확인</span><span class="sxs-lookup"><span data-stu-id="e82a1-194">-Confirm</span></span>
<span data-ttu-id="e82a1-195">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e82a1-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e82a1-196">-WhatIf</span></span>
<span data-ttu-id="e82a1-197">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e82a1-198">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e82a1-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82a1-199">CommonParameters</span></span>
<span data-ttu-id="e82a1-200">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e82a1-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82a1-201">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e82a1-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82a1-202">입력</span><span class="sxs-lookup"><span data-stu-id="e82a1-202">INPUTS</span></span>

### <span data-ttu-id="e82a1-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e82a1-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e82a1-204">System.String</span><span class="sxs-lookup"><span data-stu-id="e82a1-204">System.String</span></span>

## <span data-ttu-id="e82a1-205">출력</span><span class="sxs-lookup"><span data-stu-id="e82a1-205">OUTPUTS</span></span>

### <span data-ttu-id="e82a1-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDMicrosoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="e82a1-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e82a1-207">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e82a1-207">NOTES</span></span>

## <span data-ttu-id="e82a1-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e82a1-208">RELATED LINKS</span></span>
