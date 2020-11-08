---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046050"
---
# <span data-ttu-id="19bdc-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="19bdc-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="19bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="19bdc-103">저장소 작업이 있는 스케줄러 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="19bdc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19bdc-104">SYNTAX</span></span>

### <span data-ttu-id="19bdc-105">필수</span><span class="sxs-lookup"><span data-stu-id="19bdc-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19bdc-106">정기</span><span class="sxs-lookup"><span data-stu-id="19bdc-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19bdc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="19bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="19bdc-108">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="19bdc-109">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="19bdc-110">**AzureSchedulerStorageQueueJob** Cmdlet은 Azure 저장소 작업을 포함 하는 스케줄러 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="19bdc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="19bdc-111">EXAMPLES</span></span>

### <span data-ttu-id="19bdc-112">예제 1: 저장소 큐 메시지 업데이트</span><span class="sxs-lookup"><span data-stu-id="19bdc-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="19bdc-113">이 명령은 Job12 이라는 저장소 작업에 대 한 큐 메시지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="19bdc-114">명령은 작업 컬렉션 이름과 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="19bdc-115">예제 2: 저장소 큐 작업 사용</span><span class="sxs-lookup"><span data-stu-id="19bdc-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="19bdc-116">이 명령은 Job16 이라는 작업을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="19bdc-117">이 명령은 *JobState* 매개 변수에 해당 값을 지정 하 여 작업의 상태를 사용으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="19bdc-118">변수</span><span class="sxs-lookup"><span data-stu-id="19bdc-118">PARAMETERS</span></span>

### <span data-ttu-id="19bdc-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="19bdc-119">-EndTime</span></span>
<span data-ttu-id="19bdc-120">스케줄러에서 작업의 시작을 중지 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="19bdc-121">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="19bdc-122">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="19bdc-122">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="19bdc-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="19bdc-124">헤더를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-124">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="19bdc-125">-ErrorActionMethod</span></span>
<span data-ttu-id="19bdc-126">HTTP 및 HTTPS 동작 형식에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="19bdc-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-127">Valid values are:</span></span> 

- <span data-ttu-id="19bdc-128">가져오기</span><span class="sxs-lookup"><span data-stu-id="19bdc-128">GET</span></span>
- <span data-ttu-id="19bdc-129">저장할</span><span class="sxs-lookup"><span data-stu-id="19bdc-129">PUT</span></span>
- <span data-ttu-id="19bdc-130">올리기</span><span class="sxs-lookup"><span data-stu-id="19bdc-130">POST</span></span>
- <span data-ttu-id="19bdc-131">부분</span><span class="sxs-lookup"><span data-stu-id="19bdc-131">HEAD</span></span>
- <span data-ttu-id="19bdc-132">삭제</span><span class="sxs-lookup"><span data-stu-id="19bdc-132">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="19bdc-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="19bdc-134">저장소 작업 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-134">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="19bdc-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="19bdc-136">올리기 및 게시 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-136">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="19bdc-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="19bdc-138">저장소 큐에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19bdc-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="19bdc-140">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-140">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="19bdc-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="19bdc-142">저장소 큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-142">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="19bdc-143">-ErrorActionURI</span></span>
<span data-ttu-id="19bdc-144">오류 작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-144">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="19bdc-145">-ExecutionCount</span></span>
<span data-ttu-id="19bdc-146">실행 되는 작업의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="19bdc-147">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-147">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-148">-빈도</span><span class="sxs-lookup"><span data-stu-id="19bdc-148">-Frequency</span></span>
<span data-ttu-id="19bdc-149">이 스케줄러 작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-149">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-150">-Interval</span><span class="sxs-lookup"><span data-stu-id="19bdc-150">-Interval</span></span>
<span data-ttu-id="19bdc-151">*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="19bdc-152">-JobCollectionName</span></span>
<span data-ttu-id="19bdc-153">스케줄러 작업을 포함할 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-153">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="19bdc-154">-JobName</span></span>
<span data-ttu-id="19bdc-155">업데이트할 스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-155">Specifies the name of the scheduler job to update.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="19bdc-156">-JobState</span></span>
<span data-ttu-id="19bdc-157">스케줄러 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="19bdc-158">-위치</span><span class="sxs-lookup"><span data-stu-id="19bdc-158">-Location</span></span>
<span data-ttu-id="19bdc-159">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="19bdc-160">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-160">Valid values are:</span></span> 

- <span data-ttu-id="19bdc-161">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="19bdc-161">Anywhere Asia</span></span>
- <span data-ttu-id="19bdc-162">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="19bdc-162">Anywhere Europe</span></span>
- <span data-ttu-id="19bdc-163">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="19bdc-163">Anywhere US</span></span>
- <span data-ttu-id="19bdc-164">동아시아</span><span class="sxs-lookup"><span data-stu-id="19bdc-164">East Asia</span></span>
- <span data-ttu-id="19bdc-165">미국 동부</span><span class="sxs-lookup"><span data-stu-id="19bdc-165">East US</span></span>
- <span data-ttu-id="19bdc-166">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="19bdc-166">North Central US</span></span>
- <span data-ttu-id="19bdc-167">동유럽</span><span class="sxs-lookup"><span data-stu-id="19bdc-167">North Europe</span></span>
- <span data-ttu-id="19bdc-168">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="19bdc-168">South Central US</span></span>
- <span data-ttu-id="19bdc-169">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="19bdc-169">Southeast Asia</span></span>
- <span data-ttu-id="19bdc-170">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="19bdc-170">West Europe</span></span>
- <span data-ttu-id="19bdc-171">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="19bdc-171">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19bdc-172">-PassThru</span></span>
<span data-ttu-id="19bdc-173">이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="19bdc-174">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-174">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19bdc-175">-프로필</span><span class="sxs-lookup"><span data-stu-id="19bdc-175">-Profile</span></span>
<span data-ttu-id="19bdc-176">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19bdc-177">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19bdc-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="19bdc-178">-SASToken</span></span>
<span data-ttu-id="19bdc-179">저장소 큐에 대 한 SAS 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-179">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="19bdc-180">-StartTime</span></span>
<span data-ttu-id="19bdc-181">작업을 시작 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="19bdc-182">-StorageQueueAccount</span></span>
<span data-ttu-id="19bdc-183">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-183">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="19bdc-184">-StorageQueueMessage</span></span>
<span data-ttu-id="19bdc-185">저장소 작업에 대 한 큐 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-185">Specifies the queue message for the Storage job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="19bdc-186">-StorageQueueName</span></span>
<span data-ttu-id="19bdc-187">저장소 큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-187">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bdc-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bdc-188">CommonParameters</span></span>
<span data-ttu-id="19bdc-189">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19bdc-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bdc-190">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19bdc-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bdc-191">입력</span><span class="sxs-lookup"><span data-stu-id="19bdc-191">INPUTS</span></span>

## <span data-ttu-id="19bdc-192">출력</span><span class="sxs-lookup"><span data-stu-id="19bdc-192">OUTPUTS</span></span>

## <span data-ttu-id="19bdc-193">상속자</span><span class="sxs-lookup"><span data-stu-id="19bdc-193">NOTES</span></span>

## <span data-ttu-id="19bdc-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19bdc-194">RELATED LINKS</span></span>

[<span data-ttu-id="19bdc-195">새로운 AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="19bdc-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


