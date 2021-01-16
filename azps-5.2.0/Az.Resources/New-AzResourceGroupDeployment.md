---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344061"
---
# <span data-ttu-id="a1fe0-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a1fe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fe0-103">리소스 그룹에 Azure 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="a1fe0-104">구문</span><span class="sxs-lookup"><span data-stu-id="a1fe0-104">SYNTAX</span></span>

### <span data-ttu-id="a1fe0-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="a1fe0-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1fe0-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1fe0-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1fe0-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1fe0-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1fe0-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1fe0-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1fe0-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1fe0-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1fe0-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a1fe0-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1fe0-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a1fe0-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1fe0-117">설명</span><span class="sxs-lookup"><span data-stu-id="a1fe0-117">DESCRIPTION</span></span>
<span data-ttu-id="a1fe0-118">**New-AzResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="a1fe0-119">여기에는 배포에 필요한 리소스가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="a1fe0-120">Azure 리소스는 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 머신 또는 Storage 계정과 같은 사용자 관리 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="a1fe0-121">Azure 리소스 그룹은 웹 사이트, 데이터베이스 서버 및 금융 웹 사이트에 필요한 데이터베이스와 같은 단위로 배포되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="a1fe0-122">리소스 그룹 배포는 템플릿을 사용하여 리소스 그룹에 리소스를 추가하고 Azure에서 사용할 수 있도록 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="a1fe0-123">템플릿을 사용하지 않고 리소스 그룹에 리소스를 추가하기 위해 New-AzResource cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="a1fe0-124">리소스 그룹 배포를 추가하기 위해 기존 리소스 그룹 및 리소스 그룹 템플릿의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="a1fe0-125">리소스 그룹 템플릿은 웹 포털과 같은 복잡한 클라우드 기반 서비스에 대한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="a1fe0-126">템플릿에는 필수 리소스에 대한 매개 변수 자리 지정자 및 구성 가능한 속성 값(예: 이름 및 크기)이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="a1fe0-127">Azure 템플릿 갤러리에서 많은 템플릿을 찾거나 사용자 자신의 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="a1fe0-128">사용자 지정 템플릿을 사용하여 리소스 그룹을 만들 경우 *TemplateFile* 매개 변수 또는 TemplateUri 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="a1fe0-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="a1fe0-129">각 템플릿에는 구성 가능한 속성에 대한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="a1fe0-130">템플릿 매개 변수에 대한 값을 지정하기 위해 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a1fe0-131">또는 템플릿을 지정할 때 명령에 동적으로 추가되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a1fe0-132">동적 매개 변수를 사용하거나 명령 프롬프트에 입력하거나, 매개 변수를 나타내기 위해 마이너스 기호(-)를 입력하고 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="a1fe0-133">명령 프롬프트에 입력하는 템플릿 매개 변수 값은 템플릿 매개 변수 개체 또는 파일의 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="a1fe0-134">예제</span><span class="sxs-lookup"><span data-stu-id="a1fe0-134">EXAMPLES</span></span>

### <span data-ttu-id="a1fe0-135">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="a1fe0-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="a1fe0-136">이 명령은 정의된 태그 매개 변수를 사용하여 디스크에 사용자 지정 템플릿 및 템플릿 파일을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="a1fe0-137">이 명령은 *TemplateFile* 매개 변수를 사용하여 템플릿 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a1fe0-138">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="a1fe0-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="a1fe0-139">이 명령은 메모리 내 해시테이블로 변환된 디스크의 사용자 지정 및 템플릿 파일을 사용하여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="a1fe0-140">처음 두 명령은 디스크의 템플릿 파일에 대한 텍스트를 읽고 메모리 내 해시테이블로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="a1fe0-141">마지막 명령은 *TemplateObject* 매개 변수를 사용하여 해시테이블 및 *TemplateParameterFile* 매개 변수를 지정하여 매개 변수 및 매개 변수 값을 포함하는 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a1fe0-142">예제 3</span><span class="sxs-lookup"><span data-stu-id="a1fe0-142">Example 3</span></span>

<span data-ttu-id="a1fe0-143">리소스 그룹에 Azure 배포를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="a1fe0-144">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="a1fe0-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="a1fe0-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1fe0-145">PARAMETERS</span></span>

### <span data-ttu-id="a1fe0-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1fe0-146">-AsJob</span></span>
<span data-ttu-id="a1fe0-147">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a1fe0-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1fe0-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fe0-148">-DefaultProfile</span></span>
<span data-ttu-id="a1fe0-149">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a1fe0-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1fe0-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="a1fe0-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="a1fe0-151">디버그 로그 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-151">Specifies a debug log level.</span></span>
<span data-ttu-id="a1fe0-152">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a1fe0-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1fe0-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="a1fe0-153">RequestContent</span></span>
- <span data-ttu-id="a1fe0-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="a1fe0-154">ResponseContent</span></span>
- <span data-ttu-id="a1fe0-155">모두</span><span class="sxs-lookup"><span data-stu-id="a1fe0-155">All</span></span>
- <span data-ttu-id="a1fe0-156">없음</span><span class="sxs-lookup"><span data-stu-id="a1fe0-156">None</span></span>

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

