---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 60db8b7b544b63e29b4834676da946ebbf6c39c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212168"
---
# <span data-ttu-id="1a070-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1a070-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="1a070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a070-102">SYNOPSIS</span></span>
<span data-ttu-id="1a070-103">테 넌 트 범위에서 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="1a070-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a070-104">SYNTAX</span></span>

### <span data-ttu-id="1a070-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a070-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a070-106">By서식 Objectandparameterobject</span><span class="sxs-lookup"><span data-stu-id="1a070-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-107">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="1a070-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-108">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="1a070-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-109">By서식 Objectandparameterfile</span><span class="sxs-lookup"><span data-stu-id="1a070-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-110">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="1a070-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-111">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="1a070-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-112">By서식 Objectandparameteruri</span><span class="sxs-lookup"><span data-stu-id="1a070-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-113">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="1a070-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-114">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="1a070-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a070-115">By서식 Objectwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="1a070-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a070-116">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="1a070-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a070-117">설명은</span><span class="sxs-lookup"><span data-stu-id="1a070-117">DESCRIPTION</span></span>
<span data-ttu-id="1a070-118">**AzTenantDeployment** cmdlet은 배포 템플릿과 해당 매개 변수 값이 현재 테 넌 트 범위에서 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="1a070-119">예제의</span><span class="sxs-lookup"><span data-stu-id="1a070-119">EXAMPLES</span></span>

### <span data-ttu-id="1a070-120">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용 하 여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="1a070-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="1a070-121">이 명령은 지정 된 템플릿 파일 및 매개 변수 파일을 사용 하 여 현재 테 넌 트 범위에서 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="1a070-122">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용 하 여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="1a070-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="1a070-123">이 명령은 지정 된 템플릿 파일과 매개 변수 파일에서 만든 메모리 내 해시 테이블을 사용 하 여 현재 테 넌 트 범위에서 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="1a070-124">변수</span><span class="sxs-lookup"><span data-stu-id="1a070-124">PARAMETERS</span></span>

### <span data-ttu-id="1a070-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1a070-125">-ApiVersion</span></span>
<span data-ttu-id="1a070-126">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1a070-127">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1a070-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a070-128">-DefaultProfile</span></span>
<span data-ttu-id="1a070-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-130">-위치</span><span class="sxs-lookup"><span data-stu-id="1a070-130">-Location</span></span>
<span data-ttu-id="1a070-131">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1a070-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="1a070-132">-Pre</span></span>
<span data-ttu-id="1a070-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1a070-134">-Skip서식 Parameterprompt</span><span class="sxs-lookup"><span data-stu-id="1a070-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1a070-135">제공 된 템플릿 매개 변수에 템플릿에서 사용 되는 필요한 모든 매개 변수가 포함 되어 있는지 확인 하는 PowerShell 동적 매개 변수 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="1a070-136">이 검사는 누락 된 매개 변수에 대해 사용자에 게 값을 제공 하 라는 메시지를 표시 하지만-Skiptemplate Parameterprompt는이 프롬프트를 무시 하 고 매개 변수를 템플릿에 바인딩하지 않은 경우 즉시 오류를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="1a070-137">비 대화형 스크립트의 경우-Skip비템플릿 Parameterprompt를 제공 하 여 필요한 모든 매개 변수가 충족 되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1a070-138">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="1a070-138">-TemplateFile</span></span>
<span data-ttu-id="1a070-139">서식 파일에 대 한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="1a070-140">-서식 개체</span><span class="sxs-lookup"><span data-stu-id="1a070-140">-TemplateObject</span></span>
<span data-ttu-id="1a070-141">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-141">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-142">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="1a070-142">-TemplateParameterFile</span></span>
<span data-ttu-id="1a070-143">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-143">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-144">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="1a070-144">-TemplateParameterObject</span></span>
<span data-ttu-id="1a070-145">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-145">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-146">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="1a070-146">-TemplateParameterUri</span></span>
<span data-ttu-id="1a070-147">Template 매개 변수 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-147">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a070-148">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="1a070-148">-TemplateUri</span></span>
<span data-ttu-id="1a070-149">템플릿 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="1a070-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a070-150">CommonParameters</span></span>
<span data-ttu-id="1a070-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a070-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a070-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a070-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a070-153">입력</span><span class="sxs-lookup"><span data-stu-id="1a070-153">INPUTS</span></span>

### <span data-ttu-id="1a070-154">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1a070-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1a070-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a070-155">System.String</span></span>

## <span data-ttu-id="1a070-156">출력</span><span class="sxs-lookup"><span data-stu-id="1a070-156">OUTPUTS</span></span>

### <span data-ttu-id="1a070-157">SdkModels. PSResourceManagerError에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="1a070-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="1a070-158">상속자</span><span class="sxs-lookup"><span data-stu-id="1a070-158">NOTES</span></span>

## <span data-ttu-id="1a070-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a070-159">RELATED LINKS</span></span>
