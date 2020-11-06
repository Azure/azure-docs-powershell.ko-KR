---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528834"
---
# <span data-ttu-id="baa77-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="baa77-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="baa77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa77-102">SYNOPSIS</span></span>
<span data-ttu-id="baa77-103">리소스 그룹에 Azure 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baa77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="baa77-104">SYNTAX</span></span>

### <span data-ttu-id="baa77-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="baa77-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa77-106">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="baa77-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa77-107">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="baa77-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa77-108">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="baa77-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baa77-109">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="baa77-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baa77-110">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="baa77-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baa77-111">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="baa77-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baa77-112">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="baa77-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa77-113">설명은</span><span class="sxs-lookup"><span data-stu-id="baa77-113">DESCRIPTION</span></span>
<span data-ttu-id="baa77-114">**새 AzureRmResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="baa77-115">여기에는 배포에 필요한 리소스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="baa77-116">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 컴퓨터 또는 저장소 계정)입니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="baa77-117">Azure 리소스 그룹은 웹 사이트, 데이터베이스 서버, 재무 웹 사이트에 필요한 데이터베이스 등의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="baa77-118">리소스 그룹 배포는 서식 파일을 사용 하 여 리소스 그룹에 리소스를 추가 하 고 Azure에서 사용할 수 있도록 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="baa77-119">서식 파일을 사용 하지 않고 리소스 그룹에 리소스를 추가 하려면 New-AzureRmResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="baa77-120">리소스 그룹 배포를 추가 하려면 기존 리소스 그룹 및 리소스 그룹 서식 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="baa77-121">리소스 그룹 템플릿은 웹 포털 등의 복잡 한 클라우드 기반 서비스에 대 한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="baa77-122">이 템플릿에는 필수 리소스 및 구성 가능한 속성 값 (예: 이름 및 크기)에 대 한 매개 변수 자리 표시 자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="baa77-123">Azure 서식 파일 갤러리에서 여러 서식 파일을 찾을 수도 있고 서식 파일을 직접 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="baa77-124">**AzureRmResourceGroupGalleryTemplate** cmdlet을 사용 하 여 갤러리에서 서식 파일을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="baa77-125">사용자 지정 서식 파일을 사용 하 여 리소스 그룹을 만들려면 하위 *서식 파일* 매개 변수 또는 하위 *서식 uri* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="baa77-126">각 템플릿에는 구성 가능한 속성에 대 한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="baa77-127">서식 파일 매개 변수에 대 한 값을 지정 하려면 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="baa77-128">또는 템플릿을 지정할 때 명령에 동적으로 추가 되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="baa77-129">동적 매개 변수를 사용 하려면 명령 프롬프트에 입력 하거나 빼기 기호 (-)를 입력 하 여 매개 변수를 나타내고 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="baa77-130">명령 프롬프트에서 입력 하는 템플릿 매개 변수 값은 template 매개 변수 개체 또는 파일의 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="baa77-131">예제의</span><span class="sxs-lookup"><span data-stu-id="baa77-131">EXAMPLES</span></span>

### <span data-ttu-id="baa77-132">예제 1: 사용자 지정 서식 파일 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="baa77-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="baa77-133">이 명령은 사용자 지정 서식 파일과 디스크의 서식 파일을 사용 하 여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="baa77-134">이 명령은 template *파일* 매개 변수를 사용 하 여 템플릿과 매개 변수 값이 포함 된 파일을 지정 하는 서식 파일과 템플릿 매개 변수 *파일* 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="baa77-135">서식 파일 *버전* 매개 변수를 사용 하 여 템플릿의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="baa77-136">변수</span><span class="sxs-lookup"><span data-stu-id="baa77-136">PARAMETERS</span></span>

