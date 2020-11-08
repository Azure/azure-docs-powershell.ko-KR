---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046032"
---
# <span data-ttu-id="65ea2-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65ea2-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="65ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ea2-102">SYNOPSIS</span></span>

<span data-ttu-id="65ea2-103">Runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-103">Starts a runbook job.</span></span>

## <span data-ttu-id="65ea2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65ea2-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65ea2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65ea2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="65ea2-106">**시작-AzureAutomationRunbook** Cmdlet은 Microsoft Azure Automation runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="65ea2-107">Runbook의 ID 또는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="65ea2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="65ea2-108">EXAMPLES</span></span>

### <span data-ttu-id="65ea2-109">예제 1: runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="65ea2-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="65ea2-110">이 명령은 Contoso17 이라는 Automation 계정에서 Runbk01 라는 runbook에 대 한 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="65ea2-111">변수</span><span class="sxs-lookup"><span data-stu-id="65ea2-111">PARAMETERS</span></span>

### <span data-ttu-id="65ea2-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65ea2-112">-AutomationAccountName</span></span>
<span data-ttu-id="65ea2-113">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="65ea2-114">-이름</span><span class="sxs-lookup"><span data-stu-id="65ea2-114">-Name</span></span>
<span data-ttu-id="65ea2-115">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ea2-116">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="65ea2-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ea2-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="65ea2-117">-Profile</span></span>
<span data-ttu-id="65ea2-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65ea2-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65ea2-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="65ea2-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ea2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ea2-121">CommonParameters</span></span>
<span data-ttu-id="65ea2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ea2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ea2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ea2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ea2-124">입력</span><span class="sxs-lookup"><span data-stu-id="65ea2-124">INPUTS</span></span>

## <span data-ttu-id="65ea2-125">출력</span><span class="sxs-lookup"><span data-stu-id="65ea2-125">OUTPUTS</span></span>

### <span data-ttu-id="65ea2-126">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="65ea2-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="65ea2-127">상속자</span><span class="sxs-lookup"><span data-stu-id="65ea2-127">NOTES</span></span>

## <span data-ttu-id="65ea2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65ea2-128">RELATED LINKS</span></span>

[<span data-ttu-id="65ea2-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65ea2-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="65ea2-130">새-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65ea2-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="65ea2-131">게시-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65ea2-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="65ea2-132">-AzureAutomationRunbook 제거</span><span class="sxs-lookup"><span data-stu-id="65ea2-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="65ea2-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65ea2-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


