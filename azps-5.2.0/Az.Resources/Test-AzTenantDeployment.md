---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329083"
---
# <span data-ttu-id="c55ad-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="c55ad-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="c55ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c55ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c55ad-103">테넌트 범위에서 배포의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="c55ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="c55ad-104">SYNTAX</span></span>

### <span data-ttu-id="c55ad-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="c55ad-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c55ad-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c55ad-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c55ad-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c55ad-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c55ad-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c55ad-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c55ad-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c55ad-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c55ad-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c55ad-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c55ad-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c55ad-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c55ad-117">설명</span><span class="sxs-lookup"><span data-stu-id="c55ad-117">DESCRIPTION</span></span>
<span data-ttu-id="c55ad-118">**Test-AzTenantDeployment** cmdlet은 배포 템플릿 및 해당 매개 변수 값이 현재 테넌트 범위에서 유효한지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="c55ad-119">예제</span><span class="sxs-lookup"><span data-stu-id="c55ad-119">EXAMPLES</span></span>

### <span data-ttu-id="c55ad-120">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="c55ad-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="c55ad-121">이 명령은 주어진 템플릿 파일 및 매개 변수 파일을 사용하여 현재 테넌트 범위에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="c55ad-122">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="c55ad-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c55ad-123">이 명령은 지정한 템플릿 파일 및 매개 변수 파일에서 만든 메모리 내 해시테이블을 사용하여 현재 테넌트 범위에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="c55ad-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c55ad-124">PARAMETERS</span></span>

### <span data-ttu-id="c55ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55ad-125">-DefaultProfile</span></span>
<span data-ttu-id="c55ad-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c55ad-127">-Location</span><span class="sxs-lookup"><span data-stu-id="c55ad-127">-Location</span></span>
<span data-ttu-id="c55ad-128">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c55ad-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="c55ad-129">-Pre</span></span>
<span data-ttu-id="c55ad-130">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c55ad-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c55ad-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c55ad-132">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="c55ad-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c55ad-133">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c55ad-134">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c55ad-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c55ad-135">-TemplateFile</span></span>
<span data-ttu-id="c55ad-136">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="c55ad-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c55ad-137">-TemplateObject</span></span>
<span data-ttu-id="c55ad-138">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c55ad-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c55ad-139">-TemplateParameterFile</span></span>
<span data-ttu-id="c55ad-140">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c55ad-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c55ad-141">-TemplateParameterObject</span></span>
<span data-ttu-id="c55ad-142">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c55ad-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c55ad-143">-TemplateParameterUri</span></span>
<span data-ttu-id="c55ad-144">템플릿 매개 변수 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c55ad-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c55ad-145">-TemplateUri</span></span>
<span data-ttu-id="c55ad-146">템플릿 파일에 대한 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="c55ad-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55ad-147">CommonParameters</span></span>
<span data-ttu-id="c55ad-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c55ad-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55ad-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c55ad-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55ad-150">입력</span><span class="sxs-lookup"><span data-stu-id="c55ad-150">INPUTS</span></span>

### <span data-ttu-id="c55ad-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c55ad-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c55ad-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c55ad-152">System.String</span></span>

## <span data-ttu-id="c55ad-153">출력</span><span class="sxs-lookup"><span data-stu-id="c55ad-153">OUTPUTS</span></span>

### <span data-ttu-id="c55ad-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c55ad-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="c55ad-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c55ad-155">NOTES</span></span>

## <span data-ttu-id="c55ad-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c55ad-156">RELATED LINKS</span></span>
