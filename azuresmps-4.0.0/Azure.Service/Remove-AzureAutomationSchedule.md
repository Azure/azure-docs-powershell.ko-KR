---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046170"
---
# <span data-ttu-id="f4af0-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4af0-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="f4af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4af0-102">SYNOPSIS</span></span>

<span data-ttu-id="f4af0-103">Azure Automation 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="f4af0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4af0-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4af0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f4af0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f4af0-106">**-AzureAutomationSchedule** Cmdlet은 Microsoft Azure 자동화에서 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="f4af0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f4af0-107">EXAMPLES</span></span>

### <span data-ttu-id="f4af0-108">예제 1: 일정 제거</span><span class="sxs-lookup"><span data-stu-id="f4af0-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="f4af0-109">이 명령은 MySchedule 이라는 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="f4af0-110">변수</span><span class="sxs-lookup"><span data-stu-id="f4af0-110">PARAMETERS</span></span>

### <span data-ttu-id="f4af0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4af0-111">-AutomationAccountName</span></span>
<span data-ttu-id="f4af0-112">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="f4af0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f4af0-113">-Force</span></span>
<span data-ttu-id="f4af0-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4af0-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f4af0-115">-Name</span></span>
<span data-ttu-id="f4af0-116">제거할 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="f4af0-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="f4af0-117">-Profile</span></span>
<span data-ttu-id="f4af0-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4af0-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4af0-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f4af0-120">-Confirm</span></span>
<span data-ttu-id="f4af0-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4af0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4af0-122">-WhatIf</span></span>
<span data-ttu-id="f4af0-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4af0-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4af0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4af0-125">CommonParameters</span></span>
<span data-ttu-id="f4af0-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4af0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4af0-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4af0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4af0-128">입력</span><span class="sxs-lookup"><span data-stu-id="f4af0-128">INPUTS</span></span>

## <span data-ttu-id="f4af0-129">출력</span><span class="sxs-lookup"><span data-stu-id="f4af0-129">OUTPUTS</span></span>

## <span data-ttu-id="f4af0-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f4af0-130">NOTES</span></span>

## <span data-ttu-id="f4af0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4af0-131">RELATED LINKS</span></span>

[<span data-ttu-id="f4af0-132">다운로드-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4af0-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="f4af0-133">새-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4af0-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="f4af0-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f4af0-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


