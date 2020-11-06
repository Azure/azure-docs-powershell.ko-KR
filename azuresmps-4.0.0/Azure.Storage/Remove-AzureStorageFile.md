---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24b4ddfa86027885b5094b164f24da36e9604900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523544"
---
# <span data-ttu-id="ed76d-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ed76d-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="ed76d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed76d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed76d-103">파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-103">Deletes a file.</span></span>

## <span data-ttu-id="ed76d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed76d-104">SYNTAX</span></span>

### <span data-ttu-id="ed76d-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed76d-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed76d-106">공유</span><span class="sxs-lookup"><span data-stu-id="ed76d-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed76d-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="ed76d-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed76d-108">파일</span><span class="sxs-lookup"><span data-stu-id="ed76d-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed76d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ed76d-109">DESCRIPTION</span></span>
<span data-ttu-id="ed76d-110">**제거-AzureStorageFile** cmdlet은 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="ed76d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ed76d-111">EXAMPLES</span></span>

### <span data-ttu-id="ed76d-112">예제 1: 파일 공유에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="ed76d-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="ed76d-113">이 명령은 ContosoShare06 이라는 파일 공유에서 ContosoFile22 라는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="ed76d-114">예제 2: 파일 공유 개체를 사용 하 여 파일 공유에서 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="ed76d-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="ed76d-115">이 명령은 **AzureStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed76d-116">현재 명령은 ContosoShare06에서 ContosoFile22 라는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="ed76d-117">변수</span><span class="sxs-lookup"><span data-stu-id="ed76d-117">PARAMETERS</span></span>

### <span data-ttu-id="ed76d-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed76d-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ed76d-119">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ed76d-120">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ed76d-121">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ed76d-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ed76d-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ed76d-123">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ed76d-124">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ed76d-125">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ed76d-126">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ed76d-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-127">The default value is 10.</span></span>

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

### <span data-ttu-id="ed76d-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ed76d-128">-Context</span></span>
<span data-ttu-id="ed76d-129">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ed76d-130">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-131">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="ed76d-131">-Directory</span></span>
<span data-ttu-id="ed76d-132">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ed76d-133">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-134">-파일</span><span class="sxs-lookup"><span data-stu-id="ed76d-134">-File</span></span>
<span data-ttu-id="ed76d-135">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="ed76d-136">이 cmdlet은이 매개 변수에서 지정 하는 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="ed76d-137">**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed76d-138">-PassThru</span></span>
<span data-ttu-id="ed76d-139">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ed76d-140">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ed76d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="ed76d-141">-Path</span></span>
<span data-ttu-id="ed76d-142">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-142">Specifies the path of a file.</span></span>
<span data-ttu-id="ed76d-143">이 cmdlet은이 매개 변수에서 지정 하는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ed76d-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ed76d-145">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ed76d-146">-공유</span><span class="sxs-lookup"><span data-stu-id="ed76d-146">-Share</span></span>
<span data-ttu-id="ed76d-147">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ed76d-148">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="ed76d-149">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="ed76d-150">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-150">This object contains the storage context.</span></span>
<span data-ttu-id="ed76d-151">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ed76d-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ed76d-152">-ShareName</span></span>
<span data-ttu-id="ed76d-153">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="ed76d-154">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-155">-확인</span><span class="sxs-lookup"><span data-stu-id="ed76d-155">-Confirm</span></span>
<span data-ttu-id="ed76d-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed76d-157">-WhatIf</span></span>
<span data-ttu-id="ed76d-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed76d-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed76d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed76d-160">CommonParameters</span></span>
<span data-ttu-id="ed76d-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed76d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed76d-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed76d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed76d-163">입력</span><span class="sxs-lookup"><span data-stu-id="ed76d-163">INPUTS</span></span>

## <span data-ttu-id="ed76d-164">출력</span><span class="sxs-lookup"><span data-stu-id="ed76d-164">OUTPUTS</span></span>

## <span data-ttu-id="ed76d-165">상속자</span><span class="sxs-lookup"><span data-stu-id="ed76d-165">NOTES</span></span>

## <span data-ttu-id="ed76d-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed76d-166">RELATED LINKS</span></span>

[<span data-ttu-id="ed76d-167">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ed76d-167">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="ed76d-168">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ed76d-168">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ed76d-169">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ed76d-169">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
