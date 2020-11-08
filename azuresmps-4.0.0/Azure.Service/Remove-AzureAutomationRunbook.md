---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046171"
---
# <span data-ttu-id="c590c-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c590c-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="c590c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c590c-102">SYNOPSIS</span></span>

<span data-ttu-id="c590c-103">Runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-103">Removes a runbook.</span></span>

## <span data-ttu-id="c590c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c590c-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c590c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c590c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c590c-106">**-AzureAutomationRunbook** Cmdlet은 Microsoft Azure 자동화에서 runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="c590c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c590c-107">EXAMPLES</span></span>

### <span data-ttu-id="c590c-108">예제 1: runbook 제거</span><span class="sxs-lookup"><span data-stu-id="c590c-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="c590c-109">이 명령은 Contoso17 이라는 자동화 계정에서 MyRunbook 이라는 이름의 runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c590c-110">변수</span><span class="sxs-lookup"><span data-stu-id="c590c-110">PARAMETERS</span></span>

### <span data-ttu-id="c590c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c590c-111">-AutomationAccountName</span></span>
<span data-ttu-id="c590c-112">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="c590c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c590c-113">-Force</span></span>
<span data-ttu-id="c590c-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c590c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c590c-115">-Name</span></span>
<span data-ttu-id="c590c-116">제거할 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-116">Specifies the name of the runbook to remove.</span></span>

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

### <span data-ttu-id="c590c-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="c590c-117">-Profile</span></span>
<span data-ttu-id="c590c-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c590c-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c590c-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c590c-120">-Confirm</span></span>
<span data-ttu-id="c590c-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c590c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c590c-122">-WhatIf</span></span>
<span data-ttu-id="c590c-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c590c-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c590c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c590c-125">CommonParameters</span></span>
<span data-ttu-id="c590c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c590c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c590c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c590c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c590c-128">입력</span><span class="sxs-lookup"><span data-stu-id="c590c-128">INPUTS</span></span>

## <span data-ttu-id="c590c-129">출력</span><span class="sxs-lookup"><span data-stu-id="c590c-129">OUTPUTS</span></span>

## <span data-ttu-id="c590c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c590c-130">NOTES</span></span>

## <span data-ttu-id="c590c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c590c-131">RELATED LINKS</span></span>

[<span data-ttu-id="c590c-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c590c-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="c590c-133">새-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c590c-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="c590c-134">게시-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c590c-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="c590c-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c590c-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="c590c-136">시작-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c590c-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


