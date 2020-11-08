---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045552"
---
# <span data-ttu-id="bdd66-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="bdd66-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="bdd66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd66-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd66-103">StorSimple 장치에서 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="bdd66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdd66-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bdd66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bdd66-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd66-106">**Get-AzureStorSimpleTask** Cmdlet는 Azure StorSimple 장치에서 비동기적으로 실행 되는 작업의 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="bdd66-107">StorSimple 장치를 관리 하는 동안 대부분의 만들기, 읽기, 업데이트 및 삭제 작업이 비동기적으로 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="bdd66-108">Windows PowerShell은 **TaskId** 를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="bdd66-109">ID를 사용 하 여 작업의 현재 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="bdd66-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bdd66-110">EXAMPLES</span></span>

### <span data-ttu-id="bdd66-111">예제 1: 작업 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="bdd66-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="bdd66-112">이 명령은 지정 된 ID를 가진 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="bdd66-113">결과에는 해당 작업의 상태가 완료 됨과 성공한 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="bdd66-114">변수</span><span class="sxs-lookup"><span data-stu-id="bdd66-114">PARAMETERS</span></span>

### <span data-ttu-id="bdd66-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bdd66-115">-InstanceId</span></span>
<span data-ttu-id="bdd66-116">이 cmdlet이 상태를 추적 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd66-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="bdd66-117">-Profile</span></span>
<span data-ttu-id="bdd66-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bdd66-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bdd66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd66-120">CommonParameters</span></span>
<span data-ttu-id="bdd66-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd66-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd66-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd66-123">입력</span><span class="sxs-lookup"><span data-stu-id="bdd66-123">INPUTS</span></span>

### <span data-ttu-id="bdd66-124">않아야</span><span class="sxs-lookup"><span data-stu-id="bdd66-124">None</span></span>

## <span data-ttu-id="bdd66-125">출력</span><span class="sxs-lookup"><span data-stu-id="bdd66-125">OUTPUTS</span></span>

### <span data-ttu-id="bdd66-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="bdd66-126">JobStatusInfo</span></span>
<span data-ttu-id="bdd66-127">이 cmdlet은 다음 필드를 포함 하는 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="bdd66-128">**오류가 발생 했습니다**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-128">**Error**.</span></span>
<span data-ttu-id="bdd66-129">**코드** 와 **메시지가** 포함 된 **errordetails**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="bdd66-130">**TaskId**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-130">**TaskId**.</span></span>
<span data-ttu-id="bdd66-131">**문자열** 입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-131">**String**.</span></span>
<span data-ttu-id="bdd66-132">상태가 반환 되는 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="bdd66-133">**Tasksteps**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-133">**TaskSteps**.</span></span>
<span data-ttu-id="bdd66-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="bdd66-135">각 **Taskstep** 개체에는 **세부 정보** , **ErrorCode** , **메시지** , **결과** , **상태가** 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="bdd66-136">**결과**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-136">**Result**.</span></span>
<span data-ttu-id="bdd66-137">작업의 전체 결과를 포함 하는 **Taskresult** 입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="bdd66-138">유효한 값은 Failed, Succeeded, PartialSuccess, 취소 됨, 유효 하지 않음입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="bdd66-139">**상태** 입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-139">**Status**.</span></span>
<span data-ttu-id="bdd66-140">작업의 전체 실행 상태가 포함 된 **Taskstatus** 입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="bdd66-141">유효한 값은 Inprogress, 유효 하지 않음, 완료 됨입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="bdd66-142">**Taskresult**.</span><span class="sxs-lookup"><span data-stu-id="bdd66-142">**TaskResult**.</span></span>
<span data-ttu-id="bdd66-143">**Taskresult** , **결과** 및 **상태** 를 기반으로 계산 되는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="bdd66-144">유효한 값은 Failed, Succeeded, InProgress, PartialSuccess, 취소 됨, 유효 하지 않음입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd66-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="bdd66-145">상속자</span><span class="sxs-lookup"><span data-stu-id="bdd66-145">NOTES</span></span>

## <span data-ttu-id="bdd66-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdd66-146">RELATED LINKS</span></span>

