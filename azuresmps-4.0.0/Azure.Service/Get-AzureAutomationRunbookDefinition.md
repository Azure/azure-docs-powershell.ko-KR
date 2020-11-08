---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046362"
---
# <span data-ttu-id="1ea7c-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="1ea7c-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="1ea7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ea7c-102">SYNOPSIS</span></span>

<span data-ttu-id="1ea7c-103">Runbook 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="1ea7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ea7c-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ea7c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ea7c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1ea7c-106">**AzureAutomationRunbookDefinition** cmdlet은 초안 정의, 게시 된 정의 또는 Azure Automation runbook의 두 정의 모두를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="1ea7c-107">기본적으로 게시 된 버전이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="1ea7c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1ea7c-108">EXAMPLES</span></span>

### <span data-ttu-id="1ea7c-109">예제 1: runbook 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="1ea7c-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="1ea7c-110">이 명령은 Contoso17 이라는 Azure Automation 계정에서 RunbookDef01 이라는 runbook의 게시 된 runbook 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1ea7c-111">변수</span><span class="sxs-lookup"><span data-stu-id="1ea7c-111">PARAMETERS</span></span>

### <span data-ttu-id="1ea7c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ea7c-112">-AutomationAccountName</span></span>
<span data-ttu-id="1ea7c-113">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="1ea7c-114">-이름</span><span class="sxs-lookup"><span data-stu-id="1ea7c-114">-Name</span></span>
<span data-ttu-id="1ea7c-115">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="1ea7c-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="1ea7c-116">-Profile</span></span>
<span data-ttu-id="1ea7c-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ea7c-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ea7c-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1ea7c-119">-Slot</span></span>
<span data-ttu-id="1ea7c-120">슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-120">Specifies the slot.</span></span>
<span data-ttu-id="1ea7c-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ea7c-122">함</span><span class="sxs-lookup"><span data-stu-id="1ea7c-122">Draft</span></span>
- <span data-ttu-id="1ea7c-123">게시자</span><span class="sxs-lookup"><span data-stu-id="1ea7c-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea7c-124">CommonParameters</span></span>
<span data-ttu-id="1ea7c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ea7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea7c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ea7c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea7c-127">입력</span><span class="sxs-lookup"><span data-stu-id="1ea7c-127">INPUTS</span></span>

## <span data-ttu-id="1ea7c-128">출력</span><span class="sxs-lookup"><span data-stu-id="1ea7c-128">OUTPUTS</span></span>

## <span data-ttu-id="1ea7c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1ea7c-129">NOTES</span></span>

## <span data-ttu-id="1ea7c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ea7c-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ea7c-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="1ea7c-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


