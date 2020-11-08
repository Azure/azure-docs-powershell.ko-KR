---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046096"
---
# <span data-ttu-id="b185c-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b185c-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="b185c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b185c-102">SYNOPSIS</span></span>
<span data-ttu-id="b185c-103">서비스 구성에서 액세스 제어 레코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="b185c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b185c-104">SYNTAX</span></span>

### <span data-ttu-id="b185c-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="b185c-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b185c-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="b185c-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b185c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b185c-107">DESCRIPTION</span></span>
<span data-ttu-id="b185c-108">**AzureStorSimpleAccessControlRecord** cmdlet은 서비스 구성에서 액세스 제어 레코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="b185c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b185c-109">EXAMPLES</span></span>

### <span data-ttu-id="b185c-110">예제 1: Access 컨트롤 제거 recordaccess 컨트롤에 대 한 액세스 제어</span><span class="sxs-lookup"><span data-stu-id="b185c-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="b185c-111">이 명령은 Acr10 이라는 액세스 제어 레코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="b185c-112">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="b185c-113">예제 2: pipelineAccess Controlaccess control 액세스 제어를 사용 하 여 Access Controlaccess 컨트롤 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b185c-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="b185c-114">이 명령은 **Get-AzureStorSimpleAccessControlRecord** 를 사용 하 여 Acr10 이라는 **accesscontrolrecord** 를 가져오고, 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b185c-115">명령이 **Accesscontrolrecord** 개체를 제거 하는 작업을 시작한 다음 **taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="b185c-116">작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="b185c-117">변수</span><span class="sxs-lookup"><span data-stu-id="b185c-117">PARAMETERS</span></span>

### <span data-ttu-id="b185c-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="b185c-118">-ACR</span></span>
<span data-ttu-id="b185c-119">삭제할 **Accesscontrolrecord** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="b185c-120">**Accesscontrolrecord** 개체를 가져오려면 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b185c-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="b185c-121">-ACRName</span></span>
<span data-ttu-id="b185c-122">삭제할 액세스 제어 레코드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-122">Specifies a name of the access control record to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b185c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b185c-123">-Force</span></span>
<span data-ttu-id="b185c-124">이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b185c-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="b185c-125">-Profile</span></span>
<span data-ttu-id="b185c-126">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b185c-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b185c-127">-WaitForComplete</span></span>
<span data-ttu-id="b185c-128">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b185c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b185c-129">CommonParameters</span></span>
<span data-ttu-id="b185c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b185c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b185c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b185c-132">입력</span><span class="sxs-lookup"><span data-stu-id="b185c-132">INPUTS</span></span>

### <span data-ttu-id="b185c-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b185c-133">AccessControlRecord</span></span>
<span data-ttu-id="b185c-134">이 cmdlet은 **Accesscontrolrecord** 개체를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="b185c-135">**Accesscontrolrecord** 개체에는 다음 필드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="b185c-136">**Globalid** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="b185c-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="b185c-137">**InitiatorName** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="b185c-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="b185c-138">**InstanceId** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="b185c-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="b185c-139">**Name** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="b185c-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="b185c-140">**Operationinprogress** ( **operationinprogress** )</span><span class="sxs-lookup"><span data-stu-id="b185c-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="b185c-141">**(** **Int** ).</span><span class="sxs-lookup"><span data-stu-id="b185c-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="b185c-142">출력</span><span class="sxs-lookup"><span data-stu-id="b185c-142">OUTPUTS</span></span>

### <span data-ttu-id="b185c-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="b185c-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="b185c-144">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="b185c-145">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b185c-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="b185c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b185c-146">NOTES</span></span>

## <span data-ttu-id="b185c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b185c-147">RELATED LINKS</span></span>

[<span data-ttu-id="b185c-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b185c-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b185c-149">새로운 AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b185c-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b185c-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b185c-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b185c-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="b185c-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


