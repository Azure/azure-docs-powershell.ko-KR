---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 6ecdf53ecd762c0c3b8ef378b1e8bc78b301a012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985595"
---
# <span data-ttu-id="c17dd-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c17dd-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c17dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c17dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c17dd-103">관리 그룹에서 배포의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="c17dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="c17dd-104">SYNTAX</span></span>

### <span data-ttu-id="c17dd-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="c17dd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c17dd-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c17dd-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c17dd-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c17dd-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c17dd-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c17dd-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c17dd-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="c17dd-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c17dd-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c17dd-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c17dd-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="c17dd-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c17dd-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c17dd-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c17dd-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c17dd-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c17dd-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="c17dd-119">ByTemplateSpecResourceId</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c17dd-120">설명</span><span class="sxs-lookup"><span data-stu-id="c17dd-120">DESCRIPTION</span></span>
<span data-ttu-id="c17dd-121">**Test-AzManagementGroupDeployment** cmdlet은 배포 템플릿 및 해당 매개 변수 값이 관리 그룹에서 유효한지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-121">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="c17dd-122">예제</span><span class="sxs-lookup"><span data-stu-id="c17dd-122">EXAMPLES</span></span>

### <span data-ttu-id="c17dd-123">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="c17dd-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="c17dd-124">이 명령은 주어진 템플릿 파일 및 매개 변수 파일을 사용하여 관리 그룹 "myMG"에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-124">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="c17dd-125">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="c17dd-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c17dd-126">이 명령은 지정한 템플릿 파일 및 매개 변수 파일에서 만든 메모리 내 해시테이블을 사용하여 관리 그룹 "myMG"에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-126">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="c17dd-127">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c17dd-127">PARAMETERS</span></span>

### <span data-ttu-id="c17dd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17dd-128">-DefaultProfile</span></span>
<span data-ttu-id="c17dd-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c17dd-130">-Location</span><span class="sxs-lookup"><span data-stu-id="c17dd-130">-Location</span></span>
<span data-ttu-id="c17dd-131">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c17dd-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c17dd-132">-ManagementGroupId</span></span>
<span data-ttu-id="c17dd-133">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-133">The management group id.</span></span>

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

### <span data-ttu-id="c17dd-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="c17dd-134">-Pre</span></span>
<span data-ttu-id="c17dd-135">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c17dd-136">-QueryString</span><span class="sxs-lookup"><span data-stu-id="c17dd-136">-QueryString</span></span>
<span data-ttu-id="c17dd-137">TemplateUri 매개 변수와 함께 사용할 쿼리 문자열(예: SAS 토큰)입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-137">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="c17dd-138">연결된 템플릿의 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-138">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="c17dd-139">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c17dd-139">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c17dd-140">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필요한 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="c17dd-140">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c17dd-141">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 경우 즉시 이 프롬프트와 오류를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-141">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c17dd-142">대화형이 아닌 스크립트의 경우 -SkipTemplateParameterPrompt를 제공하여 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-142">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c17dd-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c17dd-143">-TemplateFile</span></span>
<span data-ttu-id="c17dd-144">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-144">Local path to the template file.</span></span> <span data-ttu-id="c17dd-145">지원되는 템플릿 파일 형식: json 및 bicep입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-145">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="c17dd-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c17dd-146">-TemplateObject</span></span>
<span data-ttu-id="c17dd-147">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c17dd-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c17dd-148">-TemplateParameterFile</span></span>
<span data-ttu-id="c17dd-149">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-149">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c17dd-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c17dd-150">-TemplateParameterObject</span></span>
<span data-ttu-id="c17dd-151">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-151">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c17dd-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c17dd-152">-TemplateParameterUri</span></span>
<span data-ttu-id="c17dd-153">템플릿 매개 변수 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-153">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c17dd-154">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="c17dd-154">-TemplateSpecId</span></span>
<span data-ttu-id="c17dd-155">배포할 템플릿Spec의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-155">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="c17dd-156">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c17dd-156">-TemplateUri</span></span>
<span data-ttu-id="c17dd-157">템플릿 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-157">Uri to the template file.</span></span>

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

### <span data-ttu-id="c17dd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17dd-158">CommonParameters</span></span>
<span data-ttu-id="c17dd-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c17dd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17dd-160">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c17dd-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17dd-161">입력</span><span class="sxs-lookup"><span data-stu-id="c17dd-161">INPUTS</span></span>

### <span data-ttu-id="c17dd-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c17dd-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c17dd-163">System.String</span><span class="sxs-lookup"><span data-stu-id="c17dd-163">System.String</span></span>

## <span data-ttu-id="c17dd-164">출력</span><span class="sxs-lookup"><span data-stu-id="c17dd-164">OUTPUTS</span></span>

### <span data-ttu-id="c17dd-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c17dd-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="c17dd-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c17dd-166">NOTES</span></span>

## <span data-ttu-id="c17dd-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c17dd-167">RELATED LINKS</span></span>
