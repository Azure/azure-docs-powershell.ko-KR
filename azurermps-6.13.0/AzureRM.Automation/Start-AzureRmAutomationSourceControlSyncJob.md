---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524608"
---
# <span data-ttu-id="8fdd3-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="8fdd3-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="8fdd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fdd3-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdd3-103">Azure Automation 소스 제어 동기화 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fdd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8fdd3-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8fdd3-105">DESCRIPTION</span></span>
<span data-ttu-id="8fdd3-106">Start-AzureRmAutomationSourceControlSyncJob cmdlet은 지정 된 소스 컨트롤 이름에 대 한 Azure 자동화 원본 control 동기화 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="8fdd3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8fdd3-107">EXAMPLES</span></span>

### <span data-ttu-id="8fdd3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fdd3-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="8fdd3-109">변수</span><span class="sxs-lookup"><span data-stu-id="8fdd3-109">PARAMETERS</span></span>

### <span data-ttu-id="8fdd3-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8fdd3-110">-AutomationAccountName</span></span>
<span data-ttu-id="8fdd3-111">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-111">The automation account name.</span></span>

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

### <span data-ttu-id="8fdd3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdd3-112">-DefaultProfile</span></span>
<span data-ttu-id="8fdd3-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdd3-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="8fdd3-114">-JobId</span></span>
<span data-ttu-id="8fdd3-115">소스 제어 동기화 작업 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="8fdd3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fdd3-116">-ResourceGroupName</span></span>
<span data-ttu-id="8fdd3-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-117">The resource group name.</span></span>

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

### <span data-ttu-id="8fdd3-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="8fdd3-118">-SourceControlName</span></span>
<span data-ttu-id="8fdd3-119">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-119">The source control name.</span></span>

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

### <span data-ttu-id="8fdd3-120">-확인</span><span class="sxs-lookup"><span data-stu-id="8fdd3-120">-Confirm</span></span>
<span data-ttu-id="8fdd3-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fdd3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdd3-122">-WhatIf</span></span>
<span data-ttu-id="8fdd3-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fdd3-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fdd3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdd3-125">CommonParameters</span></span>
<span data-ttu-id="8fdd3-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdd3-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdd3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdd3-128">입력</span><span class="sxs-lookup"><span data-stu-id="8fdd3-128">INPUTS</span></span>

### <span data-ttu-id="8fdd3-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8fdd3-129">System.String</span></span>

## <span data-ttu-id="8fdd3-130">출력</span><span class="sxs-lookup"><span data-stu-id="8fdd3-130">OUTPUTS</span></span>

### <span data-ttu-id="8fdd3-131">SourceControlSyncJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="8fdd3-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="8fdd3-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8fdd3-132">NOTES</span></span>

## <span data-ttu-id="8fdd3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fdd3-133">RELATED LINKS</span></span>
