---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348518"
---
# <span data-ttu-id="01e1d-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="01e1d-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="01e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="01e1d-103">디렉터리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-103">Deletes a directory.</span></span>

## <span data-ttu-id="01e1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="01e1d-104">SYNTAX</span></span>

### <span data-ttu-id="01e1d-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="01e1d-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01e1d-106">공유</span><span class="sxs-lookup"><span data-stu-id="01e1d-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01e1d-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="01e1d-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01e1d-108">설명</span><span class="sxs-lookup"><span data-stu-id="01e1d-108">DESCRIPTION</span></span>
<span data-ttu-id="01e1d-109">**Remove-AzStorageDirectory** cmdlet은 디렉터리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="01e1d-110">예제</span><span class="sxs-lookup"><span data-stu-id="01e1d-110">EXAMPLES</span></span>

### <span data-ttu-id="01e1d-111">예제 1: 폴더 삭제</span><span class="sxs-lookup"><span data-stu-id="01e1d-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="01e1d-112">이 명령은 ContosoShare06이라는 파일 공유에서 ContosoWorkingFolder라는 폴더를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="01e1d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e1d-113">PARAMETERS</span></span>

### <span data-ttu-id="01e1d-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="01e1d-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="01e1d-115">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="01e1d-116">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="01e1d-117">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="01e1d-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="01e1d-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="01e1d-119">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="01e1d-120">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="01e1d-121">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="01e1d-122">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="01e1d-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-123">The default value is 10.</span></span>

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

### <span data-ttu-id="01e1d-124">-Context</span><span class="sxs-lookup"><span data-stu-id="01e1d-124">-Context</span></span>
<span data-ttu-id="01e1d-125">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="01e1d-126">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="01e1d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e1d-127">-DefaultProfile</span></span>
<span data-ttu-id="01e1d-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e1d-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="01e1d-129">-Directory</span></span>
<span data-ttu-id="01e1d-130">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="01e1d-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="01e1d-131">이 cmdlet은 이 매개 변수가 지정하는 폴더를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="01e1d-132">디렉터리를 얻습니다. New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="01e1d-133">**Get-AzStorageFile** cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="01e1d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e1d-134">-PassThru</span></span>
<span data-ttu-id="01e1d-135">이 cmdlet이 성공하면 이 cmdlet이 $True.</span><span class="sxs-lookup"><span data-stu-id="01e1d-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="01e1d-136">이 매개 변수를 지정하고 _Path_ 매개 변수에 대한 부적절한 값으로 cmdlet이 실패한 경우 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="01e1d-137">이 매개 변수를 지정하지 않으면 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="01e1d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="01e1d-138">-Path</span></span>
<span data-ttu-id="01e1d-139">폴더의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="01e1d-140">이 매개 변수가 지정하는 폴더가 비어 있는 경우 이 cmdlet은 해당 폴더를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="01e1d-141">폴더가 비어 있지 않은 경우 이 cmdlet은 변경하지 못하고 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e1d-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="01e1d-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="01e1d-143">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="01e1d-144">-공유</span><span class="sxs-lookup"><span data-stu-id="01e1d-144">-Share</span></span>
<span data-ttu-id="01e1d-145">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="01e1d-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="01e1d-146">이 cmdlet은 이 매개 변수가 지정하는 파일 공유 아래에 있는 폴더를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="01e1d-147">**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="01e1d-148">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-148">This object contains the storage context.</span></span>
<span data-ttu-id="01e1d-149">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="01e1d-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="01e1d-150">-ShareName</span></span>
<span data-ttu-id="01e1d-151">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="01e1d-152">이 cmdlet은 이 매개 변수가 지정하는 파일 공유 아래에 있는 폴더를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="01e1d-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e1d-153">-Confirm</span></span>
<span data-ttu-id="01e1d-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e1d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e1d-155">-WhatIf</span></span>
<span data-ttu-id="01e1d-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="01e1d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e1d-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e1d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e1d-158">CommonParameters</span></span>
<span data-ttu-id="01e1d-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e1d-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01e1d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e1d-161">입력</span><span class="sxs-lookup"><span data-stu-id="01e1d-161">INPUTS</span></span>

### <span data-ttu-id="01e1d-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="01e1d-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="01e1d-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="01e1d-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="01e1d-164">System.String</span><span class="sxs-lookup"><span data-stu-id="01e1d-164">System.String</span></span>

### <span data-ttu-id="01e1d-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01e1d-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="01e1d-166">출력</span><span class="sxs-lookup"><span data-stu-id="01e1d-166">OUTPUTS</span></span>

### <span data-ttu-id="01e1d-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="01e1d-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="01e1d-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01e1d-168">NOTES</span></span>

## <span data-ttu-id="01e1d-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01e1d-169">RELATED LINKS</span></span>

[<span data-ttu-id="01e1d-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="01e1d-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="01e1d-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="01e1d-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="01e1d-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="01e1d-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
