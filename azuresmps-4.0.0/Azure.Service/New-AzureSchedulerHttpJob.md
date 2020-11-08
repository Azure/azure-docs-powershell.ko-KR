---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045904"
---
# <span data-ttu-id="5a90a-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="5a90a-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="5a90a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a90a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a90a-103">HTTP 작업이 있는 스케줄러 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="5a90a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a90a-104">SYNTAX</span></span>

### <span data-ttu-id="5a90a-105">필수</span><span class="sxs-lookup"><span data-stu-id="5a90a-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a90a-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="5a90a-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a90a-107">정기</span><span class="sxs-lookup"><span data-stu-id="5a90a-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a90a-108">인증서</span><span class="sxs-lookup"><span data-stu-id="5a90a-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a90a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5a90a-109">DESCRIPTION</span></span>
<span data-ttu-id="5a90a-110">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5a90a-111">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5a90a-112">**AzureSchedulerHttpJob** CMDLET은 HTTP 작업이 있는 스케줄러 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="5a90a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5a90a-113">EXAMPLES</span></span>

### <span data-ttu-id="5a90a-114">예제 1: HTTP 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5a90a-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="5a90a-115">이 명령은 JobCollection01 이라는 작업 컬렉션에 스케줄러 HTTP 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="5a90a-116">명령에서 URI를 지정 하 고 메서드로 가져오기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="5a90a-117">예제 2: 특정 실행 횟수에 대 한 HTTP 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5a90a-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="5a90a-118">이 명령은 JobCollection01 이라는 작업 컬렉션에 스케줄러 http 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="5a90a-119">명령에서 URI를 지정 하 고 메서드로 가져오기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="5a90a-120">이 명령은 작업이 20 번 실행 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="5a90a-121">변수</span><span class="sxs-lookup"><span data-stu-id="5a90a-121">PARAMETERS</span></span>

### <span data-ttu-id="5a90a-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="5a90a-122">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="5a90a-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="5a90a-123">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="5a90a-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5a90a-124">-EndTime</span></span>
<span data-ttu-id="5a90a-125">스케줄러에서 시작 작업을 중지 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="5a90a-126">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5a90a-127">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a90a-127">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5a90a-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="5a90a-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="5a90a-129">헤더를 hashtable로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="5a90a-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="5a90a-130">-ErrorActionMethod</span></span>
<span data-ttu-id="5a90a-131">HTTP 및 HTTPS 동작 형식에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="5a90a-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-132">Valid values are:</span></span> 

- <span data-ttu-id="5a90a-133">가져오기</span><span class="sxs-lookup"><span data-stu-id="5a90a-133">GET</span></span>
- <span data-ttu-id="5a90a-134">저장할</span><span class="sxs-lookup"><span data-stu-id="5a90a-134">PUT</span></span>
- <span data-ttu-id="5a90a-135">올리기</span><span class="sxs-lookup"><span data-stu-id="5a90a-135">POST</span></span>
- <span data-ttu-id="5a90a-136">부분</span><span class="sxs-lookup"><span data-stu-id="5a90a-136">HEAD</span></span>
- <span data-ttu-id="5a90a-137">삭제</span><span class="sxs-lookup"><span data-stu-id="5a90a-137">DELETE</span></span>

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

### <span data-ttu-id="5a90a-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="5a90a-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="5a90a-139">저장소 작업 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="5a90a-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="5a90a-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="5a90a-141">올리기 및 게시 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="5a90a-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="5a90a-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="5a90a-143">저장소 큐에 대 한 SAS (공유 액세스 서명) 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="5a90a-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a90a-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="5a90a-145">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="5a90a-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5a90a-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="5a90a-147">저장소 큐의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="5a90a-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="5a90a-148">-ErrorActionURI</span></span>
<span data-ttu-id="5a90a-149">오류 작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="5a90a-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="5a90a-150">-ExecutionCount</span></span>
<span data-ttu-id="5a90a-151">실행 되는 작업의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="5a90a-152">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-152">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="5a90a-153">-빈도</span><span class="sxs-lookup"><span data-stu-id="5a90a-153">-Frequency</span></span>
<span data-ttu-id="5a90a-154">이 스케줄러 작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-154">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="5a90a-155">-헤더</span><span class="sxs-lookup"><span data-stu-id="5a90a-155">-Headers</span></span>
<span data-ttu-id="5a90a-156">헤더를 hashtable로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="5a90a-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="5a90a-157">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="5a90a-158">-Interval</span><span class="sxs-lookup"><span data-stu-id="5a90a-158">-Interval</span></span>
<span data-ttu-id="5a90a-159">*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="5a90a-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="5a90a-160">-JobCollectionName</span></span>
<span data-ttu-id="5a90a-161">스케줄러 작업을 포함할 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="5a90a-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="5a90a-162">-JobName</span></span>
<span data-ttu-id="5a90a-163">스케줄러 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="5a90a-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="5a90a-164">-JobState</span></span>
<span data-ttu-id="5a90a-165">스케줄러 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="5a90a-166">-위치</span><span class="sxs-lookup"><span data-stu-id="5a90a-166">-Location</span></span>
<span data-ttu-id="5a90a-167">클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="5a90a-168">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-168">Valid values are:</span></span> 

