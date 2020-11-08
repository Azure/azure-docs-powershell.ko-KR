---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045658"
---
# <span data-ttu-id="179f5-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="179f5-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="179f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179f5-102">SYNOPSIS</span></span>

<span data-ttu-id="179f5-103">Azure Automation 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="179f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="179f5-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="179f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="179f5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="179f5-106">**Get-AzureAutomationJobOutput** Cmdlet은 Microsoft Azure Automation 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="179f5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="179f5-107">EXAMPLES</span></span>

### <span data-ttu-id="179f5-108">예제 1: Azure Automation 작업의 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="179f5-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="179f5-109">이 명령은 지정 된 ID를 갖는 모든 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="179f5-110">변수</span><span class="sxs-lookup"><span data-stu-id="179f5-110">PARAMETERS</span></span>

### <span data-ttu-id="179f5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="179f5-111">-AutomationAccountName</span></span>
<span data-ttu-id="179f5-112">Azure Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-112">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="179f5-113">-Id</span><span class="sxs-lookup"><span data-stu-id="179f5-113">-Id</span></span>
<span data-ttu-id="179f5-114">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="179f5-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="179f5-115">-Profile</span></span>
<span data-ttu-id="179f5-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="179f5-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="179f5-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="179f5-118">-StartTime</span></span>
<span data-ttu-id="179f5-119">시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="179f5-120">-스트림</span><span class="sxs-lookup"><span data-stu-id="179f5-120">-Stream</span></span>
<span data-ttu-id="179f5-121">출력 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-121">Specifies the type of output.</span></span>
<span data-ttu-id="179f5-122">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-122">Valid values are:</span></span> 

- <span data-ttu-id="179f5-123">이상</span><span class="sxs-lookup"><span data-stu-id="179f5-123">Any</span></span>
- <span data-ttu-id="179f5-124">디버깅이</span><span class="sxs-lookup"><span data-stu-id="179f5-124">Debug</span></span>
- <span data-ttu-id="179f5-125">오류</span><span class="sxs-lookup"><span data-stu-id="179f5-125">Error</span></span>
- <span data-ttu-id="179f5-126">결과물</span><span class="sxs-lookup"><span data-stu-id="179f5-126">Output</span></span>
- <span data-ttu-id="179f5-127">진행률과</span><span class="sxs-lookup"><span data-stu-id="179f5-127">Progress</span></span>
- <span data-ttu-id="179f5-128">정보</span><span class="sxs-lookup"><span data-stu-id="179f5-128">Verbose</span></span>
- <span data-ttu-id="179f5-129">오류</span><span class="sxs-lookup"><span data-stu-id="179f5-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="179f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179f5-130">CommonParameters</span></span>
<span data-ttu-id="179f5-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="179f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179f5-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179f5-133">입력</span><span class="sxs-lookup"><span data-stu-id="179f5-133">INPUTS</span></span>

## <span data-ttu-id="179f5-134">출력</span><span class="sxs-lookup"><span data-stu-id="179f5-134">OUTPUTS</span></span>

## <span data-ttu-id="179f5-135">상속자</span><span class="sxs-lookup"><span data-stu-id="179f5-135">NOTES</span></span>

## <span data-ttu-id="179f5-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="179f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="179f5-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="179f5-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="179f5-138">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="179f5-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="179f5-139">정지-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="179f5-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="179f5-140">일시 중단-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="179f5-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


