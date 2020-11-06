---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532176"
---
# <span data-ttu-id="e2077-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e2077-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2077-102">SYNOPSIS</span></span>
<span data-ttu-id="e2077-103">로컬 파일 또는 디렉터리를 Data Lake Store에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2077-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2077-104">SYNTAX</span></span>

### <span data-ttu-id="e2077-105">NoDiagnosticLogging (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2077-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2077-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="e2077-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2077-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2077-107">DESCRIPTION</span></span>
<span data-ttu-id="e2077-108">**AzureRmDataLakeStoreItem** cmdlet은 로컬 파일 또는 디렉터리를 Data Lake store에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="e2077-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e2077-109">EXAMPLES</span></span>

### <span data-ttu-id="e2077-110">예제 1: 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="e2077-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="e2077-111">이 명령은 SrcFile.csv 파일을 업로드 하 고 File.csv을 4의 concurrency와 함께 Data Lake Store의 MyFiles 폴더에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="e2077-112">변수</span><span class="sxs-lookup"><span data-stu-id="e2077-112">PARAMETERS</span></span>

### <span data-ttu-id="e2077-113">-계정</span><span class="sxs-lookup"><span data-stu-id="e2077-113">-Account</span></span>
<span data-ttu-id="e2077-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-115">-동시성</span><span class="sxs-lookup"><span data-stu-id="e2077-115">-Concurrency</span></span>
<span data-ttu-id="e2077-116">병렬로 업로드할 파일 또는 청크 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="e2077-117">기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="e2077-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="e2077-119">폴더 업로드에 대해 병렬로 업로드할 최대 파일 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="e2077-120">폴더 및 파일 크기에 기반 하 여 기본적으로 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2077-121">-DefaultProfile</span></span>
<span data-ttu-id="e2077-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-123">-대상</span><span class="sxs-lookup"><span data-stu-id="e2077-123">-Destination</span></span>
<span data-ttu-id="e2077-124">루트 디렉터리 (/)로 시작 하 여 파일이 나 폴더를 업로드할 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="e2077-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="e2077-126">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록 하는 데 사용할 진단 로그 수준을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="e2077-127">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="e2077-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="e2077-129">파일 또는 폴더 가져오기 중에 진단 로그에서 이벤트를 기록 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e2077-130">-Force</span></span>
<span data-ttu-id="e2077-131">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="e2077-132">-ForceBinary</span></span>
<span data-ttu-id="e2077-133">추가 된 새 줄 유지에 대 한 고려 없이 복사 되는 파일을 복사 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-134">-Path</span><span class="sxs-lookup"><span data-stu-id="e2077-134">-Path</span></span>
<span data-ttu-id="e2077-135">업로드할 파일 또는 폴더의 로컬 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="e2077-136">-PerFileThreadCount</span></span>
<span data-ttu-id="e2077-137">파일 당 사용할 최대 스레드 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="e2077-138">폴더 및 파일 크기에 기반 하 여 기본적으로 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-139">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="e2077-139">-Recurse</span></span>
<span data-ttu-id="e2077-140">이 작업이 모든 하위 폴더의 모든 항목을 업로드 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-141">-Resume</span><span class="sxs-lookup"><span data-stu-id="e2077-141">-Resume</span></span>
<span data-ttu-id="e2077-142">복사 되는 파일이 이전 업로드의 연속 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="e2077-143">이렇게 하면 시스템이 완전히 업로드 되지 않은 마지막 파일에서 다시 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2077-144">-확인</span><span class="sxs-lookup"><span data-stu-id="e2077-144">-Confirm</span></span>
<span data-ttu-id="e2077-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2077-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2077-146">-WhatIf</span></span>
<span data-ttu-id="e2077-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2077-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2077-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2077-149">CommonParameters</span></span>
<span data-ttu-id="e2077-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2077-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2077-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2077-152">입력</span><span class="sxs-lookup"><span data-stu-id="e2077-152">INPUTS</span></span>

### <span data-ttu-id="e2077-153">않아야</span><span class="sxs-lookup"><span data-stu-id="e2077-153">None</span></span>
<span data-ttu-id="e2077-154">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2077-155">출력</span><span class="sxs-lookup"><span data-stu-id="e2077-155">OUTPUTS</span></span>

### <span data-ttu-id="e2077-156">이름</span><span class="sxs-lookup"><span data-stu-id="e2077-156">string</span></span>
<span data-ttu-id="e2077-157">업로드 된 파일 또는 폴더에 대 한 Data Lake Store 계정의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e2077-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="e2077-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e2077-158">NOTES</span></span>

## <span data-ttu-id="e2077-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2077-159">RELATED LINKS</span></span>

[<span data-ttu-id="e2077-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2077-161">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2077-162">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2077-163">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2077-164">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2077-165">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e2077-166">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e2077-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)

