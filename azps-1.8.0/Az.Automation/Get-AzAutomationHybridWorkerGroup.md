---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 7481975d880d3d43508756ac2daec3e665878ee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701614"
---
# <span data-ttu-id="78c28-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="78c28-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="78c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c28-102">SYNOPSIS</span></span>
<span data-ttu-id="78c28-103">하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="78c28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78c28-104">SYNTAX</span></span>

### <span data-ttu-id="78c28-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="78c28-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c28-106">ByName</span><span class="sxs-lookup"><span data-stu-id="78c28-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c28-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78c28-107">DESCRIPTION</span></span>
<span data-ttu-id="78c28-108">**AzAutomationHybridWorkerGroup** Cmdlet은 Azure Automation 하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="78c28-109">특정 그룹을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="78c28-110">예제의</span><span class="sxs-lookup"><span data-stu-id="78c28-110">EXAMPLES</span></span>

### <span data-ttu-id="78c28-111">예제 1: 모든 하이브리드 runbook worker 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="78c28-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="78c28-112">이 명령은 Contoso17 이라는 Automation 계정의 모든 하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78c28-113">예제 2: 단일 하이브리드 runbook worker 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="78c28-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="78c28-114">이 명령은 Contoso17 이라는 Automation 계정에서 HybridRunbookWorkerGroup01 이라는 하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78c28-115">예제 3: hybrid runbook worker 그룹에서 작업자 가져오기</span><span class="sxs-lookup"><span data-stu-id="78c28-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="78c28-116">이 명령은 Contoso17 이라는 Automation 계정의 HybridRunbookWorkerGroup01 이라는 하이브리드 runbook worker 그룹의 hybrid runbook worker를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="78c28-117">변수</span><span class="sxs-lookup"><span data-stu-id="78c28-117">PARAMETERS</span></span>

### <span data-ttu-id="78c28-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78c28-118">-AutomationAccountName</span></span>
<span data-ttu-id="78c28-119">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="78c28-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c28-120">-DefaultProfile</span></span>
<span data-ttu-id="78c28-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78c28-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78c28-122">-이름</span><span class="sxs-lookup"><span data-stu-id="78c28-122">-Name</span></span>
<span data-ttu-id="78c28-123">하이브리드 runbook worker 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="78c28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c28-124">-ResourceGroupName</span></span>
<span data-ttu-id="78c28-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78c28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c28-126">CommonParameters</span></span>
<span data-ttu-id="78c28-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c28-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c28-129">입력</span><span class="sxs-lookup"><span data-stu-id="78c28-129">INPUTS</span></span>

### <span data-ttu-id="78c28-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78c28-130">System.String</span></span>

## <span data-ttu-id="78c28-131">출력</span><span class="sxs-lookup"><span data-stu-id="78c28-131">OUTPUTS</span></span>

### <span data-ttu-id="78c28-132">HybridRunbookWorkerGroup를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="78c28-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="78c28-133">상속자</span><span class="sxs-lookup"><span data-stu-id="78c28-133">NOTES</span></span>

## <span data-ttu-id="78c28-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78c28-134">RELATED LINKS</span></span>
