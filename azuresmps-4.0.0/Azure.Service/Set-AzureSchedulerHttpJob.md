---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045799"
---
# <span data-ttu-id="c3347-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c3347-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="c3347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3347-102">SYNOPSIS</span></span>
<span data-ttu-id="c3347-103">HTTP 작업이 있는 스케줄러 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="c3347-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3347-104">SYNTAX</span></span>

### <span data-ttu-id="c3347-105">필수</span><span class="sxs-lookup"><span data-stu-id="c3347-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3347-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="c3347-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3347-107">정기</span><span class="sxs-lookup"><span data-stu-id="c3347-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3347-108">인증서</span><span class="sxs-lookup"><span data-stu-id="c3347-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3347-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c3347-109">DESCRIPTION</span></span>
<span data-ttu-id="c3347-110">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c3347-111">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c3347-112">**Set-AzureSchedulerHttpJob** CMDLET은 HTTP 작업이 있는 스케줄러 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="c3347-113">예제의</span><span class="sxs-lookup"><span data-stu-id="c3347-113">EXAMPLES</span></span>

### <span data-ttu-id="c3347-114">예제 1: 작업 상태를 사용 안 함으로 변경</span><span class="sxs-lookup"><span data-stu-id="c3347-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="c3347-115">이 명령은 Job01 이라는 작업의 상태를 Disabled로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="c3347-116">해당 작업은 지정 된 위치에 대 한 JobColleciton01 이라는 작업 컬렉션의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="c3347-117">예제 2: 작업의 URI 업데이트</span><span class="sxs-lookup"><span data-stu-id="c3347-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="c3347-118">이 명령은 Job01 이라는 작업의 URI를 업데이트 http://www.contoso.com 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="c3347-119">변수</span><span class="sxs-lookup"><span data-stu-id="c3347-119">PARAMETERS</span></span>

### <span data-ttu-id="c3347-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c3347-120">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="c3347-121">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c3347-122">-EndTime</span></span>
<span data-ttu-id="c3347-123">스케줄러에서 시작 작업을 중지 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="c3347-124">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="c3347-125">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3347-125">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="c3347-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="c3347-127">헤더를 hashtable로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="c3347-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="c3347-128">-ErrorActionMethod</span></span>
<span data-ttu-id="c3347-129">HTTP 및 HTTPS 동작 형식에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="c3347-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-130">Valid values are:</span></span> 

- <span data-ttu-id="c3347-131">가져오기</span><span class="sxs-lookup"><span data-stu-id="c3347-131">GET</span></span>
- <span data-ttu-id="c3347-132">저장할</span><span class="sxs-lookup"><span data-stu-id="c3347-132">PUT</span></span>
- <span data-ttu-id="c3347-133">올리기</span><span class="sxs-lookup"><span data-stu-id="c3347-133">POST</span></span>
- <span data-ttu-id="c3347-134">부분</span><span class="sxs-lookup"><span data-stu-id="c3347-134">HEAD</span></span>
- <span data-ttu-id="c3347-135">삭제</span><span class="sxs-lookup"><span data-stu-id="c3347-135">DELETE</span></span>

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

### <span data-ttu-id="c3347-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="c3347-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="c3347-137">저장소 작업 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="c3347-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="c3347-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="c3347-139">올리기 및 게시 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="c3347-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="c3347-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="c3347-141">저장소 큐에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="c3347-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3347-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="c3347-143">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="c3347-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c3347-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="c3347-145">저장소 큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="c3347-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="c3347-146">-ErrorActionURI</span></span>
<span data-ttu-id="c3347-147">오류 작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="c3347-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c3347-148">-ExecutionCount</span></span>
<span data-ttu-id="c3347-149">실행 되는 작업의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="c3347-150">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-150">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-151">-빈도</span><span class="sxs-lookup"><span data-stu-id="c3347-151">-Frequency</span></span>
<span data-ttu-id="c3347-152">이 스케줄러 작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-152">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-153">-헤더</span><span class="sxs-lookup"><span data-stu-id="c3347-153">-Headers</span></span>
<span data-ttu-id="c3347-154">헤더를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="c3347-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c3347-155">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-156">-Interval</span><span class="sxs-lookup"><span data-stu-id="c3347-156">-Interval</span></span>
<span data-ttu-id="c3347-157">*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c3347-158">-JobCollectionName</span></span>
<span data-ttu-id="c3347-159">수정할 스케줄러 작업을 포함 하는 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="c3347-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="c3347-160">-JobName</span></span>
<span data-ttu-id="c3347-161">수정할 스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="c3347-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="c3347-162">-JobState</span></span>
<span data-ttu-id="c3347-163">스케줄러 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="c3347-164">-위치</span><span class="sxs-lookup"><span data-stu-id="c3347-164">-Location</span></span>
<span data-ttu-id="c3347-165">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="c3347-166">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-166">Valid values are:</span></span> 

