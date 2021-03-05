---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5c440c6f150993b947a0db2162ef0fd664e73220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960107"
---
# <span data-ttu-id="9327b-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="9327b-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="9327b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9327b-102">SYNOPSIS</span></span>
<span data-ttu-id="9327b-103">테넌트 범위에서 배포의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="9327b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9327b-104">SYNTAX</span></span>

### <span data-ttu-id="9327b-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="9327b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9327b-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9327b-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9327b-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9327b-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9327b-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9327b-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9327b-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="9327b-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9327b-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9327b-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9327b-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="9327b-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9327b-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9327b-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9327b-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9327b-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9327b-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="9327b-119">ByTemplateSpecResourceId</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9327b-120">설명</span><span class="sxs-lookup"><span data-stu-id="9327b-120">DESCRIPTION</span></span>
<span data-ttu-id="9327b-121">**Test-AzTenantDeployment** cmdlet은 배포 템플릿 및 해당 매개 변수 값이 현재 테넌트 범위에서 유효한지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-121">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="9327b-122">예제</span><span class="sxs-lookup"><span data-stu-id="9327b-122">EXAMPLES</span></span>

### <span data-ttu-id="9327b-123">예제 1: 사용자 지정 템플릿 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="9327b-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="9327b-124">이 명령은 주어진 템플릿 파일 및 매개 변수 파일을 사용하여 현재 테넌트 범위에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-124">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="9327b-125">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="9327b-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="9327b-126">이 명령은 지정한 템플릿 파일 및 매개 변수 파일에서 만든 메모리 내 해시테이블을 사용하여 현재 테넌트 범위에서 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-126">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="9327b-127">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9327b-127">PARAMETERS</span></span>

### <span data-ttu-id="9327b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9327b-128">-DefaultProfile</span></span>
<span data-ttu-id="9327b-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9327b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="9327b-130">-Location</span></span>
<span data-ttu-id="9327b-131">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="9327b-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="9327b-132">-Pre</span></span>
<span data-ttu-id="9327b-133">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9327b-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="9327b-134">-QueryString</span></span>
<span data-ttu-id="9327b-135">TemplateUri 매개 변수와 함께 사용할 쿼리 문자열(예: SAS 토큰)입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="9327b-136">연결된 템플릿의 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="9327b-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9327b-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9327b-138">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필요한 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="9327b-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="9327b-139">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 경우 즉시 이 프롬프트와 오류를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="9327b-140">대화형이 아닌 스크립트의 경우 -SkipTemplateParameterPrompt를 제공하여 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="9327b-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9327b-141">-TemplateFile</span></span>
<span data-ttu-id="9327b-142">템플릿 파일에 대한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-142">Local path to the template file.</span></span> <span data-ttu-id="9327b-143">지원되는 템플릿 파일 형식: json 및 bicep입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="9327b-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9327b-144">-TemplateObject</span></span>
<span data-ttu-id="9327b-145">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="9327b-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9327b-146">-TemplateParameterFile</span></span>
<span data-ttu-id="9327b-147">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="9327b-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9327b-148">-TemplateParameterObject</span></span>
<span data-ttu-id="9327b-149">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="9327b-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9327b-150">-TemplateParameterUri</span></span>
<span data-ttu-id="9327b-151">템플릿 매개 변수 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="9327b-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="9327b-152">-TemplateSpecId</span></span>
<span data-ttu-id="9327b-153">배포할 템플릿Spec의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="9327b-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9327b-154">-TemplateUri</span></span>
<span data-ttu-id="9327b-155">템플릿 파일에 대한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="9327b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9327b-156">CommonParameters</span></span>
<span data-ttu-id="9327b-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9327b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9327b-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9327b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9327b-159">입력</span><span class="sxs-lookup"><span data-stu-id="9327b-159">INPUTS</span></span>

### <span data-ttu-id="9327b-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9327b-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9327b-161">System.String</span><span class="sxs-lookup"><span data-stu-id="9327b-161">System.String</span></span>

## <span data-ttu-id="9327b-162">출력</span><span class="sxs-lookup"><span data-stu-id="9327b-162">OUTPUTS</span></span>

### <span data-ttu-id="9327b-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="9327b-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="9327b-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9327b-164">NOTES</span></span>

## <span data-ttu-id="9327b-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9327b-165">RELATED LINKS</span></span>
