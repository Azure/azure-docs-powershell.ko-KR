---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045462"
---
# <span data-ttu-id="10d0a-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="10d0a-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="10d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10d0a-102">SYNOPSIS</span></span>

<span data-ttu-id="10d0a-103">일시 중단 된 자동화 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="10d0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10d0a-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="10d0a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10d0a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="10d0a-106">**Resume-AzureAutomationJob** cmdlet은 일시 중단 된 Microsoft Azure 자동화 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="10d0a-107">*Id* 매개 변수를 사용 하 여 일시 중단 된 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="10d0a-108">작업을 일시 중단 하려면 Suspend-AzureAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="10d0a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="10d0a-109">EXAMPLES</span></span>

### <span data-ttu-id="10d0a-110">예제 1: 일시 중단 된 작업 다시 시작</span><span class="sxs-lookup"><span data-stu-id="10d0a-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="10d0a-111">이 명령은 지정 된 ID를 가진 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="10d0a-112">변수</span><span class="sxs-lookup"><span data-stu-id="10d0a-112">PARAMETERS</span></span>

### <span data-ttu-id="10d0a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="10d0a-113">-AutomationAccountName</span></span>
<span data-ttu-id="10d0a-114">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="10d0a-115">-Id</span><span class="sxs-lookup"><span data-stu-id="10d0a-115">-Id</span></span>
<span data-ttu-id="10d0a-116">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="10d0a-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="10d0a-117">-Profile</span></span>
<span data-ttu-id="10d0a-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10d0a-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10d0a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d0a-120">CommonParameters</span></span>
<span data-ttu-id="10d0a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10d0a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d0a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d0a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d0a-123">입력</span><span class="sxs-lookup"><span data-stu-id="10d0a-123">INPUTS</span></span>

## <span data-ttu-id="10d0a-124">출력</span><span class="sxs-lookup"><span data-stu-id="10d0a-124">OUTPUTS</span></span>

## <span data-ttu-id="10d0a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="10d0a-125">NOTES</span></span>

## <span data-ttu-id="10d0a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10d0a-126">RELATED LINKS</span></span>

[<span data-ttu-id="10d0a-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="10d0a-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="10d0a-128">정지-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="10d0a-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="10d0a-129">일시 중단-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="10d0a-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


