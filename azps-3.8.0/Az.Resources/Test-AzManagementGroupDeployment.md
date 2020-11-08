---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 81ee04b5248a95d686c2c135dfee0e73e6722bb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041704"
---
# <span data-ttu-id="3523b-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3523b-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="3523b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3523b-102">SYNOPSIS</span></span>
<span data-ttu-id="3523b-103">관리 그룹에서 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="3523b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3523b-104">SYNTAX</span></span>

### <span data-ttu-id="3523b-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="3523b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3523b-106">By서식 Objectandparameterobject</span><span class="sxs-lookup"><span data-stu-id="3523b-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-107">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="3523b-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-108">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="3523b-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-109">By서식 Objectandparameterfile</span><span class="sxs-lookup"><span data-stu-id="3523b-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-110">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="3523b-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-111">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="3523b-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-112">By서식 Objectandparameteruri</span><span class="sxs-lookup"><span data-stu-id="3523b-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-113">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="3523b-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-114">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="3523b-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3523b-115">By서식 Objectwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="3523b-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3523b-116">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="3523b-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3523b-117">설명은</span><span class="sxs-lookup"><span data-stu-id="3523b-117">DESCRIPTION</span></span>
<span data-ttu-id="3523b-118">**테스트 AzManagementGroupDeployment** cmdlet은 관리 그룹에서 배포 템플릿과 해당 매개 변수 값이 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="3523b-119">예제의</span><span class="sxs-lookup"><span data-stu-id="3523b-119">EXAMPLES</span></span>

### <span data-ttu-id="3523b-120">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용 하 여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="3523b-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="3523b-121">이 명령은 지정 된 서식 파일 및 매개 변수 파일을 사용 하 여 관리 그룹 "myMG"에서 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="3523b-122">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용 하 여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="3523b-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="3523b-123">이 명령은 지정 된 템플릿 파일과 매개 변수 파일에서 만든 메모리 내 해시 테이블을 사용 하 여 관리 그룹 "myMG"에서 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="3523b-124">변수</span><span class="sxs-lookup"><span data-stu-id="3523b-124">PARAMETERS</span></span>

### <span data-ttu-id="3523b-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3523b-125">-ApiVersion</span></span>
<span data-ttu-id="3523b-126">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3523b-127">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3523b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3523b-128">-DefaultProfile</span></span>
<span data-ttu-id="3523b-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3523b-130">-위치</span><span class="sxs-lookup"><span data-stu-id="3523b-130">-Location</span></span>
<span data-ttu-id="3523b-131">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3523b-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3523b-132">-ManagementGroupId</span></span>
<span data-ttu-id="3523b-133">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-133">The management group id.</span></span>

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

### <span data-ttu-id="3523b-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="3523b-134">-Pre</span></span>
<span data-ttu-id="3523b-135">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3523b-136">-Skip서식 Parameterprompt</span><span class="sxs-lookup"><span data-stu-id="3523b-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3523b-137">제공 된 템플릿 매개 변수에 템플릿에서 사용 되는 필요한 모든 매개 변수가 포함 되어 있는지 확인 하는 PowerShell 동적 매개 변수 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="3523b-138">이 검사는 누락 된 매개 변수에 대해 사용자에 게 값을 제공 하 라는 메시지를 표시 하지만-Skiptemplate Parameterprompt는이 프롬프트를 무시 하 고 매개 변수를 템플릿에 바인딩하지 않은 경우 즉시 오류를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="3523b-139">비 대화형 스크립트의 경우-Skip비템플릿 Parameterprompt를 제공 하 여 필요한 모든 매개 변수가 충족 되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3523b-140">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="3523b-140">-TemplateFile</span></span>
<span data-ttu-id="3523b-141">서식 파일에 대 한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-141">Local path to the template file.</span></span>

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

### <span data-ttu-id="3523b-142">-서식 개체</span><span class="sxs-lookup"><span data-stu-id="3523b-142">-TemplateObject</span></span>
<span data-ttu-id="3523b-143">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-143">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3523b-144">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="3523b-144">-TemplateParameterFile</span></span>
<span data-ttu-id="3523b-145">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-145">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3523b-146">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="3523b-146">-TemplateParameterObject</span></span>
<span data-ttu-id="3523b-147">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-147">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3523b-148">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="3523b-148">-TemplateParameterUri</span></span>
<span data-ttu-id="3523b-149">Template 매개 변수 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-149">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3523b-150">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="3523b-150">-TemplateUri</span></span>
<span data-ttu-id="3523b-151">템플릿 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-151">Uri to the template file.</span></span>

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

### <span data-ttu-id="3523b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3523b-152">CommonParameters</span></span>
<span data-ttu-id="3523b-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3523b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3523b-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3523b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3523b-155">입력</span><span class="sxs-lookup"><span data-stu-id="3523b-155">INPUTS</span></span>

### <span data-ttu-id="3523b-156">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="3523b-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3523b-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3523b-157">System.String</span></span>

## <span data-ttu-id="3523b-158">출력</span><span class="sxs-lookup"><span data-stu-id="3523b-158">OUTPUTS</span></span>

### <span data-ttu-id="3523b-159">SdkModels. PSResourceManagerError에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="3523b-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="3523b-160">상속자</span><span class="sxs-lookup"><span data-stu-id="3523b-160">NOTES</span></span>

## <span data-ttu-id="3523b-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3523b-161">RELATED LINKS</span></span>
