---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703625"
---
# <span data-ttu-id="01bff-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="01bff-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="01bff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01bff-102">SYNOPSIS</span></span>
<span data-ttu-id="01bff-103">HTTP 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01bff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01bff-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01bff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01bff-105">DESCRIPTION</span></span>
<span data-ttu-id="01bff-106">**새 AzureRmSchedulerHttpJob** Cmdlet은 Azure SCHEDULER에서 HTTP 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="01bff-107">이 cmdlet은 *Erroractiontype* 및 *httpauthenticationtype* 매개 변수에 기반 하는 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="01bff-108">동적 매개 변수는 다른 매개 변수 값에 따라 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="01bff-109">다른 매개 변수를 지정한 후 동적 매개 변수의 이름을 검색 하려면 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="01bff-110">필수 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="01bff-111">예제의</span><span class="sxs-lookup"><span data-stu-id="01bff-111">EXAMPLES</span></span>

## <span data-ttu-id="01bff-112">변수</span><span class="sxs-lookup"><span data-stu-id="01bff-112">PARAMETERS</span></span>

### <span data-ttu-id="01bff-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="01bff-113">-EndTime</span></span>
<span data-ttu-id="01bff-114">작업에 대 한 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="01bff-115">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="01bff-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="01bff-116">-ErrorActionType</span></span>
<span data-ttu-id="01bff-117">작업에 대 한 오류 동작 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="01bff-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01bff-119">Http</span><span class="sxs-lookup"><span data-stu-id="01bff-119">Http</span></span> 
- <span data-ttu-id="01bff-120">Https</span><span class="sxs-lookup"><span data-stu-id="01bff-120">Https</span></span> 
- <span data-ttu-id="01bff-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="01bff-121">StorageQueue</span></span> 
- <span data-ttu-id="01bff-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="01bff-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="01bff-123">Service<c13> Stopic</span><span class="sxs-lookup"><span data-stu-id="01bff-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="01bff-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="01bff-124">-ExecutionCount</span></span>
<span data-ttu-id="01bff-125">작업이 실행 되는 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="01bff-126">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="01bff-127">-빈도</span><span class="sxs-lookup"><span data-stu-id="01bff-127">-Frequency</span></span>
<span data-ttu-id="01bff-128">작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="01bff-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01bff-130">길이의</span><span class="sxs-lookup"><span data-stu-id="01bff-130">Minute</span></span> 
- <span data-ttu-id="01bff-131">시간씩</span><span class="sxs-lookup"><span data-stu-id="01bff-131">Hour</span></span> 
- <span data-ttu-id="01bff-132">부활절</span><span class="sxs-lookup"><span data-stu-id="01bff-132">Day</span></span> 
- <span data-ttu-id="01bff-133">이번</span><span class="sxs-lookup"><span data-stu-id="01bff-133">Week</span></span> 
- <span data-ttu-id="01bff-134">달은</span><span class="sxs-lookup"><span data-stu-id="01bff-134">Month</span></span>

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

### <span data-ttu-id="01bff-135">-헤더</span><span class="sxs-lookup"><span data-stu-id="01bff-135">-Headers</span></span>
<span data-ttu-id="01bff-136">헤더를 포함 하는 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="01bff-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="01bff-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="01bff-138">HTTP 인증 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="01bff-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01bff-140">않아야</span><span class="sxs-lookup"><span data-stu-id="01bff-140">None</span></span> 
- <span data-ttu-id="01bff-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="01bff-141">ClientCertificate</span></span> 
- <span data-ttu-id="01bff-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="01bff-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="01bff-143">기본적</span><span class="sxs-lookup"><span data-stu-id="01bff-143">Basic</span></span>

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

### <span data-ttu-id="01bff-144">-Interval</span><span class="sxs-lookup"><span data-stu-id="01bff-144">-Interval</span></span>
<span data-ttu-id="01bff-145">작업에 대 한 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="01bff-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="01bff-146">-JobCollectionName</span></span>
<span data-ttu-id="01bff-147">작업이 속한 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="01bff-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="01bff-148">-JobName</span></span>
<span data-ttu-id="01bff-149">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="01bff-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="01bff-150">-JobState</span></span>
<span data-ttu-id="01bff-151">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-151">Specifies the state of the job.</span></span>
<span data-ttu-id="01bff-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01bff-153">수</span><span class="sxs-lookup"><span data-stu-id="01bff-153">Enabled</span></span> 
- <span data-ttu-id="01bff-154">비활성화</span><span class="sxs-lookup"><span data-stu-id="01bff-154">Disabled</span></span>

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

### <span data-ttu-id="01bff-155">-메서드</span><span class="sxs-lookup"><span data-stu-id="01bff-155">-Method</span></span>
<span data-ttu-id="01bff-156">작업의 동작 종류에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="01bff-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01bff-158">가져오기</span><span class="sxs-lookup"><span data-stu-id="01bff-158">GET</span></span> 
- <span data-ttu-id="01bff-159">저장할</span><span class="sxs-lookup"><span data-stu-id="01bff-159">PUT</span></span> 
- <span data-ttu-id="01bff-160">올리기</span><span class="sxs-lookup"><span data-stu-id="01bff-160">POST</span></span> 
- <span data-ttu-id="01bff-161">삭제</span><span class="sxs-lookup"><span data-stu-id="01bff-161">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01bff-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="01bff-162">-RequestBody</span></span>
<span data-ttu-id="01bff-163">올리기 및 게시 작업에 대 한 본문의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="01bff-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01bff-164">-ResourceGroupName</span></span>
<span data-ttu-id="01bff-165">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="01bff-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="01bff-166">-StartTime</span></span>
<span data-ttu-id="01bff-167">작업에 대 한 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="01bff-168">-Uri</span><span class="sxs-lookup"><span data-stu-id="01bff-168">-Uri</span></span>
<span data-ttu-id="01bff-169">작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-169">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01bff-170">-확인</span><span class="sxs-lookup"><span data-stu-id="01bff-170">-Confirm</span></span>
<span data-ttu-id="01bff-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01bff-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01bff-172">-WhatIf</span></span>
<span data-ttu-id="01bff-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01bff-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01bff-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bff-175">-DefaultProfile</span></span>
<span data-ttu-id="01bff-176">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01bff-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bff-177">CommonParameters</span></span>
<span data-ttu-id="01bff-178">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bff-179">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bff-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bff-180">입력</span><span class="sxs-lookup"><span data-stu-id="01bff-180">INPUTS</span></span>

## <span data-ttu-id="01bff-181">출력</span><span class="sxs-lookup"><span data-stu-id="01bff-181">OUTPUTS</span></span>

### <span data-ttu-id="01bff-182">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="01bff-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="01bff-183">상속자</span><span class="sxs-lookup"><span data-stu-id="01bff-183">NOTES</span></span>

## <span data-ttu-id="01bff-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01bff-184">RELATED LINKS</span></span>

[<span data-ttu-id="01bff-185">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="01bff-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="01bff-186">새로운 AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="01bff-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="01bff-187">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="01bff-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="01bff-188">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="01bff-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="01bff-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="01bff-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="01bff-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="01bff-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="01bff-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="01bff-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="01bff-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="01bff-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="01bff-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="01bff-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


