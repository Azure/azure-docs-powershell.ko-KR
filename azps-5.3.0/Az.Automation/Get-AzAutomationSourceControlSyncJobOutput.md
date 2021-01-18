---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494304"
---
# <span data-ttu-id="312cf-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="312cf-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="312cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="312cf-102">SYNOPSIS</span></span>
<span data-ttu-id="312cf-103">Azure Automation 원본 제어 동기화 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="312cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="312cf-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="312cf-105">설명</span><span class="sxs-lookup"><span data-stu-id="312cf-105">DESCRIPTION</span></span>
<span data-ttu-id="312cf-106">**Get-AzAutomationSourceControlSyncJobOutput** cmdlet은 Azure Automation 원본 제어 동기화 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="312cf-107">예제</span><span class="sxs-lookup"><span data-stu-id="312cf-107">EXAMPLES</span></span>

### <span data-ttu-id="312cf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="312cf-108">Example 1</span></span>
<span data-ttu-id="312cf-109">이 명령은 소스 제어 VSTSNative에 대한 ID 08d6d266-27b6-463c-beea-bc48a67ace15를 사용하여 원본 제어 동기화 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="312cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="312cf-110">PARAMETERS</span></span>

### <span data-ttu-id="312cf-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="312cf-111">-AutomationAccountName</span></span>
<span data-ttu-id="312cf-112">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-112">The automation account name.</span></span>

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

### <span data-ttu-id="312cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312cf-113">-DefaultProfile</span></span>
<span data-ttu-id="312cf-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="312cf-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="312cf-115">-JobId</span></span>
<span data-ttu-id="312cf-116">원본 제어 동기화 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="312cf-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-118">The resource group name.</span></span>

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

### <span data-ttu-id="312cf-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="312cf-119">-SourceControlName</span></span>
<span data-ttu-id="312cf-120">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-120">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312cf-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="312cf-121">-Stream</span></span>
<span data-ttu-id="312cf-122">스트림 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-122">The stream type.</span></span>
<span data-ttu-id="312cf-123">기본값은 Any입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312cf-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="312cf-124">-StreamId</span></span>
<span data-ttu-id="312cf-125">스트림 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312cf-126">CommonParameters</span></span>
<span data-ttu-id="312cf-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="312cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312cf-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="312cf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312cf-129">입력</span><span class="sxs-lookup"><span data-stu-id="312cf-129">INPUTS</span></span>

### <span data-ttu-id="312cf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="312cf-130">System.String</span></span>

### <span data-ttu-id="312cf-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="312cf-131">System.Guid</span></span>

### <span data-ttu-id="312cf-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="312cf-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="312cf-133">출력</span><span class="sxs-lookup"><span data-stu-id="312cf-133">OUTPUTS</span></span>

### <span data-ttu-id="312cf-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="312cf-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="312cf-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="312cf-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="312cf-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="312cf-136">NOTES</span></span>

## <span data-ttu-id="312cf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="312cf-137">RELATED LINKS</span></span>
