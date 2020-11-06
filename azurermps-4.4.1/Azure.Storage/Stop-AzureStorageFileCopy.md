---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 5fa3d3ee36b2abe356ec3e944bb96ac142da7410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527760"
---
# <span data-ttu-id="d4730-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4730-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="d4730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4730-102">SYNOPSIS</span></span>
<span data-ttu-id="d4730-103">지정 된 대상 파일에 대 한 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4730-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4730-104">SYNTAX</span></span>

### <span data-ttu-id="d4730-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="d4730-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4730-106">파일</span><span class="sxs-lookup"><span data-stu-id="d4730-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4730-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d4730-107">DESCRIPTION</span></span>
<span data-ttu-id="d4730-108">**AzureStorageFileCopy** cmdlet은 대상 파일에 대 한 파일 복사를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="d4730-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d4730-109">EXAMPLES</span></span>

### <span data-ttu-id="d4730-110">예제 1: 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="d4730-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="d4730-111">이 명령은 지정 된 이름을 가진 파일의 복사를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="d4730-112">변수</span><span class="sxs-lookup"><span data-stu-id="d4730-112">PARAMETERS</span></span>

### <span data-ttu-id="d4730-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d4730-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d4730-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d4730-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d4730-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d4730-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d4730-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d4730-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d4730-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d4730-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d4730-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d4730-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d4730-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d4730-123">-Context</span></span>
<span data-ttu-id="d4730-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d4730-125">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d4730-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="d4730-126">-CopyId</span></span>
<span data-ttu-id="d4730-127">복사 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="d4730-128">-파일</span><span class="sxs-lookup"><span data-stu-id="d4730-128">-File</span></span>
<span data-ttu-id="d4730-129">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d4730-130">클라우드 파일을 만들거나 Get-AzureStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="d4730-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d4730-131">-FilePath</span></span>
<span data-ttu-id="d4730-132">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-132">Specifies the path of a file.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4730-133">-Force</span><span class="sxs-lookup"><span data-stu-id="d4730-133">-Force</span></span>
<span data-ttu-id="d4730-134">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4730-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d4730-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d4730-136">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d4730-137">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d4730-137">-ShareName</span></span>
<span data-ttu-id="d4730-138">공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-138">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="d4730-139">-확인</span><span class="sxs-lookup"><span data-stu-id="d4730-139">-Confirm</span></span>
<span data-ttu-id="d4730-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4730-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4730-141">-WhatIf</span></span>
<span data-ttu-id="d4730-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4730-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4730-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4730-144">CommonParameters</span></span>
<span data-ttu-id="d4730-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4730-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4730-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4730-147">입력</span><span class="sxs-lookup"><span data-stu-id="d4730-147">INPUTS</span></span>

### <span data-ttu-id="d4730-148">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4730-148">IStorageContext</span></span>

<span data-ttu-id="d4730-149">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-149">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d4730-150">CloudFile</span><span class="sxs-lookup"><span data-stu-id="d4730-150">CloudFile</span></span>

<span data-ttu-id="d4730-151">' File ' 매개 변수는 파이프라인에서 ' CloudFile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4730-151">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="d4730-152">출력</span><span class="sxs-lookup"><span data-stu-id="d4730-152">OUTPUTS</span></span>

## <span data-ttu-id="d4730-153">상속자</span><span class="sxs-lookup"><span data-stu-id="d4730-153">NOTES</span></span>

## <span data-ttu-id="d4730-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4730-154">RELATED LINKS</span></span>

[<span data-ttu-id="d4730-155">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="d4730-155">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="d4730-156">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="d4730-156">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="d4730-157">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4730-157">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d4730-158">시작-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4730-158">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
