---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3403900fafae1615f8253b4d5671e497a1d507f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978155"
---
# <span data-ttu-id="75ee5-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="75ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="75ee5-103">리소스 그룹에 Azure 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="75ee5-104">구문</span><span class="sxs-lookup"><span data-stu-id="75ee5-104">SYNTAX</span></span>

### <span data-ttu-id="75ee5-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="75ee5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ee5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ee5-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ee5-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ee5-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="75ee5-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ee5-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ee5-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ee5-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="75ee5-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ee5-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ee5-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ee5-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="75ee5-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ee5-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="75ee5-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ee5-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="75ee5-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ee5-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="75ee5-120">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ee5-121">설명</span><span class="sxs-lookup"><span data-stu-id="75ee5-121">DESCRIPTION</span></span>
<span data-ttu-id="75ee5-122">**New-AzResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-122">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="75ee5-123">여기에는 배포에 필요한 리소스가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-123">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="75ee5-124">Azure 리소스는 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 머신 또는 Storage 계정과 같은 사용자 관리 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-124">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="75ee5-125">Azure 리소스 그룹은 금융 웹 사이트에 필요한 웹 사이트, 데이터베이스 서버 및 데이터베이스와 같은 단위로 배포되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-125">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="75ee5-126">리소스 그룹 배포는 템플릿을 사용하여 리소스 그룹에 리소스를 추가하고 Azure에서 사용할 수 있도록 해당 리소스를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-126">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="75ee5-127">템플릿을 사용하지 않고 리소스 그룹에 리소스를 추가하기 위해 New-AzResource cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-127">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="75ee5-128">리소스 그룹 배포를 추가하기 위해 기존 리소스 그룹 이름 및 리소스 그룹 템플릿을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-128">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="75ee5-129">리소스 그룹 템플릿은 웹 포털과 같은 복잡한 클라우드 기반 서비스에 대한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-129">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="75ee5-130">템플릿에는 필수 리소스 및 구성 가능한 속성 값(예: 이름 및 크기)에 대한 매개 변수 자리 를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-130">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="75ee5-131">Azure 템플릿 갤러리에서 많은 템플릿을 찾을 수 있습니다. 또는 사용자만의 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-131">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="75ee5-132">사용자 지정 템플릿을 사용하여 리소스 그룹을 만들 경우 *TemplateFile* 매개 변수 또는 TemplateUri 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="75ee5-132">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="75ee5-133">각 템플릿에는 구성 가능한 속성에 대한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="75ee5-134">템플릿 매개 변수에 대한 값을 지정하기 위해 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="75ee5-135">또는 템플릿을 지정할 때 명령에 동적으로 추가되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="75ee5-136">동적 매개 변수를 사용하거나 명령 프롬프트에 입력하거나 마이너스 기호(-)를 입력하여 매개 변수를 나타내고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="75ee5-137">명령 프롬프트에 입력하는 템플릿 매개 변수 값은 템플릿 매개 변수 개체 또는 파일의 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="75ee5-138">예제</span><span class="sxs-lookup"><span data-stu-id="75ee5-138">EXAMPLES</span></span>

### <span data-ttu-id="75ee5-139">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="75ee5-140">이 명령은 정의된 태그 매개 변수를 사용하여 디스크에 사용자 지정 템플릿 및 템플릿 파일을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-140">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="75ee5-141">명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="75ee5-142">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-142">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="75ee5-143">이 명령은 메모리 내 해시테이블로 변환된 디스크의 사용자 지정 및 템플릿 파일을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-143">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="75ee5-144">처음 두 명령은 디스크의 템플릿 파일에 대한 텍스트를 읽고 메모리 내 해시테이블로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-144">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="75ee5-145">마지막 명령은 *TemplateObject* 매개 변수를 사용하여 해시테이블 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-145">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="75ee5-146">예제 3</span><span class="sxs-lookup"><span data-stu-id="75ee5-146">Example 3</span></span>

