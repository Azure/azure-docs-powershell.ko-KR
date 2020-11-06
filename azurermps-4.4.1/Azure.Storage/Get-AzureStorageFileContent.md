---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a04a035e0fedfa4bca00eceda1dcf8dba0680c0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533235"
---
# <span data-ttu-id="2882f-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2882f-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="2882f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2882f-102">SYNOPSIS</span></span>
<span data-ttu-id="2882f-103">파일의 내용을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2882f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2882f-104">SYNTAX</span></span>

### <span data-ttu-id="2882f-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2882f-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2882f-106">공유</span><span class="sxs-lookup"><span data-stu-id="2882f-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2882f-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="2882f-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2882f-108">파일</span><span class="sxs-lookup"><span data-stu-id="2882f-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2882f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2882f-109">DESCRIPTION</span></span>
<span data-ttu-id="2882f-110">**AzureStorageFileContent** cmdlet은 파일의 콘텐츠를 다운로드 한 다음 지정 된 대상에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="2882f-111">이 cmdlet은 파일의 내용을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="2882f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2882f-112">EXAMPLES</span></span>

### <span data-ttu-id="2882f-113">예제 1: 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="2882f-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="2882f-114">이 명령은 파일 공유 ContosoShare06에서 현재 폴더로 ContosoWorkingFolder 폴더의 CurrentDataFile 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="2882f-115">예제 2: 샘플 파일 공유 아래에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="2882f-116">이 예제에서는 예제 파일 공유 아래에 있는 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="2882f-117">변수</span><span class="sxs-lookup"><span data-stu-id="2882f-117">PARAMETERS</span></span>

### <span data-ttu-id="2882f-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="2882f-118">-CheckMd5</span></span>
<span data-ttu-id="2882f-119">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-120">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-121">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-122">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2882f-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2882f-124">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-125">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-126">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-127">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2882f-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2882f-129">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-130">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-131">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-132">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-133">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2882f-133">-Context</span></span>
<span data-ttu-id="2882f-134">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-135">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-136">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-137">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-138">-대상</span><span class="sxs-lookup"><span data-stu-id="2882f-138">-Destination</span></span>
<span data-ttu-id="2882f-139">대상 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-139">Specifies the destination path.</span></span>
<span data-ttu-id="2882f-140">이 cmdlet은이 매개 변수에서 지정 하는 위치에 파일 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="2882f-141">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-142">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-143">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-144">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2882f-145">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="2882f-145">-Directory</span></span>
<span data-ttu-id="2882f-146">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2882f-147">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일에 대 한 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="2882f-148">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2882f-149">또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="2882f-150">-파일</span><span class="sxs-lookup"><span data-stu-id="2882f-150">-File</span></span>
<span data-ttu-id="2882f-151">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="2882f-152">이 cmdlet은이 매개 변수에서 지정 하는 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="2882f-153">**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="2882f-154">-Force</span><span class="sxs-lookup"><span data-stu-id="2882f-154">-Force</span></span>
<span data-ttu-id="2882f-155">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-156">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-157">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-158">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2882f-159">-PassThru</span></span>
<span data-ttu-id="2882f-160">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-161">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-162">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-163">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-164">-Path</span><span class="sxs-lookup"><span data-stu-id="2882f-164">-Path</span></span>
<span data-ttu-id="2882f-165">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-165">Specifies the path of a file.</span></span>
<span data-ttu-id="2882f-166">이 cmdlet은이 매개 변수에서 지정 하는 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="2882f-167">파일이 없는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-167">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2882f-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2882f-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2882f-169">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2882f-170">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2882f-171">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="2882f-172">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2882f-173">-공유</span><span class="sxs-lookup"><span data-stu-id="2882f-173">-Share</span></span>
<span data-ttu-id="2882f-174">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2882f-175">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="2882f-176">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="2882f-177">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-177">This object contains the storage context.</span></span>
<span data-ttu-id="2882f-178">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="2882f-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2882f-179">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2882f-179">-ShareName</span></span>
<span data-ttu-id="2882f-180">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="2882f-181">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="2882f-182">-확인</span><span class="sxs-lookup"><span data-stu-id="2882f-182">-Confirm</span></span>
<span data-ttu-id="2882f-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2882f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2882f-184">-WhatIf</span></span>
<span data-ttu-id="2882f-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2882f-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2882f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2882f-187">CommonParameters</span></span>
<span data-ttu-id="2882f-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2882f-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2882f-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2882f-190">입력</span><span class="sxs-lookup"><span data-stu-id="2882f-190">INPUTS</span></span>

### <span data-ttu-id="2882f-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2882f-191">IStorageContext</span></span>

<span data-ttu-id="2882f-192">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2882f-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2882f-193">CloudFileDirectory</span></span>

<span data-ttu-id="2882f-194">' Directory ' 매개 변수는 파이프라인에서 ' CloudFileDirectory ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="2882f-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="2882f-195">CloudFile</span></span>

<span data-ttu-id="2882f-196">' File ' 매개 변수는 파이프라인에서 ' CloudFile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="2882f-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2882f-197">CloudFileShare</span></span>

<span data-ttu-id="2882f-198">' Share ' 매개 변수는 파이프라인에서 ' CloudFileShare 범위 ' 형식의 값을 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="2882f-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="2882f-199">출력</span><span class="sxs-lookup"><span data-stu-id="2882f-199">OUTPUTS</span></span>

## <span data-ttu-id="2882f-200">상속자</span><span class="sxs-lookup"><span data-stu-id="2882f-200">NOTES</span></span>

## <span data-ttu-id="2882f-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2882f-201">RELATED LINKS</span></span>

[<span data-ttu-id="2882f-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="2882f-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="2882f-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2882f-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


