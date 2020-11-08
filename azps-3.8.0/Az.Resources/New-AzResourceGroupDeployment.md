---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: cf0b8f4897832d84630c98a8518b3c10eefcf5e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043495"
---
# <span data-ttu-id="0592f-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0592f-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="0592f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0592f-102">SYNOPSIS</span></span>
<span data-ttu-id="0592f-103">리소스 그룹에 Azure 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="0592f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0592f-104">SYNTAX</span></span>

### <span data-ttu-id="0592f-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="0592f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0592f-106">By서식 Objectandparameterobject</span><span class="sxs-lookup"><span data-stu-id="0592f-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-107">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="0592f-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-108">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="0592f-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-109">By서식 Objectandparameterfile</span><span class="sxs-lookup"><span data-stu-id="0592f-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-110">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="0592f-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-111">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="0592f-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-112">By서식 Objectandparameteruri</span><span class="sxs-lookup"><span data-stu-id="0592f-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-113">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="0592f-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-114">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="0592f-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592f-115">By서식 Objectwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="0592f-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0592f-116">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="0592f-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0592f-117">설명은</span><span class="sxs-lookup"><span data-stu-id="0592f-117">DESCRIPTION</span></span>
<span data-ttu-id="0592f-118">**새 AzResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="0592f-119">여기에는 배포에 필요한 리소스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="0592f-120">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 컴퓨터 또는 저장소 계정)입니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="0592f-121">Azure 리소스 그룹은 웹 사이트, 데이터베이스 서버, 재무 웹 사이트에 필요한 데이터베이스 등의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="0592f-122">리소스 그룹 배포는 서식 파일을 사용 하 여 리소스 그룹에 리소스를 추가 하 고 Azure에서 사용할 수 있도록 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="0592f-123">서식 파일을 사용 하지 않고 리소스 그룹에 리소스를 추가 하려면 New-AzResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="0592f-124">리소스 그룹 배포를 추가 하려면 기존 리소스 그룹 및 리소스 그룹 서식 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="0592f-125">리소스 그룹 템플릿은 웹 포털 등의 복잡 한 클라우드 기반 서비스에 대 한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="0592f-126">이 템플릿에는 필수 리소스 및 구성 가능한 속성 값 (예: 이름 및 크기)에 대 한 매개 변수 자리 표시 자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="0592f-127">Azure 서식 파일 갤러리에서 여러 서식 파일을 찾을 수도 있고 서식 파일을 직접 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="0592f-128">사용자 지정 서식 파일을 사용 하 여 리소스 그룹을 만들려면 하위 *서식 파일* 매개 변수 또는 하위 *서식 uri* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="0592f-129">각 템플릿에는 구성 가능한 속성에 대 한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="0592f-130">서식 파일 매개 변수에 대 한 값을 지정 하려면 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0592f-131">또는 템플릿을 지정할 때 명령에 동적으로 추가 되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0592f-132">동적 매개 변수를 사용 하려면 명령 프롬프트에 입력 하거나 빼기 기호 (-)를 입력 하 여 매개 변수를 나타내고 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="0592f-133">명령 프롬프트에서 입력 하는 템플릿 매개 변수 값은 template 매개 변수 개체 또는 파일의 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="0592f-134">예제의</span><span class="sxs-lookup"><span data-stu-id="0592f-134">EXAMPLES</span></span>

### <span data-ttu-id="0592f-135">예제 1: 사용자 지정 서식 파일 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="0592f-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="0592f-136">이 명령은 사용자 지정 서식 파일과 디스크의 서식 파일을 사용 하 여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-136">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="0592f-137">이 명령은 template *파일* 매개 변수를 사용 하 여 템플릿과 매개 변수 값이 포함 된 파일을 지정 하는 서식 파일과 템플릿 매개 변수 *파일* 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="0592f-138">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="0592f-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="0592f-139">이 명령은 메모리 내 hashtable로 변환 된 디스크에서 사용자 지정 및 템플릿 파일을 사용 하 여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="0592f-140">처음 두 명령은 디스크의 템플릿 파일에 대 한 텍스트를 읽고이를 메모리 내의 hashtable으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="0592f-141">마지막 명령은 a a i a i a i a i a i a i a a i a i a i a i a i a i a i i a i *매개 변수를* 사용 하 여 *매개 변수*</span><span class="sxs-lookup"><span data-stu-id="0592f-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="0592f-142">변수</span><span class="sxs-lookup"><span data-stu-id="0592f-142">PARAMETERS</span></span>

### <span data-ttu-id="0592f-143">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0592f-143">-ApiVersion</span></span>
<span data-ttu-id="0592f-144">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-144">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0592f-145">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-145">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0592f-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0592f-146">-AsJob</span></span>
<span data-ttu-id="0592f-147">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0592f-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0592f-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0592f-148">-DefaultProfile</span></span>
<span data-ttu-id="0592f-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0592f-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0592f-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="0592f-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="0592f-151">디버그 로그 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-151">Specifies a debug log level.</span></span>
<span data-ttu-id="0592f-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0592f-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="0592f-153">RequestContent</span></span>
- <span data-ttu-id="0592f-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="0592f-154">ResponseContent</span></span>
- <span data-ttu-id="0592f-155">모든</span><span class="sxs-lookup"><span data-stu-id="0592f-155">All</span></span>
- <span data-ttu-id="0592f-156">않아야</span><span class="sxs-lookup"><span data-stu-id="0592f-156">None</span></span>

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