### <span data-ttu-id="a1fe0-157">-Force</span><span class="sxs-lookup"><span data-stu-id="a1fe0-157">-Force</span></span>
<span data-ttu-id="a1fe0-158">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1fe0-159">-Mode</span><span class="sxs-lookup"><span data-stu-id="a1fe0-159">-Mode</span></span>
<span data-ttu-id="a1fe0-160">배포 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-160">Specifies the deployment mode.</span></span> <span data-ttu-id="a1fe0-161">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a1fe0-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1fe0-162">완료: 전체 모드에서 Resource Manager는 리소스 그룹에 있지만 템플릿에 지정되지 않은 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="a1fe0-163">증분: 증분 모드에서 Resource Manager는 리소스 그룹에 존재하지만 템플릿에 지정되지 않은 변경되지 않은 리소스를 그대로 갑니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="a1fe0-164">-Name</span><span class="sxs-lookup"><span data-stu-id="a1fe0-164">-Name</span></span>
<span data-ttu-id="a1fe0-165">만들 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="a1fe0-166">지정하지 않으면 템플릿 파일이 제공될 때 기본적으로 템플릿 파일 이름이 지정됩니다. 기본적으로 템플릿 개체가 제공되는 현재 시간(예: "20131223140835")입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="a1fe0-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="a1fe0-167">-Pre</span></span>
<span data-ttu-id="a1fe0-168">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1fe0-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1fe0-169">-ResourceGroupName</span></span>
<span data-ttu-id="a1fe0-170">배포할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="a1fe0-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a1fe0-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="a1fe0-172">-RollbackToLastDeployment를 사용하는 경우 리소스 그룹에서 지정한 이름을 사용하여 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="a1fe0-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="a1fe0-174">-RollBackDeploymentName을 사용하는 경우 리소스 그룹에서 마지막으로 성공한 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="a1fe0-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a1fe0-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a1fe0-176">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="a1fe0-177">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="a1fe0-178">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a1fe0-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1fe0-179">-Tag</span></span>
<span data-ttu-id="a1fe0-180">배포에 배치할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="a1fe0-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a1fe0-181">-TemplateFile</span></span>
<span data-ttu-id="a1fe0-182">JSON 템플릿 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="a1fe0-183">**Save-AzResourceGroupGalleryTemplate** cmdlet을 사용하여 만든 템플릿과 같이 JSON 파일로 저장된 사용자 지정 템플릿 또는 갤러리 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="a1fe0-184">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a1fe0-184">-TemplateObject</span></span>
<span data-ttu-id="a1fe0-185">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a1fe0-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a1fe0-186">-TemplateParameterFile</span></span>
<span data-ttu-id="a1fe0-187">템플릿 매개 변수의 이름 및 값을 포함하는 JSON 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="a1fe0-188">템플릿에 매개 변수가 있는 경우 *TemplateParameterFile* 매개 변수 또는 *TemplateParameterObject* 매개 변수를 사용하여 매개 변수 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a1fe0-189">템플릿 매개 변수는 템플릿을 지정할 때 명령에 동적으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a1fe0-190">동적 매개 변수를 사용 설정하기 위해 매개 변수 이름을 나타내기 위해 마이너스 기호(-)를 입력한 다음 Tab 키를 사용하여 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="a1fe0-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a1fe0-191">-TemplateParameterObject</span></span>
<span data-ttu-id="a1fe0-192">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="a1fe0-193">다음에서 해시 테이블에 대한 도움말을 `Get-Help about_Hash_Tables` Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a1fe0-194">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="a1fe0-195">템플릿 매개 변수는 템플릿을 지정할 때 명령에 동적으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="a1fe0-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a1fe0-196">-TemplateParameterUri</span></span>
<span data-ttu-id="a1fe0-197">템플릿 매개 변수 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a1fe0-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a1fe0-198">-TemplateUri</span></span>
<span data-ttu-id="a1fe0-199">JSON 템플릿 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="a1fe0-200">이 파일은 **Save-AzResourceGroupGalleryTemplate을** 사용하는 경우와 같이 JSON 파일로 저장된 사용자 지정 템플릿 또는 갤러리 템플릿일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="a1fe0-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="a1fe0-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="a1fe0-202">결과에서 제외할 콤마로 구분된 리소스 변경 What-If 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="a1fe0-203">-WhatIf 또는 -Confirm 스위치가 설정된 경우 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="a1fe0-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="a1fe0-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="a1fe0-205">결과 What-If 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-205">The What-If result format.</span></span>

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

### <span data-ttu-id="a1fe0-206">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1fe0-206">-Confirm</span></span>
<span data-ttu-id="a1fe0-207">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1fe0-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1fe0-208">-WhatIf</span></span>
<span data-ttu-id="a1fe0-209">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a1fe0-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1fe0-210">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1fe0-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fe0-211">CommonParameters</span></span>
<span data-ttu-id="a1fe0-212">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fe0-213">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1fe0-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fe0-214">입력</span><span class="sxs-lookup"><span data-stu-id="a1fe0-214">INPUTS</span></span>

### <span data-ttu-id="a1fe0-215">System.String</span><span class="sxs-lookup"><span data-stu-id="a1fe0-215">System.String</span></span>

### <span data-ttu-id="a1fe0-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a1fe0-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a1fe0-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1fe0-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a1fe0-218">출력</span><span class="sxs-lookup"><span data-stu-id="a1fe0-218">OUTPUTS</span></span>

### <span data-ttu-id="a1fe0-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a1fe0-220">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a1fe0-220">NOTES</span></span>

## <span data-ttu-id="a1fe0-221">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1fe0-221">RELATED LINKS</span></span>

[<span data-ttu-id="a1fe0-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a1fe0-223">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a1fe0-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="a1fe0-224">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1fe0-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a1fe0-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a1fe0-226">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a1fe0-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a1fe0-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)