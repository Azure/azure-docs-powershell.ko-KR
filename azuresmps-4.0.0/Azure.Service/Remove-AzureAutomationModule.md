---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046481"
---
# <span data-ttu-id="985c3-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="985c3-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="985c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985c3-102">SYNOPSIS</span></span>

<span data-ttu-id="985c3-103">자동화에서 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="985c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="985c3-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="985c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="985c3-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="985c3-106">**제거-AzureAutomationModule** Cmdlet은 Microsoft Azure 자동화에서 automation 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="985c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="985c3-107">EXAMPLES</span></span>

### <span data-ttu-id="985c3-108">예제 1: 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="985c3-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="985c3-109">이 명령은 Contoso17 이라는 자동화 계정에서 ContosoModule 이라는 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="985c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="985c3-110">PARAMETERS</span></span>

### <span data-ttu-id="985c3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="985c3-111">-AutomationAccountName</span></span>
<span data-ttu-id="985c3-112">모듈과 함께 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="985c3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="985c3-113">-Force</span></span>
<span data-ttu-id="985c3-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="985c3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="985c3-115">-Name</span></span>
<span data-ttu-id="985c3-116">제거할 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="985c3-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="985c3-117">-Profile</span></span>
<span data-ttu-id="985c3-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="985c3-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="985c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985c3-120">CommonParameters</span></span>
<span data-ttu-id="985c3-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="985c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985c3-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="985c3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985c3-123">입력</span><span class="sxs-lookup"><span data-stu-id="985c3-123">INPUTS</span></span>

## <span data-ttu-id="985c3-124">출력</span><span class="sxs-lookup"><span data-stu-id="985c3-124">OUTPUTS</span></span>

## <span data-ttu-id="985c3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="985c3-125">NOTES</span></span>

## <span data-ttu-id="985c3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="985c3-126">RELATED LINKS</span></span>

[<span data-ttu-id="985c3-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="985c3-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="985c3-128">새-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="985c3-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="985c3-129">Set AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="985c3-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


