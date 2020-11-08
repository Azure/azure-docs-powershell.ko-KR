---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045931"
---
# <span data-ttu-id="f70ae-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f70ae-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="f70ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f70ae-102">SYNOPSIS</span></span>

<span data-ttu-id="f70ae-103">자동화 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="f70ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f70ae-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f70ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f70ae-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f70ae-106">**새-AzureAutomationVariable** Cmdlet은 Microsoft Azure 자동화에 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="f70ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f70ae-107">EXAMPLES</span></span>

### <span data-ttu-id="f70ae-108">예제 1: 간단한 값을 사용 하 여 새 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="f70ae-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="f70ae-109">이 명령은 Contoso17 이라는 Azure Automation 계정에 문자열 값이 포함 된 MyStringVariable 이라는 새 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f70ae-110">예제 2: 복잡 한 값을 사용 하 여 새 변수 만들기</span><span class="sxs-lookup"><span data-stu-id="f70ae-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="f70ae-111">이러한 명령은 Contoso17 이라는 자동화 계정에 MyComplexVariable 이라는 새 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f70ae-112">복합 개체는 해당 값 (이 경우 가상 컴퓨터 개체)에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="f70ae-113">변수</span><span class="sxs-lookup"><span data-stu-id="f70ae-113">PARAMETERS</span></span>

### <span data-ttu-id="f70ae-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f70ae-114">-AutomationAccountName</span></span>
<span data-ttu-id="f70ae-115">변수가 저장 될 자동화 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

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

### <span data-ttu-id="f70ae-116">-설명</span><span class="sxs-lookup"><span data-stu-id="f70ae-116">-Description</span></span>
<span data-ttu-id="f70ae-117">변수에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-117">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="f70ae-118">암호화 된</span><span class="sxs-lookup"><span data-stu-id="f70ae-118">-Encrypted</span></span>
<span data-ttu-id="f70ae-119">변수 값을 암호화 된 상태로 저장 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70ae-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f70ae-120">-Name</span></span>
<span data-ttu-id="f70ae-121">변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-121">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="f70ae-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="f70ae-122">-Profile</span></span>
<span data-ttu-id="f70ae-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f70ae-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f70ae-125">-값</span><span class="sxs-lookup"><span data-stu-id="f70ae-125">-Value</span></span>
<span data-ttu-id="f70ae-126">변수에 저장할 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70ae-127">CommonParameters</span></span>
<span data-ttu-id="f70ae-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f70ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70ae-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f70ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70ae-130">입력</span><span class="sxs-lookup"><span data-stu-id="f70ae-130">INPUTS</span></span>

## <span data-ttu-id="f70ae-131">출력</span><span class="sxs-lookup"><span data-stu-id="f70ae-131">OUTPUTS</span></span>

### <span data-ttu-id="f70ae-132">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="f70ae-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f70ae-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f70ae-133">NOTES</span></span>

## <span data-ttu-id="f70ae-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f70ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="f70ae-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f70ae-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="f70ae-136">-AzureAutomationVariable 제거</span><span class="sxs-lookup"><span data-stu-id="f70ae-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="f70ae-137">Set AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f70ae-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


