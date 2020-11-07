---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 8fe4c554fd781d198af6bea784a433c141c2d41d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703919"
---
# <span data-ttu-id="32f34-101">Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="32f34-101">Get-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="32f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f34-102">SYNOPSIS</span></span>
<span data-ttu-id="32f34-103">하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32f34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32f34-104">SYNTAX</span></span>

### <span data-ttu-id="32f34-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="32f34-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f34-106">ByName</span><span class="sxs-lookup"><span data-stu-id="32f34-106">ByName</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32f34-107">설명은</span><span class="sxs-lookup"><span data-stu-id="32f34-107">DESCRIPTION</span></span>
<span data-ttu-id="32f34-108">**AzureRmAutomationHybridWorkerGroup** Cmdlet은 Azure Automation 하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="32f34-109">특정 그룹을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="32f34-110">예제의</span><span class="sxs-lookup"><span data-stu-id="32f34-110">EXAMPLES</span></span>

### <span data-ttu-id="32f34-111">예제 1: 모든 하이브리드 runbook worker 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="32f34-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="32f34-112">이 명령은 Contoso17 이라는 Automation 계정의 모든 하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="32f34-113">예제 2: 단일 하이브리드 runbook worker 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="32f34-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="32f34-114">이 명령은 Contoso17 이라는 Automation 계정에서 HybridRunbookWorkerGroup01 이라는 하이브리드 runbook worker 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="32f34-115">예제 3: hybrid runbook worker 그룹에서 작업자 가져오기</span><span class="sxs-lookup"><span data-stu-id="32f34-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="32f34-116">이 명령은 Contoso17 이라는 Automation 계정의 HybridRunbookWorkerGroup01 이라는 하이브리드 runbook worker 그룹의 hybrid runbook worker를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="32f34-117">변수</span><span class="sxs-lookup"><span data-stu-id="32f34-117">PARAMETERS</span></span>

### <span data-ttu-id="32f34-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32f34-118">-AutomationAccountName</span></span>
<span data-ttu-id="32f34-119">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="32f34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f34-120">-DefaultProfile</span></span>
<span data-ttu-id="32f34-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32f34-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32f34-122">-이름</span><span class="sxs-lookup"><span data-stu-id="32f34-122">-Name</span></span>
<span data-ttu-id="32f34-123">하이브리드 runbook worker 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="32f34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f34-124">-ResourceGroupName</span></span>
<span data-ttu-id="32f34-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="32f34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f34-126">CommonParameters</span></span>
<span data-ttu-id="32f34-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32f34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f34-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f34-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f34-129">입력</span><span class="sxs-lookup"><span data-stu-id="32f34-129">INPUTS</span></span>

### <span data-ttu-id="32f34-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32f34-130">System.String</span></span>
<span data-ttu-id="32f34-131">매개 변수: Name (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32f34-131">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="32f34-132">출력</span><span class="sxs-lookup"><span data-stu-id="32f34-132">OUTPUTS</span></span>

### <span data-ttu-id="32f34-133">HybridRunbookWorkerGroup를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="32f34-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="32f34-134">상속자</span><span class="sxs-lookup"><span data-stu-id="32f34-134">NOTES</span></span>

## <span data-ttu-id="32f34-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32f34-135">RELATED LINKS</span></span>
