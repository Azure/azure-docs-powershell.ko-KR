---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345093"
---
# <span data-ttu-id="e57fa-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e57fa-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e57fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e57fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e57fa-103">리소스 그룹 배포의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="e57fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="e57fa-104">SYNTAX</span></span>

### <span data-ttu-id="e57fa-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="e57fa-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e57fa-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e57fa-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e57fa-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e57fa-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e57fa-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e57fa-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e57fa-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e57fa-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e57fa-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e57fa-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57fa-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e57fa-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e57fa-117">설명</span><span class="sxs-lookup"><span data-stu-id="e57fa-117">DESCRIPTION</span></span>
<span data-ttu-id="e57fa-118">**Test-AzResourceGroupDeployment** cmdlet은 Azure 리소스 그룹 배포 템플릿 및 해당 매개 변수 값이 유효한지 여부를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="e57fa-119">예제</span><span class="sxs-lookup"><span data-stu-id="e57fa-119">EXAMPLES</span></span>

### <span data-ttu-id="e57fa-120">예제 1: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="e57fa-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="e57fa-121">이 명령은 지정한 템플릿 파일 및 매개 변수 파일에서 만든 메모리 내 해시테이블을 사용하여 주어진 리소스 그룹의 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="e57fa-122">예제 2: 템플릿 파일 및 매개 변수 파일을 통해 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="e57fa-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="e57fa-123">이 명령은 제공된 템플릿 파일 및 매개 변수 파일을 사용하여 주어진 리소스 그룹 및 리소스의 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="e57fa-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e57fa-124">PARAMETERS</span></span>

### <span data-ttu-id="e57fa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57fa-125">-DefaultProfile</span></span>
<span data-ttu-id="e57fa-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e57fa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e57fa-127">-Mode</span><span class="sxs-lookup"><span data-stu-id="e57fa-127">-Mode</span></span>
<span data-ttu-id="e57fa-128">배포 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="e57fa-129">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="e57fa-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e57fa-130">증분</span><span class="sxs-lookup"><span data-stu-id="e57fa-130">Incremental</span></span>
- <span data-ttu-id="e57fa-131">완료</span><span class="sxs-lookup"><span data-stu-id="e57fa-131">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57fa-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e57fa-132">-Pre</span></span>
<span data-ttu-id="e57fa-133">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e57fa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57fa-134">-ResourceGroupName</span></span>
<span data-ttu-id="e57fa-135">테스트할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="e57fa-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="e57fa-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="e57fa-137">-RollbackToLastDeployment를 사용하는 경우 리소스 그룹에서 지정한 이름을 사용하여 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="e57fa-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="e57fa-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="e57fa-139">-RollBackDeploymentName을 사용하는 경우 리소스 그룹에서 마지막으로 성공한 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="e57fa-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e57fa-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e57fa-141">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필수 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="e57fa-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="e57fa-142">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 것으로 확인된 경우 이 프롬프트와 오류가 즉시 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="e57fa-143">비대화형 스크립트의 경우 모든 필수 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공하려면 -SkipTemplateParameterPrompt를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e57fa-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e57fa-144">-TemplateFile</span></span>
<span data-ttu-id="e57fa-145">JSON 템플릿 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="e57fa-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e57fa-146">-TemplateObject</span></span>
<span data-ttu-id="e57fa-147">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e57fa-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e57fa-148">-TemplateParameterFile</span></span>
<span data-ttu-id="e57fa-149">템플릿 매개 변수의 이름 및 값을 포함하는 JSON 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="e57fa-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e57fa-150">-TemplateParameterObject</span></span>
<span data-ttu-id="e57fa-151">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="e57fa-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e57fa-152">-TemplateParameterUri</span></span>
<span data-ttu-id="e57fa-153">템플릿 매개 변수 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="e57fa-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e57fa-154">-TemplateUri</span></span>
<span data-ttu-id="e57fa-155">JSON 템플릿 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="e57fa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57fa-156">CommonParameters</span></span>
<span data-ttu-id="e57fa-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e57fa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57fa-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e57fa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57fa-159">입력</span><span class="sxs-lookup"><span data-stu-id="e57fa-159">INPUTS</span></span>

### <span data-ttu-id="e57fa-160">System.String</span><span class="sxs-lookup"><span data-stu-id="e57fa-160">System.String</span></span>

### <span data-ttu-id="e57fa-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="e57fa-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="e57fa-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e57fa-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e57fa-163">출력</span><span class="sxs-lookup"><span data-stu-id="e57fa-163">OUTPUTS</span></span>

### <span data-ttu-id="e57fa-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="e57fa-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="e57fa-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e57fa-165">NOTES</span></span>

## <span data-ttu-id="e57fa-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e57fa-166">RELATED LINKS</span></span>

[<span data-ttu-id="e57fa-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e57fa-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e57fa-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e57fa-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e57fa-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e57fa-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="e57fa-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e57fa-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


