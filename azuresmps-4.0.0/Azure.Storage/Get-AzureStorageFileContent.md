---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524028"
---
# <span data-ttu-id="05428-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="05428-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="05428-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05428-102">SYNOPSIS</span></span>
<span data-ttu-id="05428-103">파일의 내용을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="05428-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05428-104">SYNTAX</span></span>

### <span data-ttu-id="05428-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="05428-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05428-106">공유</span><span class="sxs-lookup"><span data-stu-id="05428-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05428-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="05428-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05428-108">파일</span><span class="sxs-lookup"><span data-stu-id="05428-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05428-109">설명은</span><span class="sxs-lookup"><span data-stu-id="05428-109">DESCRIPTION</span></span>
<span data-ttu-id="05428-110">**AzureStorageFileContent** cmdlet은 파일의 콘텐츠를 다운로드 한 다음 지정 된 대상에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="05428-111">이 cmdlet은 파일의 내용을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05428-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="05428-112">예제의</span><span class="sxs-lookup"><span data-stu-id="05428-112">EXAMPLES</span></span>

### <span data-ttu-id="05428-113">예제 1: 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="05428-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="05428-114">이 명령은 파일 공유 ContosoShare06에서 현재 폴더로 ContosoWorkingFolder 폴더의 CurrentDataFile 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

## <span data-ttu-id="05428-115">변수</span><span class="sxs-lookup"><span data-stu-id="05428-115">PARAMETERS</span></span>

### <span data-ttu-id="05428-116">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="05428-116">-CheckMd5</span></span>
<span data-ttu-id="05428-117">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-117">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-118">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-118">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-119">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-119">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-120">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-120">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="05428-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="05428-122">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-122">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-123">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-123">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-124">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-124">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-125">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-125">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="05428-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="05428-127">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-127">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-128">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-128">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-129">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-129">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-130">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-130">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-131">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="05428-131">-Context</span></span>
<span data-ttu-id="05428-132">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-132">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-133">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-133">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-134">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-134">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-135">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-135">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-136">-대상</span><span class="sxs-lookup"><span data-stu-id="05428-136">-Destination</span></span>
<span data-ttu-id="05428-137">대상 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-137">Specifies the destination path.</span></span>
<span data-ttu-id="05428-138">이 cmdlet은이 매개 변수에서 지정 하는 위치에 파일 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-138">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="05428-139">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-139">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-140">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-140">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-141">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-141">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-142">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-142">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-143">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="05428-143">-Directory</span></span>
<span data-ttu-id="05428-144">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-144">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="05428-145">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일에 대 한 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05428-145">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="05428-146">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-146">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="05428-147">또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05428-147">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="05428-148">-파일</span><span class="sxs-lookup"><span data-stu-id="05428-148">-File</span></span>
<span data-ttu-id="05428-149">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-149">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="05428-150">이 cmdlet은이 매개 변수에서 지정 하는 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05428-150">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="05428-151">**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-151">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="05428-152">-Force</span><span class="sxs-lookup"><span data-stu-id="05428-152">-Force</span></span>
<span data-ttu-id="05428-153">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-153">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-154">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-154">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-155">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-155">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-156">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-156">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-157">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05428-157">-PassThru</span></span>
<span data-ttu-id="05428-158">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-158">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-159">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-159">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-160">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-160">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-161">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-161">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-162">-Path</span><span class="sxs-lookup"><span data-stu-id="05428-162">-Path</span></span>
<span data-ttu-id="05428-163">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-163">Specifies the path of a file.</span></span>
<span data-ttu-id="05428-164">이 cmdlet은이 매개 변수에서 지정 하는 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05428-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="05428-165">파일이 없는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="05428-166">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="05428-166">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="05428-167">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-167">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="05428-168">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="05428-168">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="05428-169">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05428-169">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="05428-170">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-170">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="05428-171">-공유</span><span class="sxs-lookup"><span data-stu-id="05428-171">-Share</span></span>
<span data-ttu-id="05428-172">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-172">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="05428-173">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-173">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="05428-174">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-174">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="05428-175">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-175">This object contains the storage context.</span></span>
<span data-ttu-id="05428-176">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="05428-176">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="05428-177">-ShareName</span><span class="sxs-lookup"><span data-stu-id="05428-177">-ShareName</span></span>
<span data-ttu-id="05428-178">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-178">Specifies the name of the file share.</span></span>
<span data-ttu-id="05428-179">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-179">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="05428-180">-확인</span><span class="sxs-lookup"><span data-stu-id="05428-180">-Confirm</span></span>
<span data-ttu-id="05428-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05428-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05428-182">-WhatIf</span></span>
<span data-ttu-id="05428-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05428-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05428-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05428-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05428-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05428-185">CommonParameters</span></span>
<span data-ttu-id="05428-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05428-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05428-187">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05428-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05428-188">입력</span><span class="sxs-lookup"><span data-stu-id="05428-188">INPUTS</span></span>

## <span data-ttu-id="05428-189">출력</span><span class="sxs-lookup"><span data-stu-id="05428-189">OUTPUTS</span></span>

## <span data-ttu-id="05428-190">상속자</span><span class="sxs-lookup"><span data-stu-id="05428-190">NOTES</span></span>

## <span data-ttu-id="05428-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05428-191">RELATED LINKS</span></span>

[<span data-ttu-id="05428-192">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="05428-192">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="05428-193">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="05428-193">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


