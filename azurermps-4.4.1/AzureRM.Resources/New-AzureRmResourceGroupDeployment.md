---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532975"
---
# <span data-ttu-id="da51a-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da51a-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="da51a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da51a-102">SYNOPSIS</span></span>
<span data-ttu-id="da51a-103">리소스 그룹에 Azure 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da51a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da51a-104">SYNTAX</span></span>

### <span data-ttu-id="da51a-105">매개 변수 없이 서식 파일을 통한 배포 (기본값)</span><span class="sxs-lookup"><span data-stu-id="da51a-105">Deployment via template file without parameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da51a-106">서식 파일 및 템플릿 매개 변수 개체를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-106">Deployment via template file and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da51a-107">템플릿 uri 및 템플릿 매개 변수 개체를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-107">Deployment via template uri and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da51a-108">서식 파일 및 템플릿 매개 변수 파일을 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-108">Deployment via template file and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da51a-109">템플릿 uri 및 템플릿 매개 변수 파일을 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-109">Deployment via template uri and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da51a-110">템플릿 파일 템플릿 매개 변수 uri를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-110">Deployment via template file template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da51a-111">템플릿 uri 및 템플릿 매개 변수 uri를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-111">Deployment via template uri and template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da51a-112">매개 변수 없이 템플릿 uri를 통한 배포</span><span class="sxs-lookup"><span data-stu-id="da51a-112">Deployment via template uri without parameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da51a-113">설명은</span><span class="sxs-lookup"><span data-stu-id="da51a-113">DESCRIPTION</span></span>
<span data-ttu-id="da51a-114">**새 AzureRmResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="da51a-115">여기에는 배포에 필요한 리소스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="da51a-116">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 컴퓨터 또는 저장소 계정)입니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="da51a-117">Azure 리소스 그룹은 웹 사이트, 데이터베이스 서버, 재무 웹 사이트에 필요한 데이터베이스 등의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="da51a-118">리소스 그룹 배포는 서식 파일을 사용 하 여 리소스 그룹에 리소스를 추가 하 고 Azure에서 사용할 수 있도록 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="da51a-119">서식 파일을 사용 하지 않고 리소스 그룹에 리소스를 추가 하려면 New-AzureRmResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="da51a-120">리소스 그룹 배포를 추가 하려면 기존 리소스 그룹 및 리소스 그룹 서식 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="da51a-121">리소스 그룹 템플릿은 웹 포털 등의 복잡 한 클라우드 기반 서비스에 대 한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="da51a-122">이 템플릿에는 필수 리소스 및 구성 가능한 속성 값 (예: 이름 및 크기)에 대 한 매개 변수 자리 표시 자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="da51a-123">Azure 서식 파일 갤러리에서 여러 서식 파일을 찾을 수도 있고 서식 파일을 직접 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="da51a-124">**AzureRmResourceGroupGalleryTemplate** cmdlet을 사용 하 여 갤러리에서 서식 파일을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="da51a-125">사용자 지정 서식 파일을 사용 하 여 리소스 그룹을 만들려면 하위 *서식 파일* 매개 변수 또는 하위 *서식 uri* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="da51a-126">각 템플릿에는 구성 가능한 속성에 대 한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="da51a-127">서식 파일 매개 변수에 대 한 값을 지정 하려면 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="da51a-128">또는 템플릿을 지정할 때 명령에 동적으로 추가 되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="da51a-129">동적 매개 변수를 사용 하려면 명령 프롬프트에 입력 하거나 빼기 기호 (-)를 입력 하 여 매개 변수를 나타내고 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="da51a-130">명령 프롬프트에서 입력 하는 템플릿 매개 변수 값은 template 매개 변수 개체 또는 파일의 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="da51a-131">예제의</span><span class="sxs-lookup"><span data-stu-id="da51a-131">EXAMPLES</span></span>

### <span data-ttu-id="da51a-132">예제 1: 사용자 지정 서식 파일 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="da51a-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="da51a-133">이 명령은 사용자 지정 서식 파일과 디스크의 서식 파일을 사용 하 여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="da51a-134">이 명령은 template *파일* 매개 변수를 사용 하 여 템플릿과 매개 변수 값이 포함 된 파일을 지정 하는 서식 파일과 템플릿 매개 변수 *파일* 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="da51a-135">서식 파일 *버전* 매개 변수를 사용 하 여 템플릿의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="da51a-136">변수</span><span class="sxs-lookup"><span data-stu-id="da51a-136">PARAMETERS</span></span>