### <span data-ttu-id="baa77-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="baa77-137">-ApiVersion</span></span>
<span data-ttu-id="baa77-138">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="baa77-139">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-139">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baa77-140">-AsJob</span></span>
<span data-ttu-id="baa77-141">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="baa77-141">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa77-142">-DefaultProfile</span></span>
<span data-ttu-id="baa77-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="baa77-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="baa77-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="baa77-145">디버그 로그 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-145">Specifies a debug log level.</span></span>
<span data-ttu-id="baa77-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="baa77-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="baa77-147">RequestContent</span></span>
- <span data-ttu-id="baa77-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="baa77-148">ResponseContent</span></span>
- <span data-ttu-id="baa77-149">모든</span><span class="sxs-lookup"><span data-stu-id="baa77-149">All</span></span>
- <span data-ttu-id="baa77-150">않아야</span><span class="sxs-lookup"><span data-stu-id="baa77-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-151">-Force</span><span class="sxs-lookup"><span data-stu-id="baa77-151">-Force</span></span>
<span data-ttu-id="baa77-152">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-152">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-153">-모드</span><span class="sxs-lookup"><span data-stu-id="baa77-153">-Mode</span></span>
<span data-ttu-id="baa77-154">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-154">Specifies the deployment mode.</span></span> <span data-ttu-id="baa77-155">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="baa77-156">마칠</span><span class="sxs-lookup"><span data-stu-id="baa77-156">Complete</span></span>
- <span data-ttu-id="baa77-157">진행</span><span class="sxs-lookup"><span data-stu-id="baa77-157">Incremental</span></span>

<span data-ttu-id="baa77-158">완료 모드에서 리소스 관리자는 리소스 그룹에 존재 하지만 서식 파일에 지정 되지 않은 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="baa77-159">증분 모드에서 리소스 관리자는 리소스 그룹에는 있지만 서식 파일에 지정 되지 않은 변경 되지 않은 리소스를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-160">-이름</span><span class="sxs-lookup"><span data-stu-id="baa77-160">-Name</span></span>
<span data-ttu-id="baa77-161">만들려는 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="baa77-162">-Pre</span></span>
<span data-ttu-id="baa77-163">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa77-164">-ResourceGroupName</span></span>
<span data-ttu-id="baa77-165">배포할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-166">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="baa77-166">-TemplateFile</span></span>
<span data-ttu-id="baa77-167">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="baa77-168">이는 사용자 지정 서식 파일 이거나 **AzureRmResourceGroupGalleryTemplate** cmdlet을 사용 하 여 만든 것과 같은 JSON 파일로 저장 되는 갤러리 서식 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-169">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="baa77-169">-TemplateParameterFile</span></span>
<span data-ttu-id="baa77-170">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="baa77-171">템플릿에 매개 변수가 포함 된 경우에는 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 사용 하 여 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="baa77-172">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="baa77-173">동적 매개 변수를 사용 하려면 매개 변수 이름을 나타내는 빼기 기호 (-)를 입력 한 다음 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-174">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="baa77-174">-TemplateParameterObject</span></span>
<span data-ttu-id="baa77-175">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="baa77-176">Windows PowerShell의 해시 테이블에 대 한 도움말을 보려면를 입력 `Get-Help about_Hash_Tables` 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="baa77-177">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="baa77-178">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-179">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="baa77-179">-TemplateParameterUri</span></span>
<span data-ttu-id="baa77-180">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-181">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="baa77-181">-TemplateUri</span></span>
<span data-ttu-id="baa77-182">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="baa77-183">이 파일은 **AzureRmResourceGroupGalleryTemplate** 를 사용 하는 것과 같이 JSON 파일로 저장 되는 사용자 지정 서식 파일 또는 갤러리 서식 파일이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-184">-확인</span><span class="sxs-lookup"><span data-stu-id="baa77-184">-Confirm</span></span>
<span data-ttu-id="baa77-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa77-186">-WhatIf</span></span>
<span data-ttu-id="baa77-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa77-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa77-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa77-189">CommonParameters</span></span>
<span data-ttu-id="baa77-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa77-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa77-191">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa77-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa77-192">입력</span><span class="sxs-lookup"><span data-stu-id="baa77-192">INPUTS</span></span>

### <span data-ttu-id="baa77-193">않아야</span><span class="sxs-lookup"><span data-stu-id="baa77-193">None</span></span>

## <span data-ttu-id="baa77-194">출력</span><span class="sxs-lookup"><span data-stu-id="baa77-194">OUTPUTS</span></span>

### <span data-ttu-id="baa77-195">. PSResourceGroupDeployment의 모든 모델</span><span class="sxs-lookup"><span data-stu-id="baa77-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="baa77-196">상속자</span><span class="sxs-lookup"><span data-stu-id="baa77-196">NOTES</span></span>

## <span data-ttu-id="baa77-197">관련 링크</span><span class="sxs-lookup"><span data-stu-id="baa77-197">RELATED LINKS</span></span>

[<span data-ttu-id="baa77-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="baa77-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="baa77-199">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="baa77-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="baa77-200">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="baa77-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="baa77-201">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="baa77-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="baa77-202">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="baa77-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="baa77-203">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="baa77-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


