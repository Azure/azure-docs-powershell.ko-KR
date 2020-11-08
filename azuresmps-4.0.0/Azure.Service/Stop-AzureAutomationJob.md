---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045942"
---
# <span data-ttu-id="7e591-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7e591-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="7e591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e591-102">SYNOPSIS</span></span>

<span data-ttu-id="7e591-103">자동화 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-103">Stops an Automation job.</span></span>

## <span data-ttu-id="7e591-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e591-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e591-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e591-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7e591-106">**Stop-AzureAutomationJob** Cmdlet은 Microsoft Azure Automation 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="7e591-107">실행 중인 자동화 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-107">Specify a running automation job.</span></span>

## <span data-ttu-id="7e591-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7e591-108">EXAMPLES</span></span>

### <span data-ttu-id="7e591-109">예제 1: 작업 중지</span><span class="sxs-lookup"><span data-stu-id="7e591-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="7e591-110">이 명령은 지정 된 ID를 가진 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="7e591-111">변수</span><span class="sxs-lookup"><span data-stu-id="7e591-111">PARAMETERS</span></span>

### <span data-ttu-id="7e591-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e591-112">-AutomationAccountName</span></span>
<span data-ttu-id="7e591-113">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="7e591-114">-Id</span><span class="sxs-lookup"><span data-stu-id="7e591-114">-Id</span></span>
<span data-ttu-id="7e591-115">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="7e591-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="7e591-116">-Profile</span></span>
<span data-ttu-id="7e591-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e591-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e591-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e591-119">CommonParameters</span></span>
<span data-ttu-id="7e591-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e591-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e591-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e591-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e591-122">입력</span><span class="sxs-lookup"><span data-stu-id="7e591-122">INPUTS</span></span>

## <span data-ttu-id="7e591-123">출력</span><span class="sxs-lookup"><span data-stu-id="7e591-123">OUTPUTS</span></span>

## <span data-ttu-id="7e591-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7e591-124">NOTES</span></span>

## <span data-ttu-id="7e591-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e591-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e591-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7e591-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="7e591-127">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7e591-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="7e591-128">일시 중단-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7e591-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


