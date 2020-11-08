---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045655"
---
# <span data-ttu-id="d7eee-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d7eee-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="d7eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7eee-102">SYNOPSIS</span></span>

<span data-ttu-id="d7eee-103">Azure Automation 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="d7eee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7eee-104">SYNTAX</span></span>

### <span data-ttu-id="d7eee-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7eee-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d7eee-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d7eee-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7eee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d7eee-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d7eee-108">**Get-AzureAutomationSchedule** Cmdlet은 Microsoft Azure Automation 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="d7eee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d7eee-109">EXAMPLES</span></span>

### <span data-ttu-id="d7eee-110">예제 1: 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="d7eee-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="d7eee-111">이 명령은 DailySchedule08 라는 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="d7eee-112">변수</span><span class="sxs-lookup"><span data-stu-id="d7eee-112">PARAMETERS</span></span>

### <span data-ttu-id="d7eee-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d7eee-113">-AutomationAccountName</span></span>
<span data-ttu-id="d7eee-114">Azure Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="d7eee-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d7eee-115">-Name</span></span>
<span data-ttu-id="d7eee-116">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eee-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="d7eee-117">-Profile</span></span>
<span data-ttu-id="d7eee-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7eee-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7eee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7eee-120">CommonParameters</span></span>
<span data-ttu-id="d7eee-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7eee-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7eee-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7eee-123">입력</span><span class="sxs-lookup"><span data-stu-id="d7eee-123">INPUTS</span></span>

## <span data-ttu-id="d7eee-124">출력</span><span class="sxs-lookup"><span data-stu-id="d7eee-124">OUTPUTS</span></span>

### <span data-ttu-id="d7eee-125">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="d7eee-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="d7eee-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d7eee-126">NOTES</span></span>

## <span data-ttu-id="d7eee-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7eee-127">RELATED LINKS</span></span>

[<span data-ttu-id="d7eee-128">새-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d7eee-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="d7eee-129">-AzureAutomationSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="d7eee-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="d7eee-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d7eee-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