- <span data-ttu-id="5a90a-169">아시아 어디서 나</span><span class="sxs-lookup"><span data-stu-id="5a90a-169">Anywhere Asia</span></span>
- <span data-ttu-id="5a90a-170">유럽 어디서 나</span><span class="sxs-lookup"><span data-stu-id="5a90a-170">Anywhere Europe</span></span>
- <span data-ttu-id="5a90a-171">미국 어디서 나</span><span class="sxs-lookup"><span data-stu-id="5a90a-171">Anywhere US</span></span>
- <span data-ttu-id="5a90a-172">동아시아</span><span class="sxs-lookup"><span data-stu-id="5a90a-172">East Asia</span></span>
- <span data-ttu-id="5a90a-173">미국 동부</span><span class="sxs-lookup"><span data-stu-id="5a90a-173">East US</span></span>
- <span data-ttu-id="5a90a-174">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="5a90a-174">North Central US</span></span>
- <span data-ttu-id="5a90a-175">동유럽</span><span class="sxs-lookup"><span data-stu-id="5a90a-175">North Europe</span></span>
- <span data-ttu-id="5a90a-176">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="5a90a-176">South Central US</span></span>
- <span data-ttu-id="5a90a-177">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="5a90a-177">Southeast Asia</span></span>
- <span data-ttu-id="5a90a-178">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="5a90a-178">West Europe</span></span>
- <span data-ttu-id="5a90a-179">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="5a90a-179">West US</span></span>

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

### <span data-ttu-id="5a90a-180">-메서드</span><span class="sxs-lookup"><span data-stu-id="5a90a-180">-Method</span></span>
<span data-ttu-id="5a90a-181">HTTP 및 HTTPS 동작 형식에 대 한 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="5a90a-182">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-182">Valid values are:</span></span> 

- <span data-ttu-id="5a90a-183">가져오기</span><span class="sxs-lookup"><span data-stu-id="5a90a-183">GET</span></span>
- <span data-ttu-id="5a90a-184">저장할</span><span class="sxs-lookup"><span data-stu-id="5a90a-184">PUT</span></span>
- <span data-ttu-id="5a90a-185">올리기</span><span class="sxs-lookup"><span data-stu-id="5a90a-185">POST</span></span>
- <span data-ttu-id="5a90a-186">부분</span><span class="sxs-lookup"><span data-stu-id="5a90a-186">HEAD</span></span>
- <span data-ttu-id="5a90a-187">삭제</span><span class="sxs-lookup"><span data-stu-id="5a90a-187">DELETE</span></span>

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

### <span data-ttu-id="5a90a-188">-프로필</span><span class="sxs-lookup"><span data-stu-id="5a90a-188">-Profile</span></span>
<span data-ttu-id="5a90a-189">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a90a-190">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a90a-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="5a90a-191">-RequestBody</span></span>
<span data-ttu-id="5a90a-192">올리기 및 게시 작업의 본문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-192">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="5a90a-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5a90a-193">-StartTime</span></span>
<span data-ttu-id="5a90a-194">작업을 시작 하는 데 사용할 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="5a90a-195">-URI</span><span class="sxs-lookup"><span data-stu-id="5a90a-195">-URI</span></span>
<span data-ttu-id="5a90a-196">작업 작업에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a90a-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a90a-197">CommonParameters</span></span>
<span data-ttu-id="5a90a-198">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a90a-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a90a-199">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a90a-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a90a-200">입력</span><span class="sxs-lookup"><span data-stu-id="5a90a-200">INPUTS</span></span>

## <span data-ttu-id="5a90a-201">출력</span><span class="sxs-lookup"><span data-stu-id="5a90a-201">OUTPUTS</span></span>

## <span data-ttu-id="5a90a-202">상속자</span><span class="sxs-lookup"><span data-stu-id="5a90a-202">NOTES</span></span>

## <span data-ttu-id="5a90a-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a90a-203">RELATED LINKS</span></span>

[<span data-ttu-id="5a90a-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="5a90a-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


