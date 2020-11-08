---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045657"
---
# <span data-ttu-id="8d18d-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d18d-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="8d18d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d18d-102">SYNOPSIS</span></span>

<span data-ttu-id="8d18d-103">Runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-103">Gets a runbook.</span></span>

## <span data-ttu-id="8d18d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d18d-104">SYNTAX</span></span>

### <span data-ttu-id="8d18d-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d18d-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8d18d-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="8d18d-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d18d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d18d-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8d18d-108">**Get-AzureAutomationRunbook** cmdlet은 하나 이상의 Microsoft Azure 자동화 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="8d18d-109">기본적으로 모든 runbook이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="8d18d-110">특정 runbook을 가져오려면 해당 이름 또는 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="8d18d-111">특정 일정에 연결 된 모든 runbook을 가져오려면 일정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="8d18d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8d18d-112">EXAMPLES</span></span>

### <span data-ttu-id="8d18d-113">예제 1: 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d18d-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8d18d-114">이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8d18d-115">변수</span><span class="sxs-lookup"><span data-stu-id="8d18d-115">PARAMETERS</span></span>

### <span data-ttu-id="8d18d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8d18d-116">-AutomationAccountName</span></span>
<span data-ttu-id="8d18d-117">Azure Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-117">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d18d-118">-이름</span><span class="sxs-lookup"><span data-stu-id="8d18d-118">-Name</span></span>
<span data-ttu-id="8d18d-119">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d18d-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="8d18d-120">-Profile</span></span>
<span data-ttu-id="8d18d-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d18d-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d18d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d18d-123">CommonParameters</span></span>
<span data-ttu-id="8d18d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d18d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d18d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d18d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d18d-126">입력</span><span class="sxs-lookup"><span data-stu-id="8d18d-126">INPUTS</span></span>

## <span data-ttu-id="8d18d-127">출력</span><span class="sxs-lookup"><span data-stu-id="8d18d-127">OUTPUTS</span></span>

### <span data-ttu-id="8d18d-128">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="8d18d-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="8d18d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8d18d-129">NOTES</span></span>

## <span data-ttu-id="8d18d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d18d-130">RELATED LINKS</span></span>

[<span data-ttu-id="8d18d-131">새-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d18d-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="8d18d-132">게시-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d18d-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="8d18d-133">-AzureAutomationRunbook 제거</span><span class="sxs-lookup"><span data-stu-id="8d18d-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="8d18d-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d18d-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="8d18d-135">시작-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d18d-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


