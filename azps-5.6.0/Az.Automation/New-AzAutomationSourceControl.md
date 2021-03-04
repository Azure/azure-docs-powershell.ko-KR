---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: d9fbbed1beb67ce1bc8732cb5641c78705fd6a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956496"
---
# <span data-ttu-id="b3819-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="b3819-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="b3819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3819-102">SYNOPSIS</span></span>
<span data-ttu-id="b3819-103">Automation 원본 컨트롤을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="b3819-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3819-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3819-105">설명</span><span class="sxs-lookup"><span data-stu-id="b3819-105">DESCRIPTION</span></span>
<span data-ttu-id="b3819-106">New-AzAutomationSourceControl cmdlet은 내 VSTS TFVC, VSTS Git 또는 GitHub와 Azure Automation 계정을 연결하는 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="b3819-107">예제</span><span class="sxs-lookup"><span data-stu-id="b3819-107">EXAMPLES</span></span>

### <span data-ttu-id="b3819-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3819-108">Example 1</span></span>
<span data-ttu-id="b3819-109">내 VSTS TFVC 프로젝트와 Azure Automation 계정을 연결하는 소스 제어 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="b3819-110">TFVC 프로젝트에 분기가 없습니다. 따라서 분기 매개 변수는 지정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="b3819-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="b3819-111">Example 2</span></span>
<span data-ttu-id="b3819-112">내 VSTS Git 프로젝트와 Azure Automation 계정을 연결하는 원본 제어 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="b3819-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="b3819-113">Example 3</span></span>
<span data-ttu-id="b3819-114">내 Azure Automation 계정을 내 GitHub 프로젝트와 연결하는 소스 제어 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="b3819-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3819-115">PARAMETERS</span></span>

### <span data-ttu-id="b3819-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="b3819-116">-AccessToken</span></span>
<span data-ttu-id="b3819-117">원본 제어 액세스 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3819-118">-AutomationAccountName</span></span>
<span data-ttu-id="b3819-119">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="b3819-120">-Branch</span></span>
<span data-ttu-id="b3819-121">원본 제어 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-121">The source control branch.</span></span>

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

### <span data-ttu-id="b3819-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3819-122">-DefaultProfile</span></span>
<span data-ttu-id="b3819-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3819-124">-Description</span><span class="sxs-lookup"><span data-stu-id="b3819-124">-Description</span></span>
<span data-ttu-id="b3819-125">원본 제어 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-125">The source control description.</span></span>

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

### <span data-ttu-id="b3819-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="b3819-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="b3819-127">원본 컨트롤의 publishRunbook 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="b3819-128">DoNotPublishRunbook을 설정하면 사용자 Runbook을 '초안'으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="b3819-129">-EnableAutoSync</span></span>
<span data-ttu-id="b3819-130">원본 컨트롤에 대한 autoSync 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="b3819-131">-FolderPath</span></span>
<span data-ttu-id="b3819-132">원본 제어 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-132">The source control folder path.</span></span>

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

### <span data-ttu-id="b3819-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b3819-133">-Name</span></span>
<span data-ttu-id="b3819-134">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-134">The source control name.</span></span>

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

### <span data-ttu-id="b3819-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="b3819-135">-RepoUrl</span></span>
<span data-ttu-id="b3819-136">원본 제어 리포지포지타 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3819-137">-ResourceGroupName</span></span>
<span data-ttu-id="b3819-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="b3819-139">-SourceType</span></span>
<span data-ttu-id="b3819-140">원본 제어 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-141">-확인</span><span class="sxs-lookup"><span data-stu-id="b3819-141">-Confirm</span></span>
<span data-ttu-id="b3819-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3819-143">-WhatIf</span></span>
<span data-ttu-id="b3819-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3819-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3819-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3819-146">CommonParameters</span></span>
<span data-ttu-id="b3819-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3819-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3819-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3819-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3819-149">입력</span><span class="sxs-lookup"><span data-stu-id="b3819-149">INPUTS</span></span>

### <span data-ttu-id="b3819-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b3819-150">System.String</span></span>

## <span data-ttu-id="b3819-151">출력</span><span class="sxs-lookup"><span data-stu-id="b3819-151">OUTPUTS</span></span>

### <span data-ttu-id="b3819-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="b3819-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="b3819-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3819-153">NOTES</span></span>

## <span data-ttu-id="b3819-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3819-154">RELATED LINKS</span></span>
