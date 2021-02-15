---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182084"
---
# <span data-ttu-id="773fa-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="773fa-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="773fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="773fa-102">SYNOPSIS</span></span>
<span data-ttu-id="773fa-103">Azure Automation 원본 제어 동기화 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="773fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="773fa-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="773fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="773fa-105">DESCRIPTION</span></span>
<span data-ttu-id="773fa-106">이 Start-AzAutomationSourceControlSyncJob cmdlet은 주어진 소스 제어 이름에 대한 Azure Automation 소스 제어 동기화 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="773fa-107">예제</span><span class="sxs-lookup"><span data-stu-id="773fa-107">EXAMPLES</span></span>

### <span data-ttu-id="773fa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="773fa-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="773fa-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="773fa-109">PARAMETERS</span></span>

### <span data-ttu-id="773fa-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="773fa-110">-AutomationAccountName</span></span>
<span data-ttu-id="773fa-111">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-111">The automation account name.</span></span>

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

### <span data-ttu-id="773fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773fa-112">-DefaultProfile</span></span>
<span data-ttu-id="773fa-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773fa-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="773fa-114">-JobId</span></span>
<span data-ttu-id="773fa-115">원본 제어 동기화 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773fa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="773fa-116">-ResourceGroupName</span></span>
<span data-ttu-id="773fa-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-117">The resource group name.</span></span>

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

### <span data-ttu-id="773fa-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="773fa-118">-SourceControlName</span></span>
<span data-ttu-id="773fa-119">원본 제어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-119">The source control name.</span></span>

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

### <span data-ttu-id="773fa-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="773fa-120">-Confirm</span></span>
<span data-ttu-id="773fa-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="773fa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="773fa-122">-WhatIf</span></span>
<span data-ttu-id="773fa-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="773fa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="773fa-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773fa-125">CommonParameters</span></span>
<span data-ttu-id="773fa-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="773fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773fa-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="773fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773fa-128">입력</span><span class="sxs-lookup"><span data-stu-id="773fa-128">INPUTS</span></span>

### <span data-ttu-id="773fa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="773fa-129">System.String</span></span>

## <span data-ttu-id="773fa-130">출력</span><span class="sxs-lookup"><span data-stu-id="773fa-130">OUTPUTS</span></span>

### <span data-ttu-id="773fa-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="773fa-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="773fa-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="773fa-132">NOTES</span></span>

## <span data-ttu-id="773fa-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="773fa-133">RELATED LINKS</span></span>
