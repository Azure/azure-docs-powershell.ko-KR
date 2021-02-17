---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3e704885c4ce2df0aee2a9b890f768983f93d7bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186401"
---
# <span data-ttu-id="942d8-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="942d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="942d8-102">SYNOPSIS</span></span>
<span data-ttu-id="942d8-103">리소스 그룹에 Azure 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="942d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="942d8-104">SYNTAX</span></span>

### <span data-ttu-id="942d8-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="942d8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942d8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="942d8-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="942d8-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="942d8-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="942d8-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="942d8-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="942d8-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="942d8-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="942d8-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="942d8-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="942d8-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="942d8-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="942d8-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="942d8-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942d8-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="942d8-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942d8-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="942d8-119">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="942d8-120">설명</span><span class="sxs-lookup"><span data-stu-id="942d8-120">DESCRIPTION</span></span>
<span data-ttu-id="942d8-121">**New-AzResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-121">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="942d8-122">여기에는 배포에 필요한 리소스가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-122">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="942d8-123">Azure 리소스는 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 머신 또는 Storage 계정과 같은 사용자 관리 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-123">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="942d8-124">Azure 리소스 그룹은 웹 사이트, 데이터베이스 서버 및 금융 웹 사이트에 필요한 데이터베이스와 같은 단위로 배포되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-124">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="942d8-125">리소스 그룹 배포는 템플릿을 사용하여 리소스 그룹에 리소스를 추가하고 Azure에서 사용할 수 있도록 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-125">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="942d8-126">템플릿을 사용하지 않고 리소스 그룹에 리소스를 추가하기 위해 New-AzResource cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-126">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="942d8-127">리소스 그룹 배포를 추가하기 위해 기존 리소스 그룹 및 리소스 그룹 템플릿의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-127">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="942d8-128">리소스 그룹 템플릿은 웹 포털과 같은 복잡한 클라우드 기반 서비스에 대한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-128">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="942d8-129">템플릿에는 필수 리소스에 대한 매개 변수 자리 지정자 및 구성 가능한 속성 값(예: 이름 및 크기)이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-129">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="942d8-130">Azure 템플릿 갤러리에서 많은 템플릿을 찾거나 사용자 자신의 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-130">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="942d8-131">사용자 지정 템플릿을 사용하여 리소스 그룹을 만들 경우 *TemplateFile* 매개 변수 또는 TemplateUri 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="942d8-131">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="942d8-132">각 템플릿에는 구성 가능한 속성에 대한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-132">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="942d8-133">템플릿 매개 변수에 대한 값을 지정하기 위해 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-133">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="942d8-134">또는 템플릿을 지정할 때 명령에 동적으로 추가되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-134">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="942d8-135">동적 매개 변수를 사용 설정하기 위해 명령 프롬프트에 입력하거나, 매개 변수를 나타내기 위해 마이너스 기호(-)를 입력하고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-135">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="942d8-136">명령 프롬프트에 입력하는 템플릿 매개 변수 값은 템플릿 매개 변수 개체 또는 파일의 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-136">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="942d8-137">예제</span><span class="sxs-lookup"><span data-stu-id="942d8-137">EXAMPLES</span></span>

### <span data-ttu-id="942d8-138">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="942d8-138">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="942d8-139">이 명령은 정의된 태그 매개 변수를 사용하여 디스크에 사용자 지정 템플릿 및 템플릿 파일을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-139">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="942d8-140">이 명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-140">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="942d8-141">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="942d8-141">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="942d8-142">이 명령은 메모리 내 해시테이블로 변환된 디스크의 사용자 지정 및 템플릿 파일을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-142">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="942d8-143">처음 두 명령은 디스크의 템플릿 파일에 대한 텍스트를 읽고 메모리 내 해시테이블로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-143">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="942d8-144">마지막 명령은 *TemplateObject* 매개 변수를 사용하여 해시테이블 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-144">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="942d8-145">예제 3</span><span class="sxs-lookup"><span data-stu-id="942d8-145">Example 3</span></span>

