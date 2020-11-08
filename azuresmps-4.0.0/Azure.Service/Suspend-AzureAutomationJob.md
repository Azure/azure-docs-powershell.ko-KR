---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045759"
---
# <span data-ttu-id="45b2e-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="45b2e-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="45b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b2e-102">SYNOPSIS</span></span>

<span data-ttu-id="45b2e-103">자동화 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="45b2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45b2e-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="45b2e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45b2e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="45b2e-106">**일시 중단-AzureAutomationJob** Cmdlet은 Microsoft Azure Automation 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="45b2e-107">실행 중인 자동화 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-107">Specify a running Automation job.</span></span>

<span data-ttu-id="45b2e-108">일시 중단 된 작업을 다시 시작 하려면 **resume-AzureAutomationJob** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="45b2e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="45b2e-109">EXAMPLES</span></span>

### <span data-ttu-id="45b2e-110">예제 1: 작업 일시 중단</span><span class="sxs-lookup"><span data-stu-id="45b2e-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="45b2e-111">이 명령은 지정 된 ID를 가진 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="45b2e-112">변수</span><span class="sxs-lookup"><span data-stu-id="45b2e-112">PARAMETERS</span></span>

### <span data-ttu-id="45b2e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="45b2e-113">-AutomationAccountName</span></span>
<span data-ttu-id="45b2e-114">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="45b2e-115">-Id</span><span class="sxs-lookup"><span data-stu-id="45b2e-115">-Id</span></span>
<span data-ttu-id="45b2e-116">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="45b2e-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="45b2e-117">-Profile</span></span>
<span data-ttu-id="45b2e-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45b2e-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45b2e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b2e-120">CommonParameters</span></span>
<span data-ttu-id="45b2e-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45b2e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b2e-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b2e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b2e-123">입력</span><span class="sxs-lookup"><span data-stu-id="45b2e-123">INPUTS</span></span>

## <span data-ttu-id="45b2e-124">출력</span><span class="sxs-lookup"><span data-stu-id="45b2e-124">OUTPUTS</span></span>

## <span data-ttu-id="45b2e-125">상속자</span><span class="sxs-lookup"><span data-stu-id="45b2e-125">NOTES</span></span>

## <span data-ttu-id="45b2e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45b2e-126">RELATED LINKS</span></span>

[<span data-ttu-id="45b2e-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="45b2e-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="45b2e-128">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="45b2e-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="45b2e-129">정지-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="45b2e-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