- <span data-ttu-id="c3347-167">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="c3347-167">Anywhere Asia</span></span>
- <span data-ttu-id="c3347-168">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="c3347-168">Anywhere Europe</span></span>
- <span data-ttu-id="c3347-169">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="c3347-169">Anywhere US</span></span>
- <span data-ttu-id="c3347-170">동아시아</span><span class="sxs-lookup"><span data-stu-id="c3347-170">East Asia</span></span>
- <span data-ttu-id="c3347-171">미국 동부</span><span class="sxs-lookup"><span data-stu-id="c3347-171">East US</span></span>
- <span data-ttu-id="c3347-172">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="c3347-172">North Central US</span></span>
- <span data-ttu-id="c3347-173">동유럽</span><span class="sxs-lookup"><span data-stu-id="c3347-173">North Europe</span></span>
- <span data-ttu-id="c3347-174">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="c3347-174">South Central US</span></span>
- <span data-ttu-id="c3347-175">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="c3347-175">Southeast Asia</span></span>
- <span data-ttu-id="c3347-176">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="c3347-176">West Europe</span></span>
- <span data-ttu-id="c3347-177">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="c3347-177">West US</span></span>

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

### <span data-ttu-id="c3347-178">-메서드</span><span class="sxs-lookup"><span data-stu-id="c3347-178">-Method</span></span>
<span data-ttu-id="c3347-179">HTTP 및 HTTPS 동작 형식에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="c3347-180">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-180">Valid values are:</span></span> 

- <span data-ttu-id="c3347-181">가져오기</span><span class="sxs-lookup"><span data-stu-id="c3347-181">GET</span></span>
- <span data-ttu-id="c3347-182">저장할</span><span class="sxs-lookup"><span data-stu-id="c3347-182">PUT</span></span>
- <span data-ttu-id="c3347-183">올리기</span><span class="sxs-lookup"><span data-stu-id="c3347-183">POST</span></span>
- <span data-ttu-id="c3347-184">부분</span><span class="sxs-lookup"><span data-stu-id="c3347-184">HEAD</span></span>
- <span data-ttu-id="c3347-185">삭제</span><span class="sxs-lookup"><span data-stu-id="c3347-185">DELETE</span></span>

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

### <span data-ttu-id="c3347-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3347-186">-PassThru</span></span>
<span data-ttu-id="c3347-187">이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="c3347-188">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3347-189">-프로필</span><span class="sxs-lookup"><span data-stu-id="c3347-189">-Profile</span></span>
<span data-ttu-id="c3347-190">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3347-191">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3347-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="c3347-192">-RequestBody</span></span>
<span data-ttu-id="c3347-193">올리기 및 게시 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-193">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3347-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c3347-194">-StartTime</span></span>
<span data-ttu-id="c3347-195">작업을 시작 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="c3347-196">-URI</span><span class="sxs-lookup"><span data-stu-id="c3347-196">-URI</span></span>
<span data-ttu-id="c3347-197">작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="c3347-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3347-198">CommonParameters</span></span>
<span data-ttu-id="c3347-199">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3347-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3347-200">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3347-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3347-201">입력</span><span class="sxs-lookup"><span data-stu-id="c3347-201">INPUTS</span></span>

## <span data-ttu-id="c3347-202">출력</span><span class="sxs-lookup"><span data-stu-id="c3347-202">OUTPUTS</span></span>

## <span data-ttu-id="c3347-203">상속자</span><span class="sxs-lookup"><span data-stu-id="c3347-203">NOTES</span></span>

## <span data-ttu-id="c3347-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3347-204">RELATED LINKS</span></span>

[<span data-ttu-id="c3347-205">새로운 AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c3347-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


