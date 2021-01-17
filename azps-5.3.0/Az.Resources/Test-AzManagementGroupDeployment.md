---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492383"
---
# <span data-ttu-id="835d3-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="835d3-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="835d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="835d3-102">SYNOPSIS</span></span>
<span data-ttu-id="835d3-103">관리 그룹에서 배포의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="835d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="835d3-104">SYNTAX</span></span>

### <span data-ttu-id="835d3-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="835d3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835d3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="835d3-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835d3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="835d3-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835d3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="835d3-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835d3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="835d3-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="835d3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="835d3-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="835d3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="835d3-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="835d3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="835d3-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="835d3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="835d3-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="835d3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="835d3-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="835d3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="835d3-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835d3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="835d3-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="835d3-117">설명</span><span class="sxs-lookup"><span data-stu-id="835d3-117">DESCRIPTION</span></span>
<span data-ttu-id="835d3-118">**Test-AzManagementGroupDeployment** cmdlet은 배포 템플릿 및 해당 매개 변수 값이 관리 그룹에서 유효한지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="835d3-119">예제</span><span class="sxs-lookup"><span data-stu-id="835d3-119">EXAMPLES</span></span>

### <span data-ttu-id="835d3-120">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="835d3-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="835d3-121">이 명령은 주어진 템플릿 파일 및 매개 변수 파일을 사용하여 관리 그룹 "myMG"에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="835d3-122">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="835d3-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="835d3-123">이 명령은 지정한 템플릿 파일 및 매개 변수 파일에서 만든 메모리 내 해시테이블을 사용하여 관리 그룹 "myMG"에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="835d3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="835d3-124">PARAMETERS</span></span>

### <span data-ttu-id="835d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835d3-125">-DefaultProfile</span></span>
<span data-ttu-id="835d3-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="835d3-127">-Location</span><span class="sxs-lookup"><span data-stu-id="835d3-127">-Location</span></span>
<span data-ttu-id="835d3-128">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="835d3-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="835d3-129">-ManagementGroupId</span></span>
<span data-ttu-id="835d3-130">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-130">The management group id.</span></span>

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

### <span data-ttu-id="835d3-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="835d3-131">-Pre</span></span>
<span data-ttu-id="835d3-132">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="835d3-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="835d3-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="835d3-134">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="835d3-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="835d3-135">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="835d3-136">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="835d3-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="835d3-137">-TemplateFile</span></span>
<span data-ttu-id="835d3-138">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="835d3-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="835d3-139">-TemplateObject</span></span>
<span data-ttu-id="835d3-140">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="835d3-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="835d3-141">-TemplateParameterFile</span></span>
<span data-ttu-id="835d3-142">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="835d3-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="835d3-143">-TemplateParameterObject</span></span>
<span data-ttu-id="835d3-144">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="835d3-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="835d3-145">-TemplateParameterUri</span></span>
<span data-ttu-id="835d3-146">템플릿 매개 변수 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="835d3-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="835d3-147">-TemplateUri</span></span>
<span data-ttu-id="835d3-148">템플릿 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="835d3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835d3-149">CommonParameters</span></span>
<span data-ttu-id="835d3-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="835d3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835d3-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="835d3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835d3-152">입력</span><span class="sxs-lookup"><span data-stu-id="835d3-152">INPUTS</span></span>

### <span data-ttu-id="835d3-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="835d3-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="835d3-154">System.String</span><span class="sxs-lookup"><span data-stu-id="835d3-154">System.String</span></span>

## <span data-ttu-id="835d3-155">출력</span><span class="sxs-lookup"><span data-stu-id="835d3-155">OUTPUTS</span></span>

### <span data-ttu-id="835d3-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="835d3-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="835d3-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="835d3-157">NOTES</span></span>

## <span data-ttu-id="835d3-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="835d3-158">RELATED LINKS</span></span>
