---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046071"
---
# <span data-ttu-id="9c5b2-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9c5b2-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="9c5b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c5b2-102">SYNOPSIS</span></span>

<span data-ttu-id="9c5b2-103">자동화 일정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="9c5b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c5b2-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c5b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c5b2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9c5b2-106">**Set-AzureAutomationSchedule** Cmdlet은 Microsoft Azure 자동화의 일정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="9c5b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9c5b2-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5b2-108">예제 1: 일정 수정</span><span class="sxs-lookup"><span data-stu-id="9c5b2-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="9c5b2-109">이 명령은 Schedule01 이라는 일정에 대 한 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="9c5b2-110">변수</span><span class="sxs-lookup"><span data-stu-id="9c5b2-110">PARAMETERS</span></span>

### <span data-ttu-id="9c5b2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9c5b2-111">-AutomationAccountName</span></span>
<span data-ttu-id="9c5b2-112">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="9c5b2-113">-설명</span><span class="sxs-lookup"><span data-stu-id="9c5b2-113">-Description</span></span>
<span data-ttu-id="9c5b2-114">일정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5b2-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="9c5b2-115">-IsEnabled</span></span>
<span data-ttu-id="9c5b2-116">일정을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5b2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9c5b2-117">-Name</span></span>
<span data-ttu-id="9c5b2-118">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="9c5b2-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="9c5b2-119">-Profile</span></span>
<span data-ttu-id="9c5b2-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c5b2-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c5b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5b2-122">CommonParameters</span></span>
<span data-ttu-id="9c5b2-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c5b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5b2-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5b2-125">입력</span><span class="sxs-lookup"><span data-stu-id="9c5b2-125">INPUTS</span></span>

## <span data-ttu-id="9c5b2-126">출력</span><span class="sxs-lookup"><span data-stu-id="9c5b2-126">OUTPUTS</span></span>

### <span data-ttu-id="9c5b2-127">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="9c5b2-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="9c5b2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9c5b2-128">NOTES</span></span>

## <span data-ttu-id="9c5b2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c5b2-129">RELATED LINKS</span></span>

[<span data-ttu-id="9c5b2-130">다운로드-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9c5b2-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="9c5b2-131">새-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9c5b2-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="9c5b2-132">-AzureAutomationSchedule 제거</span><span class="sxs-lookup"><span data-stu-id="9c5b2-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


