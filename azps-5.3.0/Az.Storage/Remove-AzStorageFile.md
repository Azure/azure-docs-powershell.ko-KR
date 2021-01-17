---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491299"
---
# <span data-ttu-id="498cd-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="498cd-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="498cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="498cd-102">SYNOPSIS</span></span>
<span data-ttu-id="498cd-103">파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-103">Deletes a file.</span></span>

## <span data-ttu-id="498cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="498cd-104">SYNTAX</span></span>

### <span data-ttu-id="498cd-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="498cd-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="498cd-106">공유</span><span class="sxs-lookup"><span data-stu-id="498cd-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498cd-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="498cd-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="498cd-108">파일</span><span class="sxs-lookup"><span data-stu-id="498cd-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="498cd-109">설명</span><span class="sxs-lookup"><span data-stu-id="498cd-109">DESCRIPTION</span></span>
<span data-ttu-id="498cd-110">**Remove-AzStorageFile** cmdlet은 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="498cd-111">예제</span><span class="sxs-lookup"><span data-stu-id="498cd-111">EXAMPLES</span></span>

### <span data-ttu-id="498cd-112">예제 1: 파일 공유에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="498cd-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="498cd-113">이 명령은 ContosoShare06이라는 파일 공유에서 ContosoFile22라는 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="498cd-114">예제 2: 파일 공유 개체를 사용하여 파일 공유에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="498cd-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="498cd-115">이 명령은 **Get-AzStorageShare** cmdlet을 사용하여 ContosoShare06이라는 파일 공유를 얻은 다음 파이프라인 연산자를 사용하여 해당 개체를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="498cd-116">현재 명령은 ContosoShare06에서 ContosoFile22라는 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="498cd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="498cd-117">PARAMETERS</span></span>

### <span data-ttu-id="498cd-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="498cd-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="498cd-119">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="498cd-120">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="498cd-121">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="498cd-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="498cd-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="498cd-123">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="498cd-124">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="498cd-125">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="498cd-126">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="498cd-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-127">The default value is 10.</span></span>

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

### <span data-ttu-id="498cd-128">-Context</span><span class="sxs-lookup"><span data-stu-id="498cd-128">-Context</span></span>
<span data-ttu-id="498cd-129">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="498cd-130">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="498cd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498cd-131">-DefaultProfile</span></span>
<span data-ttu-id="498cd-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498cd-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="498cd-133">-Directory</span></span>
<span data-ttu-id="498cd-134">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="498cd-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="498cd-135">이 cmdlet은 이 매개 변수가 지정하는 폴더의 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498cd-136">-File</span><span class="sxs-lookup"><span data-stu-id="498cd-136">-File</span></span>
<span data-ttu-id="498cd-137">파일을 **CloudFile 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="498cd-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="498cd-138">이 cmdlet은 이 매개 변수가 지정하는 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="498cd-139">**CloudFile** 개체를 얻습니다. Get-AzStorageFile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="498cd-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="498cd-140">-PassThru</span></span>
<span data-ttu-id="498cd-141">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="498cd-142">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="498cd-143">-Path</span><span class="sxs-lookup"><span data-stu-id="498cd-143">-Path</span></span>
<span data-ttu-id="498cd-144">파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-144">Specifies the path of a file.</span></span>
<span data-ttu-id="498cd-145">이 cmdlet은 이 매개 변수가 지정하는 파일을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498cd-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="498cd-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="498cd-147">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="498cd-148">-공유</span><span class="sxs-lookup"><span data-stu-id="498cd-148">-Share</span></span>
<span data-ttu-id="498cd-149">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="498cd-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="498cd-150">이 cmdlet은 이 매개 변수가 지정하는 공유의 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="498cd-151">**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="498cd-152">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-152">This object contains the storage context.</span></span>
<span data-ttu-id="498cd-153">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498cd-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="498cd-154">-ShareName</span></span>
<span data-ttu-id="498cd-155">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="498cd-156">이 cmdlet은 이 매개 변수가 지정하는 공유의 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="498cd-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="498cd-157">-Confirm</span></span>
<span data-ttu-id="498cd-158">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498cd-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498cd-159">-WhatIf</span></span>
<span data-ttu-id="498cd-160">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="498cd-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498cd-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498cd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498cd-162">CommonParameters</span></span>
<span data-ttu-id="498cd-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="498cd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498cd-164">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="498cd-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498cd-165">입력</span><span class="sxs-lookup"><span data-stu-id="498cd-165">INPUTS</span></span>

### <span data-ttu-id="498cd-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="498cd-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="498cd-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="498cd-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="498cd-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="498cd-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="498cd-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="498cd-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="498cd-170">출력</span><span class="sxs-lookup"><span data-stu-id="498cd-170">OUTPUTS</span></span>

### <span data-ttu-id="498cd-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="498cd-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="498cd-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="498cd-172">NOTES</span></span>

## <span data-ttu-id="498cd-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="498cd-173">RELATED LINKS</span></span>

[<span data-ttu-id="498cd-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="498cd-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="498cd-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="498cd-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="498cd-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="498cd-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
