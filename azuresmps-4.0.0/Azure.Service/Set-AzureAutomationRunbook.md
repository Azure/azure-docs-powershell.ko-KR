---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046072"
---
# <span data-ttu-id="770a9-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="770a9-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="770a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770a9-102">SYNOPSIS</span></span>

<span data-ttu-id="770a9-103">Runbook의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="770a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="770a9-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="770a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="770a9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="770a9-106">**Set-AzureAutomationRunbook** Cmdlet은 Microsoft Azure Automation runbook의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="770a9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="770a9-107">EXAMPLES</span></span>

### <span data-ttu-id="770a9-108">예제 1: runbook에 대 한 자세한 로깅 설정</span><span class="sxs-lookup"><span data-stu-id="770a9-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="770a9-109">이 명령은 Contoso17 이라는 자동화 계정에서 지정 된 runbook의 작업에 대 한 자세한 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="770a9-110">변수</span><span class="sxs-lookup"><span data-stu-id="770a9-110">PARAMETERS</span></span>

### <span data-ttu-id="770a9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="770a9-111">-AutomationAccountName</span></span>
<span data-ttu-id="770a9-112">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="770a9-113">-설명</span><span class="sxs-lookup"><span data-stu-id="770a9-113">-Description</span></span>
<span data-ttu-id="770a9-114">Runbook에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="770a9-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="770a9-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770a9-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="770a9-116">-LogVerbose</span></span>
<span data-ttu-id="770a9-117">자세한 로깅을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770a9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="770a9-118">-Name</span></span>
<span data-ttu-id="770a9-119">이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-119">Specifies a name.</span></span>

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

### <span data-ttu-id="770a9-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="770a9-120">-Profile</span></span>
<span data-ttu-id="770a9-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="770a9-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="770a9-123">태그</span><span class="sxs-lookup"><span data-stu-id="770a9-123">-Tags</span></span>
<span data-ttu-id="770a9-124">태그 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770a9-125">CommonParameters</span></span>
<span data-ttu-id="770a9-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="770a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770a9-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770a9-128">입력</span><span class="sxs-lookup"><span data-stu-id="770a9-128">INPUTS</span></span>

## <span data-ttu-id="770a9-129">출력</span><span class="sxs-lookup"><span data-stu-id="770a9-129">OUTPUTS</span></span>

### <span data-ttu-id="770a9-130">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="770a9-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="770a9-131">상속자</span><span class="sxs-lookup"><span data-stu-id="770a9-131">NOTES</span></span>

## <span data-ttu-id="770a9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="770a9-132">RELATED LINKS</span></span>

[<span data-ttu-id="770a9-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="770a9-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="770a9-134">새-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="770a9-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="770a9-135">게시-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="770a9-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="770a9-136">-AzureAutomationRunbook 제거</span><span class="sxs-lookup"><span data-stu-id="770a9-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="770a9-137">시작-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="770a9-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


