---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045902"
---
# <span data-ttu-id="5165f-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="5165f-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="5165f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5165f-102">SYNOPSIS</span></span>
<span data-ttu-id="5165f-103">저장소 작업이 있는 스케줄러 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="5165f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5165f-104">SYNTAX</span></span>

### <span data-ttu-id="5165f-105">필수</span><span class="sxs-lookup"><span data-stu-id="5165f-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5165f-106">정기</span><span class="sxs-lookup"><span data-stu-id="5165f-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5165f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5165f-107">DESCRIPTION</span></span>
<span data-ttu-id="5165f-108">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5165f-109">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5165f-110">**AzureSchedulerStorageQueueJob** Cmdlet은 Azure 저장소 작업을 포함 하는 스케줄러 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="5165f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5165f-111">EXAMPLES</span></span>

### <span data-ttu-id="5165f-112">예제 1: 한 번 실행 되는 저장소 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5165f-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="5165f-113">이 명령은 JobCollection01 이라는 컬렉션의 일부로 스케줄러 저장소 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="5165f-114">명령에 저장소 계정, 큐 이름 및 SAS 토큰이 지정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="5165f-115">작업을 즉시 한 번만 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="5165f-116">예제 2: 지정 된 횟수 만큼 실행 되는 저장소 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5165f-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="5165f-117">이 명령은 JobCollection01 이라는 컬렉션의 일부로 스케줄러 저장소 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="5165f-118">명령에 저장소 계정, 큐 이름 및 SAS 토큰이 지정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="5165f-119">이 작업은 총 20 회, 매 시간에 두 번 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="5165f-120">변수</span><span class="sxs-lookup"><span data-stu-id="5165f-120">PARAMETERS</span></span>

### <span data-ttu-id="5165f-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5165f-121">-EndTime</span></span>
<span data-ttu-id="5165f-122">스케줄러에서 작업의 시작을 중지 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="5165f-123">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5165f-124">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5165f-124">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5165f-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="5165f-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="5165f-126">헤더를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-126">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="5165f-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="5165f-127">-ErrorActionMethod</span></span>
<span data-ttu-id="5165f-128">HTTP 및 HTTPS 동작 형식에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="5165f-129">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-129">Valid values are:</span></span> 

- <span data-ttu-id="5165f-130">가져오기</span><span class="sxs-lookup"><span data-stu-id="5165f-130">GET</span></span>
- <span data-ttu-id="5165f-131">저장할</span><span class="sxs-lookup"><span data-stu-id="5165f-131">PUT</span></span>
- <span data-ttu-id="5165f-132">올리기</span><span class="sxs-lookup"><span data-stu-id="5165f-132">POST</span></span>
- <span data-ttu-id="5165f-133">부분</span><span class="sxs-lookup"><span data-stu-id="5165f-133">HEAD</span></span>
- <span data-ttu-id="5165f-134">삭제</span><span class="sxs-lookup"><span data-stu-id="5165f-134">DELETE</span></span>

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

### <span data-ttu-id="5165f-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="5165f-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="5165f-136">저장소 작업 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-136">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="5165f-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="5165f-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="5165f-138">올리기 및 게시 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-138">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="5165f-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="5165f-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="5165f-140">저장소 큐에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="5165f-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5165f-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="5165f-142">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-142">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="5165f-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5165f-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="5165f-144">저장소 큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-144">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="5165f-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="5165f-145">-ErrorActionURI</span></span>
<span data-ttu-id="5165f-146">오류 작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-146">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="5165f-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="5165f-147">-ExecutionCount</span></span>
<span data-ttu-id="5165f-148">실행 되는 작업의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="5165f-149">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="5165f-150">-빈도</span><span class="sxs-lookup"><span data-stu-id="5165f-150">-Frequency</span></span>
<span data-ttu-id="5165f-151">이 스케줄러 작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="5165f-152">-Interval</span><span class="sxs-lookup"><span data-stu-id="5165f-152">-Interval</span></span>
<span data-ttu-id="5165f-153">*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="5165f-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="5165f-154">-JobCollectionName</span></span>
<span data-ttu-id="5165f-155">스케줄러 작업을 포함할 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-155">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="5165f-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="5165f-156">-JobName</span></span>
<span data-ttu-id="5165f-157">스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-157">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="5165f-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="5165f-158">-JobState</span></span>
<span data-ttu-id="5165f-159">스케줄러 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="5165f-160">-위치</span><span class="sxs-lookup"><span data-stu-id="5165f-160">-Location</span></span>
<span data-ttu-id="5165f-161">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="5165f-162">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-162">Valid values are:</span></span> 

- <span data-ttu-id="5165f-163">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="5165f-163">Anywhere Asia</span></span>
- <span data-ttu-id="5165f-164">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="5165f-164">Anywhere Europe</span></span>
- <span data-ttu-id="5165f-165">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="5165f-165">Anywhere US</span></span>
- <span data-ttu-id="5165f-166">동아시아</span><span class="sxs-lookup"><span data-stu-id="5165f-166">East Asia</span></span>
- <span data-ttu-id="5165f-167">미국 동부</span><span class="sxs-lookup"><span data-stu-id="5165f-167">East US</span></span>
- <span data-ttu-id="5165f-168">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="5165f-168">North Central US</span></span>
- <span data-ttu-id="5165f-169">동유럽</span><span class="sxs-lookup"><span data-stu-id="5165f-169">North Europe</span></span>
- <span data-ttu-id="5165f-170">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="5165f-170">South Central US</span></span>
- <span data-ttu-id="5165f-171">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="5165f-171">Southeast Asia</span></span>
- <span data-ttu-id="5165f-172">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="5165f-172">West Europe</span></span>
- <span data-ttu-id="5165f-173">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="5165f-173">West US</span></span>

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

### <span data-ttu-id="5165f-174">-프로필</span><span class="sxs-lookup"><span data-stu-id="5165f-174">-Profile</span></span>
<span data-ttu-id="5165f-175">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5165f-176">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5165f-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="5165f-177">-SASToken</span></span>
<span data-ttu-id="5165f-178">저장소 큐에 대 한 SAS 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-178">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="5165f-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5165f-179">-StartTime</span></span>
<span data-ttu-id="5165f-180">작업을 시작 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="5165f-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="5165f-181">-StorageQueueAccount</span></span>
<span data-ttu-id="5165f-182">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-182">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="5165f-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="5165f-183">-StorageQueueMessage</span></span>
<span data-ttu-id="5165f-184">저장소 작업에 대 한 큐 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="5165f-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="5165f-185">-StorageQueueName</span></span>
<span data-ttu-id="5165f-186">저장소 큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-186">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="5165f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5165f-187">CommonParameters</span></span>
<span data-ttu-id="5165f-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5165f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5165f-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5165f-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5165f-190">입력</span><span class="sxs-lookup"><span data-stu-id="5165f-190">INPUTS</span></span>

## <span data-ttu-id="5165f-191">출력</span><span class="sxs-lookup"><span data-stu-id="5165f-191">OUTPUTS</span></span>

## <span data-ttu-id="5165f-192">상속자</span><span class="sxs-lookup"><span data-stu-id="5165f-192">NOTES</span></span>

## <span data-ttu-id="5165f-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5165f-193">RELATED LINKS</span></span>

[<span data-ttu-id="5165f-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="5165f-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