<span data-ttu-id="942d8-146">리소스 그룹에 Azure 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-146">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="942d8-147">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="942d8-147">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="942d8-148">예제 4: URI 및 SAS 토큰을 사용하여 비 공용 저장소 계정에 저장된 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="942d8-148">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="942d8-149">이 명령은 Public이 아니며 QueryString 매개 변수를 사용하여 제공되는 액세스하려면 토큰 매개 변수가 필요한 TemplateUri의 템플릿을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-149">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="942d8-150">이 명령을 실행하면 URL을 사용하여 템플릿에 효과적으로 https://example.com/example.json?foo 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-150">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="942d8-151">SAS 토큰을 QueryString으로 제공하여 저장소 계정에서 템플릿을 사용하려는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-151">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>
## <span data-ttu-id="942d8-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="942d8-152">PARAMETERS</span></span>

### <span data-ttu-id="942d8-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="942d8-153">-AsJob</span></span>
<span data-ttu-id="942d8-154">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="942d8-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="942d8-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942d8-155">-DefaultProfile</span></span>
<span data-ttu-id="942d8-156">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="942d8-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="942d8-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="942d8-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="942d8-158">디버그 로그 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-158">Specifies a debug log level.</span></span>
<span data-ttu-id="942d8-159">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="942d8-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="942d8-160">RequestContent</span><span class="sxs-lookup"><span data-stu-id="942d8-160">RequestContent</span></span>
- <span data-ttu-id="942d8-161">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="942d8-161">ResponseContent</span></span>
- <span data-ttu-id="942d8-162">모두</span><span class="sxs-lookup"><span data-stu-id="942d8-162">All</span></span>
- <span data-ttu-id="942d8-163">없음</span><span class="sxs-lookup"><span data-stu-id="942d8-163">None</span></span>

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

