---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046070"
---
# <span data-ttu-id="f6baf-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="f6baf-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="f6baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6baf-102">SYNOPSIS</span></span>

<span data-ttu-id="f6baf-103">Runbook의 초안 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="f6baf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6baf-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6baf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f6baf-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f6baf-106">**AzureAutomationRunbookDefinition** Cmdlet은 Microsoft Azure Automation runbook의 초안 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="f6baf-107">초안 runbook이 되는 runbook이 포함 된 Windows PowerShell 스크립트 (ps1) 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="f6baf-108">초안 정의가 이미 있는 경우에는 *Overwrite* 매개 변수를 사용 하 여 cmdlet에서 기존 초안을 덮어쓰도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="f6baf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f6baf-109">EXAMPLES</span></span>

### <span data-ttu-id="f6baf-110">예제 1: runbook의 기존 초안 정의 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="f6baf-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="f6baf-111">이 명령은 runbook의 기존 초안 정의를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="f6baf-112">변수</span><span class="sxs-lookup"><span data-stu-id="f6baf-112">PARAMETERS</span></span>

### <span data-ttu-id="f6baf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f6baf-113">-AutomationAccountName</span></span>
<span data-ttu-id="f6baf-114">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="f6baf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f6baf-115">-Name</span></span>
<span data-ttu-id="f6baf-116">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-116">Specifies a name.</span></span>

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

### <span data-ttu-id="f6baf-117">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f6baf-117">-Overwrite</span></span>
<span data-ttu-id="f6baf-118">기존 초안 정의를 덮어쓸지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6baf-119">-Path</span><span class="sxs-lookup"><span data-stu-id="f6baf-119">-Path</span></span>
<span data-ttu-id="f6baf-120">Runbook에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6baf-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="f6baf-121">-Profile</span></span>
<span data-ttu-id="f6baf-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f6baf-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6baf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6baf-124">CommonParameters</span></span>
<span data-ttu-id="f6baf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6baf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6baf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6baf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6baf-127">입력</span><span class="sxs-lookup"><span data-stu-id="f6baf-127">INPUTS</span></span>

## <span data-ttu-id="f6baf-128">출력</span><span class="sxs-lookup"><span data-stu-id="f6baf-128">OUTPUTS</span></span>

### <span data-ttu-id="f6baf-129">RunbookDefinition를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="f6baf-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="f6baf-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f6baf-130">NOTES</span></span>

## <span data-ttu-id="f6baf-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6baf-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6baf-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="f6baf-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


