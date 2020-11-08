---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045934"
---
# <span data-ttu-id="563c0-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="563c0-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="563c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="563c0-102">SYNOPSIS</span></span>

<span data-ttu-id="563c0-103">Runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-103">Creates a runbook.</span></span>

## <span data-ttu-id="563c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="563c0-104">SYNTAX</span></span>

### <span data-ttu-id="563c0-105">ByRunbookName (기본값)</span><span class="sxs-lookup"><span data-stu-id="563c0-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="563c0-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="563c0-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="563c0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="563c0-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="563c0-108">**새로운-AzureAutomationRunbook** cmdlet은 비어 있는 새 Microsoft Azure 자동화 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="563c0-109">이름을 지정 하 여 새 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="563c0-110">Windows PowerShell 스크립트 (ps1) 파일 경로를 지정 하 여 runbook을 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="563c0-111">가져올 스크립트에는 단일 Windows PowerShell 워크플로 정의가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="563c0-112">이 Windows PowerShell 워크플로의 이름은 runbook의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="563c0-113">예제의</span><span class="sxs-lookup"><span data-stu-id="563c0-113">EXAMPLES</span></span>

### <span data-ttu-id="563c0-114">예제 1: runbook 만들기</span><span class="sxs-lookup"><span data-stu-id="563c0-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="563c0-115">이 명령은 Contoso17 이라는 Automation 계정에 Runbook02 이라는 새 runbook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="563c0-116">변수</span><span class="sxs-lookup"><span data-stu-id="563c0-116">PARAMETERS</span></span>

### <span data-ttu-id="563c0-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="563c0-117">-AutomationAccountName</span></span>
<span data-ttu-id="563c0-118">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="563c0-119">-설명</span><span class="sxs-lookup"><span data-stu-id="563c0-119">-Description</span></span>
<span data-ttu-id="563c0-120">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="563c0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="563c0-121">-Name</span></span>
<span data-ttu-id="563c0-122">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563c0-123">-Path</span><span class="sxs-lookup"><span data-stu-id="563c0-123">-Path</span></span>
<span data-ttu-id="563c0-124">경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563c0-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="563c0-125">-Profile</span></span>
<span data-ttu-id="563c0-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="563c0-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="563c0-128">태그</span><span class="sxs-lookup"><span data-stu-id="563c0-128">-Tags</span></span>
<span data-ttu-id="563c0-129">Runbook에 대 한 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563c0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563c0-130">CommonParameters</span></span>
<span data-ttu-id="563c0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="563c0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563c0-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563c0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563c0-133">입력</span><span class="sxs-lookup"><span data-stu-id="563c0-133">INPUTS</span></span>

## <span data-ttu-id="563c0-134">출력</span><span class="sxs-lookup"><span data-stu-id="563c0-134">OUTPUTS</span></span>

### <span data-ttu-id="563c0-135">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="563c0-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="563c0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="563c0-136">NOTES</span></span>

## <span data-ttu-id="563c0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="563c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="563c0-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="563c0-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="563c0-139">게시-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="563c0-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="563c0-140">-AzureAutomationRunbook 제거</span><span class="sxs-lookup"><span data-stu-id="563c0-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="563c0-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="563c0-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="563c0-142">시작-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="563c0-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


