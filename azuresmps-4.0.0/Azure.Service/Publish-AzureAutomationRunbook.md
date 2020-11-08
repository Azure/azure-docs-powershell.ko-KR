---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045885"
---
# <span data-ttu-id="69d30-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="69d30-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="69d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69d30-102">SYNOPSIS</span></span>

<span data-ttu-id="69d30-103">Runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-103">Publishes a runbook.</span></span>

## <span data-ttu-id="69d30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69d30-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="69d30-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69d30-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="69d30-106">**게시-AzureAutomationRunbook** Cmdlet은 Microsoft Azure Automation의 프로덕션 환경에서 사용할 runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="69d30-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69d30-107">EXAMPLES</span></span>

### <span data-ttu-id="69d30-108">예제 1: runbook 게시</span><span class="sxs-lookup"><span data-stu-id="69d30-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="69d30-109">이 명령은 Contoso17 이라는 Automation 계정에 Runbk01 라는 runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="69d30-110">변수</span><span class="sxs-lookup"><span data-stu-id="69d30-110">PARAMETERS</span></span>

### <span data-ttu-id="69d30-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="69d30-111">-AutomationAccountName</span></span>
<span data-ttu-id="69d30-112">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="69d30-113">-이름</span><span class="sxs-lookup"><span data-stu-id="69d30-113">-Name</span></span>
<span data-ttu-id="69d30-114">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-114">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="69d30-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="69d30-115">-Profile</span></span>
<span data-ttu-id="69d30-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69d30-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69d30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d30-118">CommonParameters</span></span>
<span data-ttu-id="69d30-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d30-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d30-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d30-121">입력</span><span class="sxs-lookup"><span data-stu-id="69d30-121">INPUTS</span></span>

## <span data-ttu-id="69d30-122">출력</span><span class="sxs-lookup"><span data-stu-id="69d30-122">OUTPUTS</span></span>

## <span data-ttu-id="69d30-123">상속자</span><span class="sxs-lookup"><span data-stu-id="69d30-123">NOTES</span></span>

## <span data-ttu-id="69d30-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69d30-124">RELATED LINKS</span></span>

[<span data-ttu-id="69d30-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="69d30-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="69d30-126">새-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="69d30-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="69d30-127">-AzureAutomationRunbook 제거</span><span class="sxs-lookup"><span data-stu-id="69d30-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="69d30-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="69d30-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="69d30-129">시작-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="69d30-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


