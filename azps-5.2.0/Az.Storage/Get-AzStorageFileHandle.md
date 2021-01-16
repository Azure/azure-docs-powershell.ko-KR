---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349629"
---
# <span data-ttu-id="7e81d-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7e81d-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="7e81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e81d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e81d-103">파일 공유, 파일 디렉터리 또는 파일의 파일 핸들을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="7e81d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e81d-104">SYNTAX</span></span>

### <span data-ttu-id="7e81d-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e81d-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7e81d-106">공유</span><span class="sxs-lookup"><span data-stu-id="7e81d-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7e81d-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="7e81d-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7e81d-108">파일</span><span class="sxs-lookup"><span data-stu-id="7e81d-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7e81d-109">설명</span><span class="sxs-lookup"><span data-stu-id="7e81d-109">DESCRIPTION</span></span>
<span data-ttu-id="7e81d-110">**Get-AzStorageFileHandle cmdlet은** 파일 공유 또는 파일 디렉터리 또는 파일의 파일 핸들을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="7e81d-111">예제</span><span class="sxs-lookup"><span data-stu-id="7e81d-111">EXAMPLES</span></span>

### <span data-ttu-id="7e81d-112">예제 1: 파일 공유의 모든 파일 핸들을 재발적으로 나열하고 ClientIp 및 OpenTime별로 정렬</span><span class="sxs-lookup"><span data-stu-id="7e81d-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="7e81d-113">이 명령은 파일 공유에 대한 파일 핸들을 나열하고 ClientIp를 사용하여 출력을 정렬한 다음 OpenTime별로 정렬합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="7e81d-114">예제 2: 파일 디렉터리에 재발적으로 처음 2개 파일 핸들 나열</span><span class="sxs-lookup"><span data-stu-id="7e81d-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="7e81d-115">이 명령은 파일 디렉터리에 대한 처음 2개 파일 핸들을 재발적으로 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="7e81d-116">예제 3: 파일의 6번째 파일 핸들에 대한 세 번째 항목 나열</span><span class="sxs-lookup"><span data-stu-id="7e81d-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="7e81d-117">이 명령은 파일의 6번째 파일 핸들에 대한 세 번째 핸들을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="7e81d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e81d-118">PARAMETERS</span></span>

### <span data-ttu-id="7e81d-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e81d-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7e81d-120">각 요청에 대한 클라이언트 쪽 최대 실행 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="7e81d-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7e81d-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7e81d-122">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="7e81d-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-123">The default value is 10.</span></span>

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

### <span data-ttu-id="7e81d-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7e81d-124">-Context</span></span>
<span data-ttu-id="7e81d-125">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="7e81d-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="7e81d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e81d-126">-DefaultProfile</span></span>
<span data-ttu-id="7e81d-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e81d-128">-Directory</span><span class="sxs-lookup"><span data-stu-id="7e81d-128">-Directory</span></span>
<span data-ttu-id="7e81d-129">CloudFileDirectory 개체는 파일/directories가 나열되는 기본 폴더를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="7e81d-130">-File</span><span class="sxs-lookup"><span data-stu-id="7e81d-130">-File</span></span>
<span data-ttu-id="7e81d-131">CloudFile 개체는 파일 핸들을 나열할 파일을 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-131">CloudFile object indicated the file to list File Handles.</span></span>

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

### <span data-ttu-id="7e81d-132">-Path</span><span class="sxs-lookup"><span data-stu-id="7e81d-132">-Path</span></span>
<span data-ttu-id="7e81d-133">기존 파일/디렉터리에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e81d-134">-Recursive</span><span class="sxs-lookup"><span data-stu-id="7e81d-134">-Recursive</span></span>
<span data-ttu-id="7e81d-135">목록은 재발적으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-135">List handles Recursively.</span></span>
<span data-ttu-id="7e81d-136">파일 디렉터리에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="7e81d-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e81d-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7e81d-138">각 요청에 대한 서버 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="7e81d-139">-공유</span><span class="sxs-lookup"><span data-stu-id="7e81d-139">-Share</span></span>
<span data-ttu-id="7e81d-140">CloudFileShare 개체는 파일/감독이 나열될 공유를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="7e81d-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7e81d-141">-ShareName</span></span>
<span data-ttu-id="7e81d-142">파일/폴더가 나열될 파일 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="7e81d-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7e81d-143">-IncludeTotalCount</span></span>
<span data-ttu-id="7e81d-144">데이터 집합(정수)과 개체의 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="7e81d-145">cmdlet에서 총 개수를 확인할 수 없는 경우 '알 수 없는 총 수'가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="7e81d-146">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7e81d-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="7e81d-147">-Skip</span></span>
<span data-ttu-id="7e81d-148">첫 번째 'n' 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e81d-149">-First</span><span class="sxs-lookup"><span data-stu-id="7e81d-149">-First</span></span>
<span data-ttu-id="7e81d-150">첫 번째 'n' 개체만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e81d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e81d-151">CommonParameters</span></span>
<span data-ttu-id="7e81d-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e81d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e81d-153">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7e81d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e81d-154">입력</span><span class="sxs-lookup"><span data-stu-id="7e81d-154">INPUTS</span></span>

### <span data-ttu-id="7e81d-155">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7e81d-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="7e81d-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7e81d-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="7e81d-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e81d-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e81d-158">출력</span><span class="sxs-lookup"><span data-stu-id="7e81d-158">OUTPUTS</span></span>

### <span data-ttu-id="7e81d-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="7e81d-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="7e81d-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e81d-160">NOTES</span></span>

## <span data-ttu-id="7e81d-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e81d-161">RELATED LINKS</span></span>