### <span data-ttu-id="0592f-157">-Force</span><span class="sxs-lookup"><span data-stu-id="0592f-157">-Force</span></span>
<span data-ttu-id="0592f-158">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0592f-159">-모드</span><span class="sxs-lookup"><span data-stu-id="0592f-159">-Mode</span></span>
<span data-ttu-id="0592f-160">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-160">Specifies the deployment mode.</span></span> <span data-ttu-id="0592f-161">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0592f-162">완료: 완료 모드에서 리소스 관리자는 리소스 그룹에 존재 하지만 서식 파일에 지정 되지 않은 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="0592f-163">증분: 증분 모드에서 리소스 관리자는 리소스 그룹에는 있지만 서식 파일에 지정 되지 않은 변경 되지 않은 리소스를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="0592f-164">-이름</span><span class="sxs-lookup"><span data-stu-id="0592f-164">-Name</span></span>
<span data-ttu-id="0592f-165">만들려는 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-165">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="0592f-166">-Pre</span><span class="sxs-lookup"><span data-stu-id="0592f-166">-Pre</span></span>
<span data-ttu-id="0592f-167">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-167">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0592f-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0592f-168">-ResourceGroupName</span></span>
<span data-ttu-id="0592f-169">배포할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-169">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="0592f-170">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="0592f-170">-RollBackDeploymentName</span></span>
<span data-ttu-id="0592f-171">-RollbackToLastDeployment가 사용 되는 경우 리소스 그룹에서 지정 된 이름을 사용 하 여 성공한 배포로 롤백할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-171">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="0592f-172">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="0592f-172">-RollbackToLastDeployment</span></span>
<span data-ttu-id="0592f-173">-RollBackDeploymentName가 사용 되는 경우 리소스 그룹에서 마지막으로 성공한 배포에 롤백하는 것으로 표시 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-173">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="0592f-174">-Skip서식 Parameterprompt</span><span class="sxs-lookup"><span data-stu-id="0592f-174">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0592f-175">제공 된 템플릿 매개 변수에 템플릿에서 사용 되는 필요한 모든 매개 변수가 포함 되어 있는지 확인 하는 PowerShell 동적 매개 변수 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-175">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="0592f-176">이 검사는 누락 된 매개 변수에 대해 사용자에 게 값을 제공 하 라는 메시지를 표시 하지만-Skiptemplate Parameterprompt는이 프롬프트를 무시 하 고 매개 변수를 템플릿에 바인딩하지 않은 경우 즉시 오류를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-176">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="0592f-177">비 대화형 스크립트의 경우-Skip비템플릿 Parameterprompt를 제공 하 여 필요한 모든 매개 변수가 충족 되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-177">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0592f-178">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="0592f-178">-TemplateFile</span></span>
<span data-ttu-id="0592f-179">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-179">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="0592f-180">이는 사용자 지정 서식 파일 이거나 **AzResourceGroupGalleryTemplate** cmdlet을 사용 하 여 만든 것과 같은 JSON 파일로 저장 되는 갤러리 서식 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-180">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="0592f-181">-서식 개체</span><span class="sxs-lookup"><span data-stu-id="0592f-181">-TemplateObject</span></span>
<span data-ttu-id="0592f-182">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-182">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0592f-183">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="0592f-183">-TemplateParameterFile</span></span>
<span data-ttu-id="0592f-184">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-184">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="0592f-185">템플릿에 매개 변수가 포함 된 경우에는 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 사용 하 여 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-185">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="0592f-186">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-186">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="0592f-187">동적 매개 변수를 사용 하려면 매개 변수 이름을 나타내는 빼기 기호 (-)를 입력 한 다음 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-187">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="0592f-188">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="0592f-188">-TemplateParameterObject</span></span>
<span data-ttu-id="0592f-189">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-189">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="0592f-190">Windows PowerShell의 해시 테이블에 대 한 도움말을 보려면를 입력 `Get-Help about_Hash_Tables` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-190">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="0592f-191">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-191">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="0592f-192">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-192">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="0592f-193">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="0592f-193">-TemplateParameterUri</span></span>
<span data-ttu-id="0592f-194">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-194">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="0592f-195">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="0592f-195">-TemplateUri</span></span>
<span data-ttu-id="0592f-196">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-196">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="0592f-197">이 파일은 **AzResourceGroupGalleryTemplate** 를 사용 하는 것과 같이 JSON 파일로 저장 되는 사용자 지정 서식 파일 또는 갤러리 서식 파일이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-197">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="0592f-198">-확인</span><span class="sxs-lookup"><span data-stu-id="0592f-198">-Confirm</span></span>
<span data-ttu-id="0592f-199">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0592f-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0592f-200">-WhatIf</span></span>
<span data-ttu-id="0592f-201">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-201">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0592f-202">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0592f-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0592f-203">CommonParameters</span></span>
<span data-ttu-id="0592f-204">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0592f-205">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0592f-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0592f-206">입력</span><span class="sxs-lookup"><span data-stu-id="0592f-206">INPUTS</span></span>

### <span data-ttu-id="0592f-207">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0592f-207">System.String</span></span>

### <span data-ttu-id="0592f-208">DeploymentMode를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0592f-208">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="0592f-209">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0592f-209">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0592f-210">출력</span><span class="sxs-lookup"><span data-stu-id="0592f-210">OUTPUTS</span></span>

### <span data-ttu-id="0592f-211">SdkModels PSResourceGroupDeployment (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0592f-211">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="0592f-212">상속자</span><span class="sxs-lookup"><span data-stu-id="0592f-212">NOTES</span></span>

## <span data-ttu-id="0592f-213">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0592f-213">RELATED LINKS</span></span>

[<span data-ttu-id="0592f-214">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0592f-214">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="0592f-215">새로운 AzResource</span><span class="sxs-lookup"><span data-stu-id="0592f-215">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="0592f-216">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0592f-216">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="0592f-217">제거-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0592f-217">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="0592f-218">중지-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0592f-218">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="0592f-219">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0592f-219">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


