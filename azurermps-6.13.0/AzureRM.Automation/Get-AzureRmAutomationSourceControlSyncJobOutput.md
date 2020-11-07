---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 59de6fa12ef3c6bd774f05fe55d31d74bb9efa13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703484"
---
# <span data-ttu-id="4b0b7-101">Get-AzureRmAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="4b0b7-101">Get-AzureRmAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="4b0b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0b7-103">Azure 자동화 소스 제어 동기화 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-103">Gets the output of an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b0b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b0b7-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b0b7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="4b0b7-106">**AzureRmAutomationSourceControlSyncJobOutput** Cmdlet은 Azure Automation 소스 제어 동기화 작업에 대 한 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-106">The **Get-AzureRmAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="4b0b7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4b0b7-107">EXAMPLES</span></span>

### <span data-ttu-id="4b0b7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b0b7-108">Example 1</span></span>
<span data-ttu-id="4b0b7-109">이 명령은 원본 컨트롤 VSTSNative에 대 한 id 08d6d266-27b6-463c-beea-bc48a67ace15를 사용 하 여 소스 제어 동기화 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
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

## <span data-ttu-id="4b0b7-110">변수</span><span class="sxs-lookup"><span data-stu-id="4b0b7-110">PARAMETERS</span></span>

### <span data-ttu-id="4b0b7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b0b7-111">-AutomationAccountName</span></span>
<span data-ttu-id="4b0b7-112">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-112">The automation account name.</span></span>

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

### <span data-ttu-id="4b0b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0b7-113">-DefaultProfile</span></span>
<span data-ttu-id="4b0b7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b0b7-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="4b0b7-115">-JobId</span></span>
<span data-ttu-id="4b0b7-116">소스 제어 동기화 작업 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="4b0b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b0b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b0b7-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-118">The resource group name.</span></span>

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

### <span data-ttu-id="4b0b7-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="4b0b7-119">-SourceControlName</span></span>
<span data-ttu-id="4b0b7-120">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-120">The source control name.</span></span>

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

### <span data-ttu-id="4b0b7-121">-스트림</span><span class="sxs-lookup"><span data-stu-id="4b0b7-121">-Stream</span></span>
<span data-ttu-id="4b0b7-122">스트림 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-122">The stream type.</span></span>
<span data-ttu-id="4b0b7-123">기본적으로 모두로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="4b0b7-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="4b0b7-124">-StreamId</span></span>
<span data-ttu-id="4b0b7-125">스트림 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-125">The stream id.</span></span>

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

### <span data-ttu-id="4b0b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0b7-126">CommonParameters</span></span>
<span data-ttu-id="4b0b7-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0b7-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b0b7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0b7-129">입력</span><span class="sxs-lookup"><span data-stu-id="4b0b7-129">INPUTS</span></span>

### <span data-ttu-id="4b0b7-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4b0b7-130">System.String</span></span>

### <span data-ttu-id="4b0b7-131">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="4b0b7-131">System.Guid</span></span>

### <span data-ttu-id="4b0b7-132">SourceControlSyncJobStreamType-. m m.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="4b0b7-133">출력</span><span class="sxs-lookup"><span data-stu-id="4b0b7-133">OUTPUTS</span></span>

### <span data-ttu-id="4b0b7-134">SourceControlSyncJobStream를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="4b0b7-135">SourceControlSyncJobStreamRecord를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="4b0b7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4b0b7-136">NOTES</span></span>

## <span data-ttu-id="4b0b7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b0b7-137">RELATED LINKS</span></span>