### <span data-ttu-id="da51a-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da51a-137">-ApiVersion</span></span>
<span data-ttu-id="da51a-138">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="da51a-139">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="da51a-140">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="da51a-140">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="da51a-141">디버그 로그 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-141">Specifies a debug log level.</span></span>
<span data-ttu-id="da51a-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da51a-143">RequestContent</span><span class="sxs-lookup"><span data-stu-id="da51a-143">RequestContent</span></span> 
- <span data-ttu-id="da51a-144">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="da51a-144">ResponseContent</span></span> 
- <span data-ttu-id="da51a-145">모든</span><span class="sxs-lookup"><span data-stu-id="da51a-145">All</span></span> 
- <span data-ttu-id="da51a-146">않아야</span><span class="sxs-lookup"><span data-stu-id="da51a-146">None</span></span>

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

### <span data-ttu-id="da51a-147">-Force</span><span class="sxs-lookup"><span data-stu-id="da51a-147">-Force</span></span>
<span data-ttu-id="da51a-148">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-148">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da51a-149">-모드</span><span class="sxs-lookup"><span data-stu-id="da51a-149">-Mode</span></span>
<span data-ttu-id="da51a-150">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-150">Specifies the deployment mode.</span></span> <span data-ttu-id="da51a-151">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da51a-152">마칠</span><span class="sxs-lookup"><span data-stu-id="da51a-152">Complete</span></span> 
- <span data-ttu-id="da51a-153">진행</span><span class="sxs-lookup"><span data-stu-id="da51a-153">Incremental</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-154">-이름</span><span class="sxs-lookup"><span data-stu-id="da51a-154">-Name</span></span>
<span data-ttu-id="da51a-155">만들려는 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-155">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="da51a-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="da51a-156">-Pre</span></span>
<span data-ttu-id="da51a-157">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="da51a-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da51a-158">-ResourceGroupName</span></span>
<span data-ttu-id="da51a-159">배포할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-159">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="da51a-160">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="da51a-160">-TemplateFile</span></span>
<span data-ttu-id="da51a-161">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-161">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="da51a-162">이는 사용자 지정 서식 파일 이거나 **AzureRmResourceGroupGalleryTemplate** cmdlet을 사용 하 여 만든 것과 같은 JSON 파일로 저장 되는 갤러리 서식 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-162">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-163">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="da51a-163">-TemplateParameterFile</span></span>
<span data-ttu-id="da51a-164">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-164">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="da51a-165">템플릿에 매개 변수가 포함 된 경우에는 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 사용 하 여 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-165">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="da51a-166">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-166">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="da51a-167">동적 매개 변수를 사용 하려면 매개 변수 이름을 나타내는 빼기 기호 (-)를 입력 한 다음 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-167">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-168">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="da51a-168">-TemplateParameterObject</span></span>
<span data-ttu-id="da51a-169">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-169">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="da51a-170">Windows PowerShell의 해시 테이블에 대 한 도움말을 보려면를 입력 `Get-Help about_Hash_Tables` 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-170">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="da51a-171">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-171">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="da51a-172">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-173">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="da51a-173">-TemplateParameterUri</span></span>
<span data-ttu-id="da51a-174">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-174">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-175">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="da51a-175">-TemplateUri</span></span>
<span data-ttu-id="da51a-176">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-176">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="da51a-177">이 파일은 **AzureRmResourceGroupGalleryTemplate** 를 사용 하는 것과 같이 JSON 파일로 저장 되는 사용자 지정 서식 파일 또는 갤러리 서식 파일이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-177">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-178">-확인</span><span class="sxs-lookup"><span data-stu-id="da51a-178">-Confirm</span></span>
<span data-ttu-id="da51a-179">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da51a-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da51a-180">-WhatIf</span></span>
<span data-ttu-id="da51a-181">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da51a-182">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da51a-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da51a-183">-DefaultProfile</span></span>
<span data-ttu-id="da51a-184">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-184">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da51a-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da51a-185">CommonParameters</span></span>
<span data-ttu-id="da51a-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da51a-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da51a-187">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da51a-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da51a-188">입력</span><span class="sxs-lookup"><span data-stu-id="da51a-188">INPUTS</span></span>

### <span data-ttu-id="da51a-189">않아야</span><span class="sxs-lookup"><span data-stu-id="da51a-189">None</span></span>

## <span data-ttu-id="da51a-190">출력</span><span class="sxs-lookup"><span data-stu-id="da51a-190">OUTPUTS</span></span>

### <span data-ttu-id="da51a-191">. PSResourceGroupDeployment의 모든 모델</span><span class="sxs-lookup"><span data-stu-id="da51a-191">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="da51a-192">상속자</span><span class="sxs-lookup"><span data-stu-id="da51a-192">NOTES</span></span>

## <span data-ttu-id="da51a-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da51a-193">RELATED LINKS</span></span>

[<span data-ttu-id="da51a-194">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da51a-194">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="da51a-195">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="da51a-195">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="da51a-196">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da51a-196">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="da51a-197">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da51a-197">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="da51a-198">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da51a-198">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="da51a-199">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da51a-199">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


