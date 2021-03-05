---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976459"
---
# <span data-ttu-id="4dba1-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dba1-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4dba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dba1-102">SYNOPSIS</span></span>
<span data-ttu-id="4dba1-103">리소스 그룹 배포의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="4dba1-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dba1-104">SYNTAX</span></span>

### <span data-ttu-id="4dba1-105">ByTemplateFileWithNoParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="4dba1-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dba1-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dba1-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dba1-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dba1-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dba1-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dba1-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dba1-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="4dba1-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dba1-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dba1-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dba1-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="4dba1-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dba1-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4dba1-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dba1-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4dba1-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dba1-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="4dba1-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dba1-120">설명</span><span class="sxs-lookup"><span data-stu-id="4dba1-120">DESCRIPTION</span></span>
<span data-ttu-id="4dba1-121">**Test-AzResourceGroupDeployment** cmdlet은 Azure 리소스 그룹 배포 템플릿 및 해당 매개 변수 값이 유효한지 여부를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4dba1-122">예제</span><span class="sxs-lookup"><span data-stu-id="4dba1-122">EXAMPLES</span></span>

### <span data-ttu-id="4dba1-123">예제 1: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용하여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="4dba1-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4dba1-124">이 명령은 지정한 템플릿 파일 및 매개 변수 파일에서 만든 메모리 내 해시테이블을 사용하여 주어진 리소스 그룹의 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="4dba1-125">예제 2: 템플릿 파일 및 매개 변수 파일을 통해 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="4dba1-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="4dba1-126">이 명령은 제공된 템플릿 파일 및 매개 변수 파일을 사용하여 주어진 리소스 그룹 및 리소스의 배포를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="4dba1-127">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dba1-127">PARAMETERS</span></span>

### <span data-ttu-id="4dba1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dba1-128">-DefaultProfile</span></span>
<span data-ttu-id="4dba1-129">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4dba1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dba1-130">-Mode</span><span class="sxs-lookup"><span data-stu-id="4dba1-130">-Mode</span></span>
<span data-ttu-id="4dba1-131">배포 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="4dba1-132">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dba1-133">증분</span><span class="sxs-lookup"><span data-stu-id="4dba1-133">Incremental</span></span>
- <span data-ttu-id="4dba1-134">완료</span><span class="sxs-lookup"><span data-stu-id="4dba1-134">Complete</span></span>

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

### <span data-ttu-id="4dba1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="4dba1-135">-Pre</span></span>
<span data-ttu-id="4dba1-136">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4dba1-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="4dba1-137">-QueryString</span></span>
<span data-ttu-id="4dba1-138">TemplateUri 매개 변수와 함께 사용할 쿼리 문자열(예: SAS 토큰)입니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="4dba1-139">연결된 템플릿의 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="4dba1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dba1-140">-ResourceGroupName</span></span>
<span data-ttu-id="4dba1-141">테스트할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="4dba1-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="4dba1-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="4dba1-143">-RollbackToLastDeployment를 사용하는 경우 리소스 그룹에서 지정한 이름으로 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="4dba1-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="4dba1-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="4dba1-145">-RollBackDeploymentName을 사용하는 경우 리소스 그룹의 마지막 성공적인 배포로 롤백하면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="4dba1-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4dba1-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4dba1-147">제공된 템플릿 매개 변수에 템플릿에서 사용되는 모든 필요한 매개 변수가 포함되어 있는지 검사하는 PowerShell 동적 매개 변수 처리를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="4dba1-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4dba1-148">이 검사는 사용자에게 누락된 매개 변수에 대한 값을 제공하라는 메시지를 표시하지만 -SkipTemplateParameterPrompt를 제공하면 매개 변수가 템플릿에 바인딩되지 않은 경우 즉시 이 프롬프트와 오류를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4dba1-149">대화형이 아닌 스크립트의 경우 -SkipTemplateParameterPrompt를 제공하여 필요한 모든 매개 변수가 충족되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4dba1-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4dba1-150">-TemplateFile</span></span>
<span data-ttu-id="4dba1-151">템플릿 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="4dba1-152">지원되는 템플릿 파일 형식: json 및 bicep입니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="4dba1-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4dba1-153">-TemplateObject</span></span>
<span data-ttu-id="4dba1-154">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4dba1-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dba1-155">-TemplateParameterFile</span></span>
<span data-ttu-id="4dba1-156">템플릿 매개 변수의 이름과 값을 포함하는 JSON 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="4dba1-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dba1-157">-TemplateParameterObject</span></span>
<span data-ttu-id="4dba1-158">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="4dba1-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dba1-159">-TemplateParameterUri</span></span>
<span data-ttu-id="4dba1-160">템플릿 매개 변수 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-160">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="4dba1-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="4dba1-161">-TemplateSpecId</span></span>
<span data-ttu-id="4dba1-162">배포할 템플릿Spec의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-162">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="4dba1-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4dba1-163">-TemplateUri</span></span>
<span data-ttu-id="4dba1-164">템플릿 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="4dba1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dba1-165">CommonParameters</span></span>
<span data-ttu-id="4dba1-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dba1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dba1-167">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dba1-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dba1-168">입력</span><span class="sxs-lookup"><span data-stu-id="4dba1-168">INPUTS</span></span>

### <span data-ttu-id="4dba1-169">System.String</span><span class="sxs-lookup"><span data-stu-id="4dba1-169">System.String</span></span>

### <span data-ttu-id="4dba1-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="4dba1-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="4dba1-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dba1-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4dba1-172">출력</span><span class="sxs-lookup"><span data-stu-id="4dba1-172">OUTPUTS</span></span>

### <span data-ttu-id="4dba1-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="4dba1-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="4dba1-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dba1-174">NOTES</span></span>

## <span data-ttu-id="4dba1-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dba1-175">RELATED LINKS</span></span>

[<span data-ttu-id="4dba1-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dba1-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4dba1-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dba1-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4dba1-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dba1-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4dba1-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dba1-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


