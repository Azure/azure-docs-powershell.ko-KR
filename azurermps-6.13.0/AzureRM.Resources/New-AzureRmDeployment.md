---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmDeployment.md
ms.openlocfilehash: 3c28bc2a13bbcfdd496b8df01a757aa683a87802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530079"
---
# <span data-ttu-id="ea038-101">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ea038-101">New-AzureRmDeployment</span></span>

## <span data-ttu-id="ea038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea038-102">SYNOPSIS</span></span>
<span data-ttu-id="ea038-103">배포 만들기</span><span class="sxs-lookup"><span data-stu-id="ea038-103">Creat a deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea038-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea038-104">SYNTAX</span></span>

### <span data-ttu-id="ea038-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea038-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-106">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="ea038-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-107">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="ea038-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-108">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="ea038-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-109">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="ea038-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-110">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="ea038-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-111">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="ea038-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea038-112">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="ea038-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea038-113">설명은</span><span class="sxs-lookup"><span data-stu-id="ea038-113">DESCRIPTION</span></span>
<span data-ttu-id="ea038-114">**새 AzureRmDeployment** cmdlet은 현재 구독 범위에 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-114">The **New-AzureRmDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="ea038-115">여기에는 배포에 필요한 리소스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="ea038-116">Azure 리소스는 사용자가 관리 하는 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="ea038-117">리소스는 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 컴퓨터 또는 저장소 계정과 같은 리소스 그룹에 살고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="ea038-118">또는 역할 정의, 정책 정의 등과 같은 구독 수준 리소스 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="ea038-119">리소스 그룹에 리소스를 추가 하려면 리소스 그룹에 배포를 만드는 **New AzureRmDeployment** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-119">To add resources to a resource group, use the **New-AzureRmDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="ea038-120">**AzureRmDeployment** cmdlet은 구독 수준 리소스를 배포 하는 현재 구독 범위에서 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-120">The **New-AzureRmDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="ea038-121">구독에서 배포를 추가 하려면 위치 및 템플릿을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="ea038-122">위치는 Azure 리소스 관리자에 배포 데이터를 저장할 위치를 알려 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="ea038-123">템플릿은 배포할 개별 리소스를 포함 하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="ea038-124">이 템플릿에는 필수 리소스 및 구성 가능한 속성 값 (예: 이름 및 크기)에 대 한 매개 변수 자리 표시 자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="ea038-125">배포에 사용자 지정 서식 파일을 사용 하려면 *서식 파일 file* 매개 변수 또는 template *uri* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="ea038-126">각 템플릿에는 구성 가능한 속성에 대 한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="ea038-127">서식 파일 매개 변수에 대 한 값을 지정 하려면 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="ea038-128">또는 템플릿을 지정할 때 명령에 동적으로 추가 되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="ea038-129">동적 매개 변수를 사용 하려면 명령 프롬프트에 입력 하거나 빼기 기호 (-)를 입력 하 여 매개 변수를 나타내고 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="ea038-130">명령 프롬프트에서 입력 하는 템플릿 매개 변수 값은 template 매개 변수 개체 또는 파일의 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="ea038-131">예제의</span><span class="sxs-lookup"><span data-stu-id="ea038-131">EXAMPLES</span></span>

### <span data-ttu-id="ea038-132">예제 1: 사용자 지정 서식 파일 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="ea038-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="ea038-133">이 명령은 사용자 지정 서식 파일과 디스크의 서식 파일을 사용 하 여 현재 구독 범위에서 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="ea038-134">이 명령은 template *파일* 매개 변수를 사용 하 여 템플릿과 매개 변수 값이 포함 된 파일을 지정 하는 서식 파일과 템플릿 매개 변수 *파일* 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="ea038-135">서식 파일 *버전* 매개 변수를 사용 하 여 템플릿의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="ea038-136">변수</span><span class="sxs-lookup"><span data-stu-id="ea038-136">PARAMETERS</span></span>

### <span data-ttu-id="ea038-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ea038-137">-ApiVersion</span></span>
<span data-ttu-id="ea038-138">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ea038-139">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ea038-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea038-140">-AsJob</span></span>
<span data-ttu-id="ea038-141">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ea038-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea038-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea038-142">-DefaultProfile</span></span>
<span data-ttu-id="ea038-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea038-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="ea038-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="ea038-145">배포 디버그 로그 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="ea038-146">-위치</span><span class="sxs-lookup"><span data-stu-id="ea038-146">-Location</span></span>
<span data-ttu-id="ea038-147">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-147">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea038-148">-이름</span><span class="sxs-lookup"><span data-stu-id="ea038-148">-Name</span></span>
<span data-ttu-id="ea038-149">만들려는 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="ea038-150">서식 파일을 사용 하는 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-150">Only valid when a template is used.</span></span>
<span data-ttu-id="ea038-151">서식 파일을 사용 하는 경우 사용자가 배포 이름을 지정 하지 않으면 "20131223140835"과 같은 현재 시간을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea038-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea038-152">-Pre</span></span>
<span data-ttu-id="ea038-153">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ea038-154">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="ea038-154">-TemplateFile</span></span>
<span data-ttu-id="ea038-155">서식 파일에 대 한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="ea038-156">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="ea038-156">-TemplateParameterFile</span></span>
<span data-ttu-id="ea038-157">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ea038-158">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="ea038-158">-TemplateParameterObject</span></span>
<span data-ttu-id="ea038-159">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ea038-160">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="ea038-160">-TemplateParameterUri</span></span>
<span data-ttu-id="ea038-161">Template 매개 변수 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ea038-162">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="ea038-162">-TemplateUri</span></span>
<span data-ttu-id="ea038-163">템플릿 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="ea038-164">-확인</span><span class="sxs-lookup"><span data-stu-id="ea038-164">-Confirm</span></span>
<span data-ttu-id="ea038-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea038-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea038-166">-WhatIf</span></span>
<span data-ttu-id="ea038-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea038-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea038-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea038-169">CommonParameters</span></span>
<span data-ttu-id="ea038-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea038-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea038-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea038-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea038-172">입력</span><span class="sxs-lookup"><span data-stu-id="ea038-172">INPUTS</span></span>

### <span data-ttu-id="ea038-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea038-173">System.String</span></span>
<span data-ttu-id="ea038-174">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ea038-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ea038-175">출력</span><span class="sxs-lookup"><span data-stu-id="ea038-175">OUTPUTS</span></span>

### <span data-ttu-id="ea038-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ea038-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ea038-177">상속자</span><span class="sxs-lookup"><span data-stu-id="ea038-177">NOTES</span></span>

## <span data-ttu-id="ea038-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea038-178">RELATED LINKS</span></span>
