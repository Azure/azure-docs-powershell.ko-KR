---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 89c1b96744ce67765bed53f850e21a457ead4b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996977"
---
# <span data-ttu-id="a7909-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a7909-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="a7909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7909-102">SYNOPSIS</span></span>
<span data-ttu-id="a7909-103">하이브리드 Runbook worker 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="a7909-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7909-104">SYNTAX</span></span>

### <span data-ttu-id="a7909-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="a7909-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7909-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a7909-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7909-107">설명</span><span class="sxs-lookup"><span data-stu-id="a7909-107">DESCRIPTION</span></span>
<span data-ttu-id="a7909-108">**Get-AzAutomationHybridWorkerGroup** cmdlet은 Azure Automation 하이브리드 Runbook worker 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="a7909-109">특정 그룹을 얻지 못하도록 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="a7909-110">예제</span><span class="sxs-lookup"><span data-stu-id="a7909-110">EXAMPLES</span></span>

### <span data-ttu-id="a7909-111">예제 1: 모든 하이브리드 Runbook Worker 그룹 다운로드</span><span class="sxs-lookup"><span data-stu-id="a7909-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a7909-112">이 명령은 Contoso17이라는 Automation 계정의 모든 하이브리드 Runbook worker 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a7909-113">예제 2: 단일 하이브리드 Runbook Worker 그룹 다운로드</span><span class="sxs-lookup"><span data-stu-id="a7909-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="a7909-114">이 명령은 Contoso17이라는 Automation 계정에서 HybridRunbookWorkerGroup01이라는 하이브리드 Runbook Worker 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a7909-115">예제 3: 하이브리드 Runbook 작업자 그룹에서 작업자를 얻게 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="a7909-116">이 명령은 Contoso17이라는 Automation 계정에서 HybridRunbookWorkerGroup01이라는 하이브리드 Runbook 작업자 그룹에서 하이브리드 Runbook 작업자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a7909-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7909-117">PARAMETERS</span></span>

### <span data-ttu-id="a7909-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7909-118">-AutomationAccountName</span></span>
<span data-ttu-id="a7909-119">Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="a7909-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7909-120">-DefaultProfile</span></span>
<span data-ttu-id="a7909-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a7909-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7909-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a7909-122">-Name</span></span>
<span data-ttu-id="a7909-123">하이브리드 Runbook Worker 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7909-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7909-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7909-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a7909-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7909-126">CommonParameters</span></span>
<span data-ttu-id="a7909-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7909-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7909-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a7909-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7909-129">입력</span><span class="sxs-lookup"><span data-stu-id="a7909-129">INPUTS</span></span>

### <span data-ttu-id="a7909-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a7909-130">System.String</span></span>

## <span data-ttu-id="a7909-131">출력</span><span class="sxs-lookup"><span data-stu-id="a7909-131">OUTPUTS</span></span>

### <span data-ttu-id="a7909-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a7909-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="a7909-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7909-133">NOTES</span></span>

## <span data-ttu-id="a7909-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7909-134">RELATED LINKS</span></span>