### <span data-ttu-id="942d8-164">-Force</span><span class="sxs-lookup"><span data-stu-id="942d8-164">-Force</span></span>
<span data-ttu-id="942d8-165">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-165">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="942d8-166">-Mode</span><span class="sxs-lookup"><span data-stu-id="942d8-166">-Mode</span></span>
<span data-ttu-id="942d8-167">배포 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-167">Specifies the deployment mode.</span></span> <span data-ttu-id="942d8-168">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="942d8-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="942d8-169">완료: 전체 모드에서 Resource Manager는 리소스 그룹에 있지만 템플릿에 지정되지 않은 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-169">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="942d8-170">증분: 증분 모드에서 Resource Manager는 리소스 그룹에 존재하지만 템플릿에 지정되지 않은 변경되지 않은 리소스를 그대로 갑니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-170">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="942d8-171">-Name</span><span class="sxs-lookup"><span data-stu-id="942d8-171">-Name</span></span>
<span data-ttu-id="942d8-172">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-172">The name of the deployment it's going to create.</span></span> <span data-ttu-id="942d8-173">지정하지 않으면 템플릿 파일이 제공될 때 기본적으로 템플릿 파일 이름이 지정됩니다. 기본적으로 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-173">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="942d8-174">-Pre</span><span class="sxs-lookup"><span data-stu-id="942d8-174">-Pre</span></span>
<span data-ttu-id="942d8-175">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-175">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="942d8-176">-QueryString</span><span class="sxs-lookup"><span data-stu-id="942d8-176">-QueryString</span></span>
<span data-ttu-id="942d8-177">TemplateUri 매개 변수와 함께 사용할 쿼리 문자열(예: SAS 토큰)입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-177">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="942d8-178">연결된 템플릿의 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-178">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="942d8-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942d8-179">-ResourceGroupName</span></span>
<span data-ttu-id="942d8-180">배포할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-180">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="942d8-181">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="942d8-181">-RollBackDeploymentName</span></span>
<span data-ttu-id="942d8-182">-RollbackToLastDeployment를 사용하는 경우 리소스 그룹에서 지정한 이름을 사용하여 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-182">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="942d8-183">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-183">-RollbackToLastDeployment</span></span>
<span data-ttu-id="942d8-184">-RollBackDeploymentName을 사용하는 경우 리소스 그룹에서 마지막으로 성공한 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-184">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="942d8-185">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="942d8-185">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="942d8-186">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="942d8-186">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="942d8-187">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 이 프롬프트가 무시되고 템플릿에 매개 변수가 바인딩되지 않은 경우 즉시 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-187">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="942d8-188">비대화형 스크립트의 경우 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하기 위해 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-188">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="942d8-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="942d8-189">-Tag</span></span>
<span data-ttu-id="942d8-190">배포에 배치할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-190">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="942d8-191">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="942d8-191">-TemplateFile</span></span>
<span data-ttu-id="942d8-192">JSON 템플릿 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-192">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="942d8-193">**Save-AzResourceGroupGalleryTemplate** cmdlet을 사용하여 만든 템플릿과 같이 JSON 파일로 저장된 사용자 지정 템플릿 또는 갤러리 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-193">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="942d8-194">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="942d8-194">-TemplateObject</span></span>
<span data-ttu-id="942d8-195">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-195">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="942d8-196">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="942d8-196">-TemplateParameterFile</span></span>
<span data-ttu-id="942d8-197">템플릿 매개 변수의 이름 및 값을 포함하는 JSON 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-197">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="942d8-198">템플릿에 매개 변수가 있는 경우 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 사용하여 매개 변수 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-198">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="942d8-199">템플릿 매개 변수는 템플릿을 지정할 때 명령에 동적으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-199">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="942d8-200">동적 매개 변수를 사용 설정하기 위해 매개 변수 이름을 나타내기 위해 마이너스 기호(-)를 입력한 다음 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-200">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="942d8-201">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="942d8-201">-TemplateParameterObject</span></span>
<span data-ttu-id="942d8-202">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-202">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="942d8-203">다음에서 해시 테이블에 대한 도움말을 `Get-Help about_Hash_Tables` Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="942d8-203">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="942d8-204">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-204">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="942d8-205">템플릿 매개 변수는 템플릿을 지정할 때 명령에 동적으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-205">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="942d8-206">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="942d8-206">-TemplateParameterUri</span></span>
<span data-ttu-id="942d8-207">템플릿 매개 변수 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-207">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="942d8-208">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="942d8-208">-TemplateSpecId</span></span>
<span data-ttu-id="942d8-209">배포할 templateSpec의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-209">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="942d8-210">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="942d8-210">-TemplateUri</span></span>
<span data-ttu-id="942d8-211">JSON 템플릿 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-211">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="942d8-212">이 파일은 **Save-AzResourceGroupGalleryTemplate을** 사용하는 경우와 같이 JSON 파일로 저장된 사용자 지정 템플릿 또는 갤러리 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-212">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="942d8-213">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="942d8-213">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="942d8-214">결과에서 제외할 콤마로 구분된 리소스 변경 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-214">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="942d8-215">-WhatIf 또는 -Confirm 스위치가 설정된 경우 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-215">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="942d8-216">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="942d8-216">-WhatIfResultFormat</span></span>
<span data-ttu-id="942d8-217">결과 What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-217">The What-If result format.</span></span>

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

### <span data-ttu-id="942d8-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="942d8-218">-Confirm</span></span>
<span data-ttu-id="942d8-219">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942d8-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942d8-220">-WhatIf</span></span>
<span data-ttu-id="942d8-221">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="942d8-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="942d8-222">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942d8-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942d8-223">CommonParameters</span></span>
<span data-ttu-id="942d8-224">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="942d8-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942d8-225">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="942d8-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942d8-226">입력</span><span class="sxs-lookup"><span data-stu-id="942d8-226">INPUTS</span></span>

### <span data-ttu-id="942d8-227">System.String</span><span class="sxs-lookup"><span data-stu-id="942d8-227">System.String</span></span>

### <span data-ttu-id="942d8-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="942d8-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="942d8-229">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="942d8-229">System.Collections.Hashtable</span></span>

## <span data-ttu-id="942d8-230">출력</span><span class="sxs-lookup"><span data-stu-id="942d8-230">OUTPUTS</span></span>

### <span data-ttu-id="942d8-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="942d8-232">참고 사항</span><span class="sxs-lookup"><span data-stu-id="942d8-232">NOTES</span></span>

## <span data-ttu-id="942d8-233">관련 링크</span><span class="sxs-lookup"><span data-stu-id="942d8-233">RELATED LINKS</span></span>

[<span data-ttu-id="942d8-234">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-234">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="942d8-235">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="942d8-235">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="942d8-236">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="942d8-236">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="942d8-237">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-237">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="942d8-238">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-238">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="942d8-239">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="942d8-239">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)