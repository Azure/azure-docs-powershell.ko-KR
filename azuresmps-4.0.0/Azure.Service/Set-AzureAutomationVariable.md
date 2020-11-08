---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046068"
---
# <span data-ttu-id="490bf-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="490bf-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="490bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="490bf-102">SYNOPSIS</span></span>

<span data-ttu-id="490bf-103">자동화 변수를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="490bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="490bf-104">SYNTAX</span></span>

### <span data-ttu-id="490bf-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="490bf-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="490bf-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="490bf-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="490bf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="490bf-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="490bf-108">**Set-AzureAutomationVariable** Cmdlet은 Microsoft Azure Automation의 변수 값 또는 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="490bf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="490bf-109">EXAMPLES</span></span>

### <span data-ttu-id="490bf-110">예제 1: 변수 값 설정</span><span class="sxs-lookup"><span data-stu-id="490bf-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="490bf-111">이 명령은 Contoso17 이라는 Azure Automation 계정에서 MyStringVariable 변수의 새 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="490bf-112">변수</span><span class="sxs-lookup"><span data-stu-id="490bf-112">PARAMETERS</span></span>

### <span data-ttu-id="490bf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="490bf-113">-AutomationAccountName</span></span>
<span data-ttu-id="490bf-114">변수를 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="490bf-115">-설명</span><span class="sxs-lookup"><span data-stu-id="490bf-115">-Description</span></span>
<span data-ttu-id="490bf-116">변수에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-117">암호화 된</span><span class="sxs-lookup"><span data-stu-id="490bf-117">-Encrypted</span></span>
<span data-ttu-id="490bf-118">변수를 암호화할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-119">-이름</span><span class="sxs-lookup"><span data-stu-id="490bf-119">-Name</span></span>
<span data-ttu-id="490bf-120">변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="490bf-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="490bf-121">-Profile</span></span>
<span data-ttu-id="490bf-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="490bf-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="490bf-124">-값</span><span class="sxs-lookup"><span data-stu-id="490bf-124">-Value</span></span>
<span data-ttu-id="490bf-125">변수의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490bf-126">CommonParameters</span></span>
<span data-ttu-id="490bf-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="490bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490bf-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="490bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490bf-129">입력</span><span class="sxs-lookup"><span data-stu-id="490bf-129">INPUTS</span></span>

## <span data-ttu-id="490bf-130">출력</span><span class="sxs-lookup"><span data-stu-id="490bf-130">OUTPUTS</span></span>

### <span data-ttu-id="490bf-131">Microsoft. Azure. m a. 모델 변수</span><span class="sxs-lookup"><span data-stu-id="490bf-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="490bf-132">상속자</span><span class="sxs-lookup"><span data-stu-id="490bf-132">NOTES</span></span>

## <span data-ttu-id="490bf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="490bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="490bf-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="490bf-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="490bf-135">새-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="490bf-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="490bf-136">-AzureAutomationVariable 제거</span><span class="sxs-lookup"><span data-stu-id="490bf-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


