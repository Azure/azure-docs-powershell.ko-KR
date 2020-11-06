---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533447"
---
# <span data-ttu-id="1400a-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="1400a-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="1400a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1400a-102">SYNOPSIS</span></span>
<span data-ttu-id="1400a-103">Azure Automation 소스 제어 동기화 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1400a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1400a-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1400a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1400a-105">DESCRIPTION</span></span>
<span data-ttu-id="1400a-106">Get-AzureRmAutomationSourceControlSyncJob cmdlet은 Azure Automation 소스 제어 동기화 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="1400a-107">특정 소스 제어 동기화 작업을 가져오려면 해당 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="1400a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1400a-108">EXAMPLES</span></span>

### <span data-ttu-id="1400a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1400a-109">Example 1</span></span>
<span data-ttu-id="1400a-110">이 명령은 소스 제어 VSTSNative에 대 한 모든 자동화 소스 제어 동기화 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="1400a-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="1400a-111">Example 2</span></span>
<span data-ttu-id="1400a-112">이 명령은 원본 컨트롤 VSTSNative에 대 한 id 08d6d266-27b6-463c-beea-bc48a67ace15를 사용 하 여 소스 제어 동기화 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="1400a-113">변수</span><span class="sxs-lookup"><span data-stu-id="1400a-113">PARAMETERS</span></span>

### <span data-ttu-id="1400a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1400a-114">-AutomationAccountName</span></span>
<span data-ttu-id="1400a-115">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-115">The automation account name.</span></span>

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

### <span data-ttu-id="1400a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1400a-116">-DefaultProfile</span></span>
<span data-ttu-id="1400a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1400a-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="1400a-118">-JobId</span></span>
<span data-ttu-id="1400a-119">소스 제어 동기화 작업 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1400a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1400a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1400a-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-121">The resource group name.</span></span>

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

### <span data-ttu-id="1400a-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="1400a-122">-SourceControlName</span></span>
<span data-ttu-id="1400a-123">작업의 원본 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="1400a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1400a-124">CommonParameters</span></span>
<span data-ttu-id="1400a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1400a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1400a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1400a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1400a-127">입력</span><span class="sxs-lookup"><span data-stu-id="1400a-127">INPUTS</span></span>

### <span data-ttu-id="1400a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1400a-128">System.String</span></span>

### <span data-ttu-id="1400a-129">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="1400a-129">System.Guid</span></span>

## <span data-ttu-id="1400a-130">출력</span><span class="sxs-lookup"><span data-stu-id="1400a-130">OUTPUTS</span></span>

### <span data-ttu-id="1400a-131">SourceControlSyncJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="1400a-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="1400a-132">SourceControlSyncJobRecord를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="1400a-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="1400a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="1400a-133">NOTES</span></span>

## <span data-ttu-id="1400a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1400a-134">RELATED LINKS</span></span>
