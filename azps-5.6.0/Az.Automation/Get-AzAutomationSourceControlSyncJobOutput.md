---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 369dfd85b88b079e32e9ea65513d37c99f64b6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014144"
---
# <span data-ttu-id="66872-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="66872-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="66872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66872-102">SYNOPSIS</span></span>
<span data-ttu-id="66872-103">Azure Automation 원본 제어 동기화 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66872-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="66872-104">구문</span><span class="sxs-lookup"><span data-stu-id="66872-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66872-105">설명</span><span class="sxs-lookup"><span data-stu-id="66872-105">DESCRIPTION</span></span>
<span data-ttu-id="66872-106">**Get-AzAutomationSourceControlSyncJobOutput** cmdlet은 Azure Automation 원본 제어 동기화 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66872-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="66872-107">예제</span><span class="sxs-lookup"><span data-stu-id="66872-107">EXAMPLES</span></span>

### <span data-ttu-id="66872-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="66872-108">Example 1</span></span>
<span data-ttu-id="66872-109">이 명령은 원본 제어 VSTSNative에 대한 id 08d6d266-27b6-463c-beea-bc48a67ace15를 사용하여 원본 제어 동기화 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66872-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="66872-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66872-110">PARAMETERS</span></span>

### <span data-ttu-id="66872-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="66872-111">-AutomationAccountName</span></span>
<span data-ttu-id="66872-112">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-112">The automation account name.</span></span>

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

### <span data-ttu-id="66872-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66872-113">-DefaultProfile</span></span>
<span data-ttu-id="66872-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66872-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="66872-115">-JobId</span></span>
<span data-ttu-id="66872-116">원본 제어 동기화 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="66872-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66872-117">-ResourceGroupName</span></span>
<span data-ttu-id="66872-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-118">The resource group name.</span></span>

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

### <span data-ttu-id="66872-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="66872-119">-SourceControlName</span></span>
<span data-ttu-id="66872-120">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-120">The source control name.</span></span>

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

### <span data-ttu-id="66872-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="66872-121">-Stream</span></span>
<span data-ttu-id="66872-122">스트림 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-122">The stream type.</span></span>
<span data-ttu-id="66872-123">기본값은 Any입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="66872-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="66872-124">-StreamId</span></span>
<span data-ttu-id="66872-125">스트림 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="66872-125">The stream id.</span></span>

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

### <span data-ttu-id="66872-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66872-126">CommonParameters</span></span>
<span data-ttu-id="66872-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66872-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66872-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66872-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66872-129">입력</span><span class="sxs-lookup"><span data-stu-id="66872-129">INPUTS</span></span>

### <span data-ttu-id="66872-130">System.String</span><span class="sxs-lookup"><span data-stu-id="66872-130">System.String</span></span>

### <span data-ttu-id="66872-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="66872-131">System.Guid</span></span>

### <span data-ttu-id="66872-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="66872-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="66872-133">출력</span><span class="sxs-lookup"><span data-stu-id="66872-133">OUTPUTS</span></span>

### <span data-ttu-id="66872-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="66872-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="66872-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="66872-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="66872-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66872-136">NOTES</span></span>

## <span data-ttu-id="66872-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66872-137">RELATED LINKS</span></span>
