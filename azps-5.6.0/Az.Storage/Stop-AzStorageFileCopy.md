---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: b306b5820e55687c1116adc56b92e1ee5ebd4115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960000"
---
# <span data-ttu-id="75cd2-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="75cd2-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="75cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="75cd2-103">지정된 대상 파일에 대한 복사 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="75cd2-104">구문</span><span class="sxs-lookup"><span data-stu-id="75cd2-104">SYNTAX</span></span>

### <span data-ttu-id="75cd2-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="75cd2-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75cd2-106">파일</span><span class="sxs-lookup"><span data-stu-id="75cd2-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75cd2-107">설명</span><span class="sxs-lookup"><span data-stu-id="75cd2-107">DESCRIPTION</span></span>
<span data-ttu-id="75cd2-108">**Stop-AzStorageFileCopy** cmdlet은 대상 파일에 파일 복사를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="75cd2-109">예제</span><span class="sxs-lookup"><span data-stu-id="75cd2-109">EXAMPLES</span></span>

### <span data-ttu-id="75cd2-110">예제 1: 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="75cd2-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="75cd2-111">이 명령은 지정된 이름이 있는 파일 복사를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="75cd2-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="75cd2-112">PARAMETERS</span></span>

### <span data-ttu-id="75cd2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75cd2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="75cd2-114">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="75cd2-115">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="75cd2-116">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="75cd2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="75cd2-118">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="75cd2-119">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="75cd2-120">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="75cd2-121">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="75cd2-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="75cd2-123">-Context</span><span class="sxs-lookup"><span data-stu-id="75cd2-123">-Context</span></span>
<span data-ttu-id="75cd2-124">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="75cd2-125">저장소 컨텍스트를 구하기 위해 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="75cd2-126">-CopyId</span></span>
<span data-ttu-id="75cd2-127">복사 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="75cd2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cd2-128">-DefaultProfile</span></span>
<span data-ttu-id="75cd2-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-130">-File</span><span class="sxs-lookup"><span data-stu-id="75cd2-130">-File</span></span>
<span data-ttu-id="75cd2-131">**CloudFile 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="75cd2-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="75cd2-132">클라우드 파일을 만들거나 cmdlet을 사용하여 Get-AzStorageFile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="75cd2-133">-FilePath</span></span>
<span data-ttu-id="75cd2-134">파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-135">-Force</span><span class="sxs-lookup"><span data-stu-id="75cd2-135">-Force</span></span>
<span data-ttu-id="75cd2-136">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="75cd2-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="75cd2-138">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-138">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="75cd2-139">-ShareName</span></span>
<span data-ttu-id="75cd2-140">공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cd2-141">-확인</span><span class="sxs-lookup"><span data-stu-id="75cd2-141">-Confirm</span></span>
<span data-ttu-id="75cd2-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cd2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cd2-143">-WhatIf</span></span>
<span data-ttu-id="75cd2-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75cd2-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cd2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cd2-146">CommonParameters</span></span>
<span data-ttu-id="75cd2-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75cd2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cd2-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75cd2-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cd2-149">입력</span><span class="sxs-lookup"><span data-stu-id="75cd2-149">INPUTS</span></span>

### <span data-ttu-id="75cd2-150">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="75cd2-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="75cd2-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="75cd2-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75cd2-152">출력</span><span class="sxs-lookup"><span data-stu-id="75cd2-152">OUTPUTS</span></span>

### <span data-ttu-id="75cd2-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="75cd2-153">System.Void</span></span>

## <span data-ttu-id="75cd2-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75cd2-154">NOTES</span></span>

## <span data-ttu-id="75cd2-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75cd2-155">RELATED LINKS</span></span>

[<span data-ttu-id="75cd2-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="75cd2-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="75cd2-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="75cd2-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="75cd2-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="75cd2-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="75cd2-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="75cd2-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
