---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046368"
---
# <span data-ttu-id="5f9f7-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5f9f7-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="5f9f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f9f7-102">SYNOPSIS</span></span>

<span data-ttu-id="5f9f7-103">Azure Automation 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="5f9f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f9f7-104">SYNTAX</span></span>

### <span data-ttu-id="5f9f7-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f9f7-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f9f7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5f9f7-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f9f7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f9f7-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5f9f7-108">**Get-AzureAutomationModule** cmdlet은 하나 이상의 Microsoft Azure 자동화 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="5f9f7-109">기본적으로 모든 모듈이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-109">By default, all modules are returned.</span></span>
<span data-ttu-id="5f9f7-110">특정 모듈을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="5f9f7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5f9f7-111">EXAMPLES</span></span>

### <span data-ttu-id="5f9f7-112">예제 1: 모든 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f9f7-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5f9f7-113">이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="5f9f7-114">예제 2: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f9f7-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="5f9f7-115">이 명령은 Contoso17 이라는 Azure Automation 계정에서 ContosoModule 라는 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5f9f7-116">변수</span><span class="sxs-lookup"><span data-stu-id="5f9f7-116">PARAMETERS</span></span>

### <span data-ttu-id="5f9f7-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f9f7-117">-AutomationAccountName</span></span>
<span data-ttu-id="5f9f7-118">검색할 runbook이 있는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="5f9f7-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5f9f7-119">-Name</span></span>
<span data-ttu-id="5f9f7-120">검색할 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-120">Specifies the name of a module to retrieve.</span></span>

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

### <span data-ttu-id="5f9f7-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="5f9f7-121">-Profile</span></span>
<span data-ttu-id="5f9f7-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f9f7-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f9f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9f7-124">CommonParameters</span></span>
<span data-ttu-id="5f9f7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9f7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f9f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9f7-127">입력</span><span class="sxs-lookup"><span data-stu-id="5f9f7-127">INPUTS</span></span>

## <span data-ttu-id="5f9f7-128">출력</span><span class="sxs-lookup"><span data-stu-id="5f9f7-128">OUTPUTS</span></span>

### <span data-ttu-id="5f9f7-129">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="5f9f7-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="5f9f7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5f9f7-130">NOTES</span></span>

## <span data-ttu-id="5f9f7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f9f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f9f7-132">새-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5f9f7-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="5f9f7-133">-AzureAutomationModule 제거</span><span class="sxs-lookup"><span data-stu-id="5f9f7-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="5f9f7-134">Set AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="5f9f7-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


