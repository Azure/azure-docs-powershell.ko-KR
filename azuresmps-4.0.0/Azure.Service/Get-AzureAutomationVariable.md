---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045653"
---
# <span data-ttu-id="e3048-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e3048-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="e3048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3048-102">SYNOPSIS</span></span>

<span data-ttu-id="e3048-103">자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="e3048-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3048-104">SYNTAX</span></span>

### <span data-ttu-id="e3048-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3048-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e3048-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e3048-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3048-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e3048-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e3048-108">**Get-AzureAutomationVariable** cmdlet은 하나 이상의 Microsoft Azure 자동화 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="e3048-109">기본적으로 모든 변수가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-109">By default, all variables are returned.</span></span>
<span data-ttu-id="e3048-110">특정 변수를 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="e3048-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e3048-111">EXAMPLES</span></span>

### <span data-ttu-id="e3048-112">예제 1: 변수 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3048-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="e3048-113">이러한 명령은 MyVariable 이라는 자동화 변수를 가져오고 해당 값을 $value 이라는 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="e3048-114">변수</span><span class="sxs-lookup"><span data-stu-id="e3048-114">PARAMETERS</span></span>

### <span data-ttu-id="e3048-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3048-115">-AutomationAccountName</span></span>
<span data-ttu-id="e3048-116">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="e3048-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e3048-117">-Name</span></span>
<span data-ttu-id="e3048-118">변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3048-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="e3048-119">-Profile</span></span>
<span data-ttu-id="e3048-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3048-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3048-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3048-122">CommonParameters</span></span>
<span data-ttu-id="e3048-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3048-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3048-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3048-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3048-125">입력</span><span class="sxs-lookup"><span data-stu-id="e3048-125">INPUTS</span></span>

## <span data-ttu-id="e3048-126">출력</span><span class="sxs-lookup"><span data-stu-id="e3048-126">OUTPUTS</span></span>

### <span data-ttu-id="e3048-127">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="e3048-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="e3048-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e3048-128">NOTES</span></span>

## <span data-ttu-id="e3048-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3048-129">RELATED LINKS</span></span>

[<span data-ttu-id="e3048-130">새-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e3048-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="e3048-131">-AzureAutomationVariable 제거</span><span class="sxs-lookup"><span data-stu-id="e3048-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="e3048-132">Set AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e3048-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


