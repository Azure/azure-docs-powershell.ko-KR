---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046169"
---
# <span data-ttu-id="22652-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="22652-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="22652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22652-102">SYNOPSIS</span></span>

<span data-ttu-id="22652-103">자동화 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="22652-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22652-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22652-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22652-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="22652-106">**제거-AzureAutomationVariable** Cmdlet은 Microsoft Azure 자동화에서 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="22652-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22652-107">EXAMPLES</span></span>

### <span data-ttu-id="22652-108">예제 1: 변수 제거</span><span class="sxs-lookup"><span data-stu-id="22652-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="22652-109">이 명령은 사용자 유효성 검사를 요청 하지 않고 Contoso17 이라는 이름 MyStringVariable 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="22652-110">변수</span><span class="sxs-lookup"><span data-stu-id="22652-110">PARAMETERS</span></span>

### <span data-ttu-id="22652-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22652-111">-AutomationAccountName</span></span>
<span data-ttu-id="22652-112">변수를 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="22652-113">-Force</span><span class="sxs-lookup"><span data-stu-id="22652-113">-Force</span></span>
<span data-ttu-id="22652-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22652-115">-이름</span><span class="sxs-lookup"><span data-stu-id="22652-115">-Name</span></span>
<span data-ttu-id="22652-116">변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="22652-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="22652-117">-Profile</span></span>
<span data-ttu-id="22652-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22652-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="22652-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22652-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22652-120">CommonParameters</span></span>
<span data-ttu-id="22652-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22652-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22652-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22652-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22652-123">입력</span><span class="sxs-lookup"><span data-stu-id="22652-123">INPUTS</span></span>

## <span data-ttu-id="22652-124">출력</span><span class="sxs-lookup"><span data-stu-id="22652-124">OUTPUTS</span></span>

## <span data-ttu-id="22652-125">상속자</span><span class="sxs-lookup"><span data-stu-id="22652-125">NOTES</span></span>

## <span data-ttu-id="22652-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22652-126">RELATED LINKS</span></span>

[<span data-ttu-id="22652-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="22652-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="22652-128">새-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="22652-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="22652-129">Set AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="22652-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