<span data-ttu-id="75ee5-147">리소스 그룹에 Azure 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-147">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="75ee5-148">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="75ee5-148">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="75ee5-149">예제 4: uri 및 SAS 토큰을 사용하여 공용 저장소가 아닌 계정에 저장된 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="75ee5-149">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="75ee5-150">이 명령은 공용이 아니며 QueryString 매개 변수를 사용하여 제공되는 액세스하려면 토큰 매개 변수가 필요한 TemplateUri의 템플릿을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-150">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="75ee5-151">이 명령을 실행하면 URL을 사용하여 템플릿에 효과적으로 https://example.com/example.json?foo 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-151">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="75ee5-152">SAS 토큰을 QueryString으로 제공하여 저장소 계정에서 템플릿을 사용하려는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-152">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

## <span data-ttu-id="75ee5-153">매개 변수</span><span class="sxs-lookup"><span data-stu-id="75ee5-153">PARAMETERS</span></span>

### <span data-ttu-id="75ee5-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75ee5-154">-AsJob</span></span>
<span data-ttu-id="75ee5-155">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="75ee5-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75ee5-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ee5-156">-DefaultProfile</span></span>
<span data-ttu-id="75ee5-157">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="75ee5-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75ee5-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="75ee5-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="75ee5-159">디버그 로그 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-159">Specifies a debug log level.</span></span>
<span data-ttu-id="75ee5-160">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75ee5-161">RequestContent</span><span class="sxs-lookup"><span data-stu-id="75ee5-161">RequestContent</span></span>
- <span data-ttu-id="75ee5-162">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="75ee5-162">ResponseContent</span></span>
- <span data-ttu-id="75ee5-163">모두</span><span class="sxs-lookup"><span data-stu-id="75ee5-163">All</span></span>
- <span data-ttu-id="75ee5-164">없음</span><span class="sxs-lookup"><span data-stu-id="75ee5-164">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ee5-165">-Force</span><span class="sxs-lookup"><span data-stu-id="75ee5-165">-Force</span></span>
<span data-ttu-id="75ee5-166">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-166">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75ee5-167">-Mode</span><span class="sxs-lookup"><span data-stu-id="75ee5-167">-Mode</span></span>
<span data-ttu-id="75ee5-168">배포 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-168">Specifies the deployment mode.</span></span> <span data-ttu-id="75ee5-169">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-169">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75ee5-170">완료: 완료 모드에서 Resource Manager는 리소스 그룹에 있지만 템플릿에 지정되지 않은 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-170">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="75ee5-171">증분: 증분 모드에서 Resource Manager는 리소스 그룹에 존재하지만 템플릿에 지정되지 않은 변경되지 않은 리소스를 그대로 떠 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-171">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ee5-172">-Name</span><span class="sxs-lookup"><span data-stu-id="75ee5-172">-Name</span></span>
<span data-ttu-id="75ee5-173">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-173">The name of the deployment it's going to create.</span></span> <span data-ttu-id="75ee5-174">지정하지 않으면 템플릿 파일이 제공될 때 템플릿 파일 이름을 기본값으로 지정합니다. 기본값은 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-174">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="75ee5-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="75ee5-175">-Pre</span></span>
<span data-ttu-id="75ee5-176">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="75ee5-177">-QueryString</span><span class="sxs-lookup"><span data-stu-id="75ee5-177">-QueryString</span></span>
<span data-ttu-id="75ee5-178">TemplateUri 매개 변수와 함께 사용할 쿼리 문자열(예: SAS 토큰)입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-178">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="75ee5-179">연결된 템플릿의 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-179">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="75ee5-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ee5-180">-ResourceGroupName</span></span>
<span data-ttu-id="75ee5-181">배포할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-181">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="75ee5-182">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="75ee5-182">-RollBackDeploymentName</span></span>
<span data-ttu-id="75ee5-183">-RollbackToLastDeployment를 사용하는 경우 리소스 그룹에서 지정한 이름으로 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-183">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ee5-184">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-184">-RollbackToLastDeployment</span></span>
<span data-ttu-id="75ee5-185">-RollBackDeploymentName을 사용하는 경우 리소스 그룹의 마지막 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-185">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="75ee5-186">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="75ee5-186">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="75ee5-187">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필요한 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="75ee5-187">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="75ee5-188">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 경우 즉시 이 프롬프트와 오류를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-188">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="75ee5-189">대화형이 아닌 스크립트의 경우 -SkipTemplateParameterPrompt를 제공하여 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-189">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="75ee5-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="75ee5-190">-Tag</span></span>
<span data-ttu-id="75ee5-191">배포에 넣을 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-191">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="75ee5-192">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="75ee5-192">-TemplateFile</span></span>
<span data-ttu-id="75ee5-193">템플릿 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-193">Specifies the full path of a template file.</span></span> <span data-ttu-id="75ee5-194">지원되는 템플릿 파일 형식: json 및 bicep입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-194">Supported template file type: json and bicep.</span></span>
<span data-ttu-id="75ee5-195">**Save-AzResourceGroupGalleryTemplate** cmdlet을 사용하여 만든 파일과 같이 JSON 파일로 저장되는 사용자 지정 템플릿 또는 갤러리 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-195">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="75ee5-196">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="75ee5-196">-TemplateObject</span></span>
<span data-ttu-id="75ee5-197">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-197">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="75ee5-198">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ee5-198">-TemplateParameterFile</span></span>
<span data-ttu-id="75ee5-199">템플릿 매개 변수의 이름과 값을 포함하는 JSON 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-199">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="75ee5-200">템플릿에 매개 변수가 있는 경우 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 사용하여 매개 변수 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-200">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="75ee5-201">템플릿을 지정할 때 템플릿 매개 변수가 명령에 동적으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-201">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="75ee5-202">동적 매개 변수를 사용하게 하여 마이너스 기호(-)를 입력하여 매개 변수 이름을 나타내고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-202">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="75ee5-203">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ee5-203">-TemplateParameterObject</span></span>
<span data-ttu-id="75ee5-204">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-204">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="75ee5-205">에서 해시 테이블에 대한 도움말을 Windows PowerShell `Get-Help about_Hash_Tables` 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-205">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="75ee5-206">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-206">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="75ee5-207">템플릿을 지정할 때 템플릿 매개 변수가 명령에 동적으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-207">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="75ee5-208">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ee5-208">-TemplateParameterUri</span></span>
<span data-ttu-id="75ee5-209">템플릿 매개 변수 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-209">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="75ee5-210">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="75ee5-210">-TemplateSpecId</span></span>
<span data-ttu-id="75ee5-211">배포할 템플릿Spec의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-211">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="75ee5-212">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="75ee5-212">-TemplateUri</span></span>
<span data-ttu-id="75ee5-213">템플릿 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-213">Specifies the URI of a template file.</span></span>
<span data-ttu-id="75ee5-214">이 파일은 **Save-AzResourceGroupGalleryTemplate를** 사용하여 JSON 파일로 저장되는 사용자 지정 템플릿 또는 갤러리 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-214">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="75ee5-215">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="75ee5-215">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="75ee5-216">결과에서 제외할 콤마로 구분된 리소스 변경 형식을 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-216">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="75ee5-217">-WhatIf 또는 -Confirm 스위치가 설정된 경우 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-217">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="75ee5-218">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="75ee5-218">-WhatIfResultFormat</span></span>
<span data-ttu-id="75ee5-219">What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-219">The What-If result format.</span></span>

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

