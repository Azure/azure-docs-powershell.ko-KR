---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: ad5979d65565107ac071bcaac94bc178b8c36d1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490420"
---
# <span data-ttu-id="5f54b-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5f54b-101">New-AzDeployment</span></span>

## <span data-ttu-id="5f54b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f54b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f54b-103">배포 만들기</span><span class="sxs-lookup"><span data-stu-id="5f54b-103">Create a deployment</span></span>

## <span data-ttu-id="5f54b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f54b-104">SYNTAX</span></span>

### <span data-ttu-id="5f54b-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="5f54b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f54b-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f54b-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f54b-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f54b-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f54b-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f54b-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f54b-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f54b-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f54b-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5f54b-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f54b-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5f54b-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f54b-117">설명</span><span class="sxs-lookup"><span data-stu-id="5f54b-117">DESCRIPTION</span></span>
<span data-ttu-id="5f54b-118">**New-AzDeployment** cmdlet은 현재 구독 범위에 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="5f54b-119">여기에는 배포에 필요한 리소스가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="5f54b-120">Azure 리소스는 사용자 관리 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="5f54b-121">리소스는 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 머신 또는 Storage 계정과 같은 리소스 그룹에 상주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="5f54b-122">또는 역할 정의, 정책 정의 등의 구독 수준 리소스일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="5f54b-123">리소스 그룹에 리소스를 추가하기 위해 리소스 그룹에 배포를 만드는 **New-AzResourceGroupDeployment를** 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="5f54b-124">**New-AzDeployment** cmdlet은 구독 수준 리소스를 배포하는 현재 구독 범위에서 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="5f54b-125">구독에서 배포를 추가하려면 위치 및 템플릿을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="5f54b-126">위치는 배포 데이터를 저장할 위치를 Azure Resource Manager에 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="5f54b-127">템플릿은 배포할 개별 리소스를 포함하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="5f54b-128">템플릿에는 필수 리소스에 대한 매개 변수 자리 지정자 및 구성 가능한 속성 값(예: 이름 및 크기)이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="5f54b-129">배포에 사용자 지정 템플릿을 사용하 고 *TemplateFile* 매개 변수 또는 TemplateUri 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="5f54b-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5f54b-130">각 템플릿에는 구성 가능한 속성에 대한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5f54b-131">템플릿 매개 변수에 대한 값을 지정하기 위해 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5f54b-132">또는 템플릿을 지정할 때 명령에 동적으로 추가되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5f54b-133">동적 매개 변수를 사용하거나 명령 프롬프트에 입력하거나, 매개 변수를 나타내기 위해 마이너스 기호(-)를 입력하고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5f54b-134">명령 프롬프트에 입력하는 템플릿 매개 변수 값은 템플릿 매개 변수 개체 또는 파일의 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="5f54b-135">예제</span><span class="sxs-lookup"><span data-stu-id="5f54b-135">EXAMPLES</span></span>

### <span data-ttu-id="5f54b-136">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="5f54b-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="5f54b-137">이 명령은 정의된 태그 매개 변수를 사용하여 사용자 지정 템플릿 및 디스크의 템플릿 파일을 사용하여 현재 구독 범위에 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="5f54b-138">이 명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5f54b-139">*TemplateVersion 매개 변수를 사용하여* 템플릿의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="5f54b-140">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="5f54b-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="5f54b-141">이 명령은 사용자 지정 템플릿 및 메모리 내 해시테이블로 변환된 디스크의 템플릿 파일을 사용하여 현재 구독 범위에서 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="5f54b-142">처음 두 명령은 디스크의 템플릿 파일에 대한 텍스트를 읽고 메모리 내 해시테이블로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="5f54b-143">마지막 명령은 *TemplateObject* 매개 변수를 사용하여 이 해시테이블을 지정하고 *TemplateParameterFile* 매개 변수를 사용하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5f54b-144">*TemplateVersion 매개 변수를 사용하여* 템플릿의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="5f54b-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f54b-145">PARAMETERS</span></span>

### <span data-ttu-id="5f54b-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f54b-146">-AsJob</span></span>
<span data-ttu-id="5f54b-147">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5f54b-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f54b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f54b-148">-DefaultProfile</span></span>
<span data-ttu-id="5f54b-149">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f54b-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5f54b-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5f54b-151">배포 디버그 로그 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-151">The deployment debug log level.</span></span>

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

### <span data-ttu-id="5f54b-152">-Location</span><span class="sxs-lookup"><span data-stu-id="5f54b-152">-Location</span></span>
<span data-ttu-id="5f54b-153">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-153">The location to store deployment data.</span></span>

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

### <span data-ttu-id="5f54b-154">-Name</span><span class="sxs-lookup"><span data-stu-id="5f54b-154">-Name</span></span>
<span data-ttu-id="5f54b-155">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="5f54b-156">지정하지 않으면 템플릿 파일이 제공될 때 기본적으로 템플릿 파일 이름이 지정됩니다. 기본적으로 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="5f54b-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="5f54b-157">-Pre</span></span>
<span data-ttu-id="5f54b-158">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5f54b-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="5f54b-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="5f54b-160">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="5f54b-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="5f54b-161">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="5f54b-162">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="5f54b-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f54b-163">-Tag</span></span>
<span data-ttu-id="5f54b-164">배포에 배치할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="5f54b-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5f54b-165">-TemplateFile</span></span>
<span data-ttu-id="5f54b-166">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="5f54b-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="5f54b-167">-TemplateObject</span></span>
<span data-ttu-id="5f54b-168">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="5f54b-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5f54b-169">-TemplateParameterFile</span></span>
<span data-ttu-id="5f54b-170">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="5f54b-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5f54b-171">-TemplateParameterObject</span></span>
<span data-ttu-id="5f54b-172">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="5f54b-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5f54b-173">-TemplateParameterUri</span></span>
<span data-ttu-id="5f54b-174">템플릿 매개 변수 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="5f54b-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5f54b-175">-TemplateUri</span></span>
<span data-ttu-id="5f54b-176">템플릿 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="5f54b-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="5f54b-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="5f54b-178">결과에서 제외할 콤마로 구분된 리소스 변경 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="5f54b-179">-WhatIf 또는 -Confirm 스위치가 설정된 경우 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="5f54b-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="5f54b-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="5f54b-181">결과 What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-181">The What-If result format.</span></span>

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

### <span data-ttu-id="5f54b-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f54b-182">-Confirm</span></span>
<span data-ttu-id="5f54b-183">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f54b-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f54b-184">-WhatIf</span></span>
<span data-ttu-id="5f54b-185">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5f54b-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f54b-186">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f54b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f54b-187">CommonParameters</span></span>
<span data-ttu-id="5f54b-188">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f54b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f54b-189">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5f54b-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f54b-190">입력</span><span class="sxs-lookup"><span data-stu-id="5f54b-190">INPUTS</span></span>

### <span data-ttu-id="5f54b-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f54b-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5f54b-192">System.String</span><span class="sxs-lookup"><span data-stu-id="5f54b-192">System.String</span></span>

## <span data-ttu-id="5f54b-193">출력</span><span class="sxs-lookup"><span data-stu-id="5f54b-193">OUTPUTS</span></span>

### <span data-ttu-id="5f54b-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="5f54b-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5f54b-195">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f54b-195">NOTES</span></span>

## <span data-ttu-id="5f54b-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f54b-196">RELATED LINKS</span></span>
