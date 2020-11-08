---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047924"
---
# <span data-ttu-id="2671d-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="2671d-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="2671d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2671d-102">SYNOPSIS</span></span>
<span data-ttu-id="2671d-103">자동화 원본 컨트롤을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="2671d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2671d-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2671d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2671d-105">DESCRIPTION</span></span>
<span data-ttu-id="2671d-106">New-AzAutomationSourceControl cmdlet은 사용자의 VSTS TFVC, VSTS Git 또는 GitHub와 함께 Azure Automation 계정을 연결 하는 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="2671d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2671d-107">EXAMPLES</span></span>

### <span data-ttu-id="2671d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2671d-108">Example 1</span></span>
<span data-ttu-id="2671d-109">원본 컨트롤 구성을 만들어 내 VSTS TFVC 프로젝트에 Azure Automation 계정을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="2671d-110">TFVC 프로젝트에는 분기가 없기 때문에 분기 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="2671d-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="2671d-111">Example 2</span></span>
<span data-ttu-id="2671d-112">Azure Automation 계정을 사용자의 VSTS Git 프로젝트에 연결 하는 데 사용 되는 소스 제어 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="2671d-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="2671d-113">Example 3</span></span>
<span data-ttu-id="2671d-114">내 GitHub 프로젝트에 Azure Automation 계정을 연결 하는 소스 제어 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="2671d-115">변수</span><span class="sxs-lookup"><span data-stu-id="2671d-115">PARAMETERS</span></span>

### <span data-ttu-id="2671d-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2671d-116">-AccessToken</span></span>
<span data-ttu-id="2671d-117">소스 제어 액세스 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-117">The source control access token.</span></span>

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

### <span data-ttu-id="2671d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2671d-118">-AutomationAccountName</span></span>
<span data-ttu-id="2671d-119">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-119">The automation account name.</span></span>

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

### <span data-ttu-id="2671d-120">-분기</span><span class="sxs-lookup"><span data-stu-id="2671d-120">-Branch</span></span>
<span data-ttu-id="2671d-121">소스 제어 분기입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-121">The source control branch.</span></span>

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

### <span data-ttu-id="2671d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2671d-122">-DefaultProfile</span></span>
<span data-ttu-id="2671d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2671d-124">-설명</span><span class="sxs-lookup"><span data-stu-id="2671d-124">-Description</span></span>
<span data-ttu-id="2671d-125">소스 제어 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-125">The source control description.</span></span>

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

### <span data-ttu-id="2671d-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="2671d-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="2671d-127">원본 컨트롤의 # Runbook 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="2671d-128">DoNotPublishRunbook가 설정 되어 있으면 사용자 runbook을 ' 초안 '으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="2671d-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="2671d-129">-EnableAutoSync</span></span>
<span data-ttu-id="2671d-130">원본 컨트롤에 대 한 autoSync 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="2671d-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="2671d-131">-FolderPath</span></span>
<span data-ttu-id="2671d-132">소스 제어 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-132">The source control folder path.</span></span>

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

### <span data-ttu-id="2671d-133">-이름</span><span class="sxs-lookup"><span data-stu-id="2671d-133">-Name</span></span>
<span data-ttu-id="2671d-134">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-134">The source control name.</span></span>

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

### <span data-ttu-id="2671d-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="2671d-135">-RepoUrl</span></span>
<span data-ttu-id="2671d-136">원본 컨트롤 리포지토리 url</span><span class="sxs-lookup"><span data-stu-id="2671d-136">The source control repo url.</span></span>

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

### <span data-ttu-id="2671d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2671d-137">-ResourceGroupName</span></span>
<span data-ttu-id="2671d-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-138">The resource group name.</span></span>

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

### <span data-ttu-id="2671d-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="2671d-139">-SourceType</span></span>
<span data-ttu-id="2671d-140">소스 컨트롤 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-140">The source control type.</span></span>

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

### <span data-ttu-id="2671d-141">-확인</span><span class="sxs-lookup"><span data-stu-id="2671d-141">-Confirm</span></span>
<span data-ttu-id="2671d-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2671d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2671d-143">-WhatIf</span></span>
<span data-ttu-id="2671d-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2671d-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2671d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2671d-146">CommonParameters</span></span>
<span data-ttu-id="2671d-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2671d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2671d-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2671d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2671d-149">입력</span><span class="sxs-lookup"><span data-stu-id="2671d-149">INPUTS</span></span>

### <span data-ttu-id="2671d-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2671d-150">System.String</span></span>

## <span data-ttu-id="2671d-151">출력</span><span class="sxs-lookup"><span data-stu-id="2671d-151">OUTPUTS</span></span>

### <span data-ttu-id="2671d-152">SourceControl를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="2671d-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="2671d-153">상속자</span><span class="sxs-lookup"><span data-stu-id="2671d-153">NOTES</span></span>

## <span data-ttu-id="2671d-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2671d-154">RELATED LINKS</span></span>