### <span data-ttu-id="75ee5-220">-확인</span><span class="sxs-lookup"><span data-stu-id="75ee5-220">-Confirm</span></span>
<span data-ttu-id="75ee5-221">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-221">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ee5-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ee5-222">-WhatIf</span></span>
<span data-ttu-id="75ee5-223">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ee5-224">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-224">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ee5-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ee5-225">CommonParameters</span></span>
<span data-ttu-id="75ee5-226">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75ee5-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ee5-227">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75ee5-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ee5-228">입력</span><span class="sxs-lookup"><span data-stu-id="75ee5-228">INPUTS</span></span>

### <span data-ttu-id="75ee5-229">System.String</span><span class="sxs-lookup"><span data-stu-id="75ee5-229">System.String</span></span>

### <span data-ttu-id="75ee5-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="75ee5-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="75ee5-231">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="75ee5-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="75ee5-232">출력</span><span class="sxs-lookup"><span data-stu-id="75ee5-232">OUTPUTS</span></span>

### <span data-ttu-id="75ee5-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="75ee5-234">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75ee5-234">NOTES</span></span>

## <span data-ttu-id="75ee5-235">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75ee5-235">RELATED LINKS</span></span>

[<span data-ttu-id="75ee5-236">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-236">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="75ee5-237">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="75ee5-237">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="75ee5-238">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75ee5-238">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="75ee5-239">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-239">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="75ee5-240">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-240">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="75ee5-241">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75ee5-241">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)