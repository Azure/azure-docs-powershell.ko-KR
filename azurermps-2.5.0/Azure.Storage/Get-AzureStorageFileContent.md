---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
ms.openlocfilehash: c390a51997e175efb834366a65e10d671f384fa8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880810"
---
# <span data-ttu-id="bbd21-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bbd21-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="bbd21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd21-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd21-103">파일의 내용을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbd21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bbd21-104">SYNTAX</span></span>

### <span data-ttu-id="bbd21-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="bbd21-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbd21-106">공유</span><span class="sxs-lookup"><span data-stu-id="bbd21-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbd21-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="bbd21-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbd21-108">파일</span><span class="sxs-lookup"><span data-stu-id="bbd21-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbd21-109">설명은</span><span class="sxs-lookup"><span data-stu-id="bbd21-109">DESCRIPTION</span></span>
<span data-ttu-id="bbd21-110">**AzureStorageFileContent** cmdlet은 파일의 콘텐츠를 다운로드 한 다음 지정 된 대상에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="bbd21-111">이 cmdlet은 파일의 내용을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="bbd21-112">예제의</span><span class="sxs-lookup"><span data-stu-id="bbd21-112">EXAMPLES</span></span>

### <span data-ttu-id="bbd21-113">예제 1: 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="bbd21-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="bbd21-114">이 명령은 파일 공유 ContosoShare06에서 현재 폴더로 ContosoWorkingFolder 폴더의 CurrentDataFile 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="bbd21-115">예제 2: 샘플 파일 공유 아래에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="bbd21-116">이 예제에서는 예제 파일 공유 아래에 있는 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="bbd21-117">변수</span><span class="sxs-lookup"><span data-stu-id="bbd21-117">PARAMETERS</span></span>

### <span data-ttu-id="bbd21-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="bbd21-118">-CheckMd5</span></span>
<span data-ttu-id="bbd21-119">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-120">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-121">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-122">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbd21-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bbd21-124">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-125">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-126">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-127">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bbd21-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bbd21-129">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-130">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-131">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-132">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-133">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bbd21-133">-Context</span></span>
<span data-ttu-id="bbd21-134">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-135">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-136">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-137">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd21-138">-DefaultProfile</span></span>
<span data-ttu-id="bbd21-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd21-140">-대상</span><span class="sxs-lookup"><span data-stu-id="bbd21-140">-Destination</span></span>
<span data-ttu-id="bbd21-141">대상 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-141">Specifies the destination path.</span></span>
<span data-ttu-id="bbd21-142">이 cmdlet은이 매개 변수에서 지정 하는 위치에 파일 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="bbd21-143">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-144">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-145">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-146">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd21-147">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="bbd21-147">-Directory</span></span>
<span data-ttu-id="bbd21-148">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="bbd21-149">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일에 대 한 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="bbd21-150">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="bbd21-151">또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd21-152">-파일</span><span class="sxs-lookup"><span data-stu-id="bbd21-152">-File</span></span>
<span data-ttu-id="bbd21-153">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="bbd21-154">이 cmdlet은이 매개 변수에서 지정 하는 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="bbd21-155">**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd21-156">-Force</span><span class="sxs-lookup"><span data-stu-id="bbd21-156">-Force</span></span>
<span data-ttu-id="bbd21-157">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-158">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-159">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-160">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbd21-161">-PassThru</span></span>
<span data-ttu-id="bbd21-162">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-163">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-164">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-165">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-166">-Path</span><span class="sxs-lookup"><span data-stu-id="bbd21-166">-Path</span></span>
<span data-ttu-id="bbd21-167">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-167">Specifies the path of a file.</span></span>
<span data-ttu-id="bbd21-168">이 cmdlet은이 매개 변수에서 지정 하는 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="bbd21-169">파일이 없는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bbd21-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bbd21-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bbd21-171">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="bbd21-172">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="bbd21-173">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="bbd21-174">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="bbd21-175">-공유</span><span class="sxs-lookup"><span data-stu-id="bbd21-175">-Share</span></span>
<span data-ttu-id="bbd21-176">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bbd21-177">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="bbd21-178">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="bbd21-179">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-179">This object contains the storage context.</span></span>
<span data-ttu-id="bbd21-180">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="bbd21-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd21-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bbd21-181">-ShareName</span></span>
<span data-ttu-id="bbd21-182">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="bbd21-183">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="bbd21-184">-확인</span><span class="sxs-lookup"><span data-stu-id="bbd21-184">-Confirm</span></span>
<span data-ttu-id="bbd21-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd21-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd21-186">-WhatIf</span></span>
<span data-ttu-id="bbd21-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd21-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd21-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd21-189">CommonParameters</span></span>
<span data-ttu-id="bbd21-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd21-191">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd21-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd21-192">입력</span><span class="sxs-lookup"><span data-stu-id="bbd21-192">INPUTS</span></span>

### <span data-ttu-id="bbd21-193">WindowsAzure 파일. c a c 공유</span><span class="sxs-lookup"><span data-stu-id="bbd21-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="bbd21-194">매개 변수: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbd21-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="bbd21-195">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="bbd21-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="bbd21-196">매개 변수: Directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbd21-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="bbd21-197">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="bbd21-198">매개 변수: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bbd21-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="bbd21-199">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbd21-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bbd21-200">출력</span><span class="sxs-lookup"><span data-stu-id="bbd21-200">OUTPUTS</span></span>

### <span data-ttu-id="bbd21-201">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbd21-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="bbd21-202">상속자</span><span class="sxs-lookup"><span data-stu-id="bbd21-202">NOTES</span></span>

## <span data-ttu-id="bbd21-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbd21-203">RELATED LINKS</span></span>

[<span data-ttu-id="bbd21-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="bbd21-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="bbd21-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bbd21-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


