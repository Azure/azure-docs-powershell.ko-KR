---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2810a73e54151d8227a115aa71f486d09811def8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528397"
---
# <span data-ttu-id="05957-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="05957-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="05957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05957-102">SYNOPSIS</span></span>
<span data-ttu-id="05957-103">스케줄러 HTTP 작업을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05957-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05957-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05957-105">설명은</span><span class="sxs-lookup"><span data-stu-id="05957-105">DESCRIPTION</span></span>
<span data-ttu-id="05957-106">**Set-AzureRmSchedulerHttpJob** Cmdlet은 Azure SCHEDULER의 HTTP 작업을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="05957-107">이 cmdlet은 *Erroractiontype* 및 *httpauthenticationtype* 매개 변수에 기반 하는 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="05957-108">동적 매개 변수는 다른 매개 변수 값에 따라 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05957-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="05957-109">다른 매개 변수를 지정한 후 동적 매개 변수의 이름을 검색 하려면 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="05957-110">필수 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="05957-111">예제의</span><span class="sxs-lookup"><span data-stu-id="05957-111">EXAMPLES</span></span>

## <span data-ttu-id="05957-112">변수</span><span class="sxs-lookup"><span data-stu-id="05957-112">PARAMETERS</span></span>

### <span data-ttu-id="05957-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05957-113">-DefaultProfile</span></span>
<span data-ttu-id="05957-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05957-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="05957-115">-EndTime</span></span>
<span data-ttu-id="05957-116">작업에 대 한 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="05957-117">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="05957-118">-ErrorActionType</span></span>
<span data-ttu-id="05957-119">작업에 대 한 오류 동작 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="05957-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="05957-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05957-121">Http</span><span class="sxs-lookup"><span data-stu-id="05957-121">Http</span></span> 
- <span data-ttu-id="05957-122">Https</span><span class="sxs-lookup"><span data-stu-id="05957-122">Https</span></span> 
- <span data-ttu-id="05957-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="05957-123">StorageQueue</span></span> 
- <span data-ttu-id="05957-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="05957-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="05957-125">Service<c13> Stopic</span><span class="sxs-lookup"><span data-stu-id="05957-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05957-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="05957-126">-ExecutionCount</span></span>
<span data-ttu-id="05957-127">작업이 실행 되는 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="05957-128">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05957-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-129">-빈도</span><span class="sxs-lookup"><span data-stu-id="05957-129">-Frequency</span></span>
<span data-ttu-id="05957-130">작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="05957-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="05957-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05957-132">길이의</span><span class="sxs-lookup"><span data-stu-id="05957-132">Minute</span></span> 
- <span data-ttu-id="05957-133">시간씩</span><span class="sxs-lookup"><span data-stu-id="05957-133">Hour</span></span> 
- <span data-ttu-id="05957-134">부활절</span><span class="sxs-lookup"><span data-stu-id="05957-134">Day</span></span> 
- <span data-ttu-id="05957-135">이번</span><span class="sxs-lookup"><span data-stu-id="05957-135">Week</span></span> 
- <span data-ttu-id="05957-136">달은</span><span class="sxs-lookup"><span data-stu-id="05957-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-137">-헤더</span><span class="sxs-lookup"><span data-stu-id="05957-137">-Headers</span></span>
<span data-ttu-id="05957-138">헤더를 포함 하는 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05957-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="05957-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="05957-140">HTTP 인증 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="05957-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="05957-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05957-142">않아야</span><span class="sxs-lookup"><span data-stu-id="05957-142">None</span></span> 
- <span data-ttu-id="05957-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="05957-143">ClientCertificate</span></span> 
- <span data-ttu-id="05957-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="05957-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="05957-145">기본적</span><span class="sxs-lookup"><span data-stu-id="05957-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-146">-Interval</span><span class="sxs-lookup"><span data-stu-id="05957-146">-Interval</span></span>
<span data-ttu-id="05957-147">작업에 대 한 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-147">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="05957-148">-JobCollectionName</span></span>
<span data-ttu-id="05957-149">작업이 속한 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-149">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05957-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="05957-150">-JobName</span></span>
<span data-ttu-id="05957-151">이 cmdlet이 수정 하는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-151">Specifies the name of the job that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05957-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="05957-152">-JobState</span></span>
<span data-ttu-id="05957-153">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-153">Specifies the state of the job.</span></span>
<span data-ttu-id="05957-154">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="05957-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05957-155">수</span><span class="sxs-lookup"><span data-stu-id="05957-155">Enabled</span></span> 
- <span data-ttu-id="05957-156">비활성화</span><span class="sxs-lookup"><span data-stu-id="05957-156">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05957-157">-메서드</span><span class="sxs-lookup"><span data-stu-id="05957-157">-Method</span></span>
<span data-ttu-id="05957-158">이 작업의 동작 종류에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="05957-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="05957-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05957-160">가져오기</span><span class="sxs-lookup"><span data-stu-id="05957-160">GET</span></span> 
- <span data-ttu-id="05957-161">저장할</span><span class="sxs-lookup"><span data-stu-id="05957-161">PUT</span></span> 
- <span data-ttu-id="05957-162">올리기</span><span class="sxs-lookup"><span data-stu-id="05957-162">POST</span></span> 
- <span data-ttu-id="05957-163">삭제</span><span class="sxs-lookup"><span data-stu-id="05957-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="05957-164">-RequestBody</span></span>
<span data-ttu-id="05957-165">올리기 및 게시 작업에 대 한 본문의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-165">Specifies the value of the body for PUT and POST job actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05957-166">-ResourceGroupName</span></span>
<span data-ttu-id="05957-167">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-167">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05957-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05957-168">-StartTime</span></span>
<span data-ttu-id="05957-169">작업에 대 한 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-170">-Uri</span><span class="sxs-lookup"><span data-stu-id="05957-170">-Uri</span></span>
<span data-ttu-id="05957-171">작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-172">-확인</span><span class="sxs-lookup"><span data-stu-id="05957-172">-Confirm</span></span>
<span data-ttu-id="05957-173">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-173">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05957-174">-WhatIf</span></span>
<span data-ttu-id="05957-175">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05957-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05957-176">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05957-176">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05957-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05957-177">CommonParameters</span></span>
<span data-ttu-id="05957-178">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05957-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05957-179">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05957-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05957-180">입력</span><span class="sxs-lookup"><span data-stu-id="05957-180">INPUTS</span></span>

### <span data-ttu-id="05957-181">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05957-181">System.String</span></span>

### <span data-ttu-id="05957-182">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="05957-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="05957-183">출력</span><span class="sxs-lookup"><span data-stu-id="05957-183">OUTPUTS</span></span>

### <span data-ttu-id="05957-184">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="05957-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="05957-185">상속자</span><span class="sxs-lookup"><span data-stu-id="05957-185">NOTES</span></span>

## <span data-ttu-id="05957-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05957-186">RELATED LINKS</span></span>

[<span data-ttu-id="05957-187">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="05957-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="05957-188">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="05957-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="05957-189">새로운 AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="05957-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="05957-190">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="05957-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="05957-191">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="05957-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="05957-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="05957-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="05957-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="05957-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="05957-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="05957-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="05957-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="05957-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


