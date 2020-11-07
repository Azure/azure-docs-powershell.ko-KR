---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 61e63d2b3c66c17ce32d8b4c7346adba5879f7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697719"
---
# <span data-ttu-id="0343c-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="0343c-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="0343c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0343c-102">SYNOPSIS</span></span>
<span data-ttu-id="0343c-103">Azure Automation 소스 제어 동기화 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="0343c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0343c-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0343c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0343c-105">DESCRIPTION</span></span>
<span data-ttu-id="0343c-106">Start-AzAutomationSourceControlSyncJob cmdlet은 지정 된 소스 제어 이름에 대 한 Azure Automation 소스 제어 동기화 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="0343c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0343c-107">EXAMPLES</span></span>

### <span data-ttu-id="0343c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0343c-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="0343c-109">변수</span><span class="sxs-lookup"><span data-stu-id="0343c-109">PARAMETERS</span></span>

### <span data-ttu-id="0343c-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0343c-110">-AutomationAccountName</span></span>
<span data-ttu-id="0343c-111">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-111">The automation account name.</span></span>

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

### <span data-ttu-id="0343c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0343c-112">-DefaultProfile</span></span>
<span data-ttu-id="0343c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0343c-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="0343c-114">-JobId</span></span>
<span data-ttu-id="0343c-115">소스 제어 동기화 작업 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="0343c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0343c-116">-ResourceGroupName</span></span>
<span data-ttu-id="0343c-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-117">The resource group name.</span></span>

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

### <span data-ttu-id="0343c-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="0343c-118">-SourceControlName</span></span>
<span data-ttu-id="0343c-119">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-119">The source control name.</span></span>

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

### <span data-ttu-id="0343c-120">-확인</span><span class="sxs-lookup"><span data-stu-id="0343c-120">-Confirm</span></span>
<span data-ttu-id="0343c-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0343c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0343c-122">-WhatIf</span></span>
<span data-ttu-id="0343c-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0343c-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0343c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0343c-125">CommonParameters</span></span>
<span data-ttu-id="0343c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0343c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0343c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0343c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0343c-128">입력</span><span class="sxs-lookup"><span data-stu-id="0343c-128">INPUTS</span></span>

### <span data-ttu-id="0343c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0343c-129">System.String</span></span>

## <span data-ttu-id="0343c-130">출력</span><span class="sxs-lookup"><span data-stu-id="0343c-130">OUTPUTS</span></span>

### <span data-ttu-id="0343c-131">SourceControlSyncJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="0343c-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="0343c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0343c-132">NOTES</span></span>

## <span data-ttu-id="0343c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0343c-133">RELATED LINKS</span></span>
