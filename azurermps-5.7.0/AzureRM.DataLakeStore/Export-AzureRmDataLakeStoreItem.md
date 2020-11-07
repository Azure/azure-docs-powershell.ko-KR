---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702374"
---
# <span data-ttu-id="ba70e-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ba70e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba70e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba70e-103">Data Lake Store에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba70e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba70e-104">SYNTAX</span></span>

### <span data-ttu-id="ba70e-105">NoDiagnosticLogging (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba70e-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba70e-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="ba70e-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba70e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ba70e-107">DESCRIPTION</span></span>
<span data-ttu-id="ba70e-108">**Export-AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="ba70e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ba70e-109">EXAMPLES</span></span>

### <span data-ttu-id="ba70e-110">예제 1: Data Lake Store에서 항목 다운로드</span><span class="sxs-lookup"><span data-stu-id="ba70e-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="ba70e-111">이 명령은 데이터 호수 저장소에서 파일 TestSource.csv를 동시성이 4 인 C:\Test.csv으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="ba70e-112">변수</span><span class="sxs-lookup"><span data-stu-id="ba70e-112">PARAMETERS</span></span>

### <span data-ttu-id="ba70e-113">-계정</span><span class="sxs-lookup"><span data-stu-id="ba70e-113">-Account</span></span>
<span data-ttu-id="ba70e-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ba70e-115">-동시성</span><span class="sxs-lookup"><span data-stu-id="ba70e-115">-Concurrency</span></span>
<span data-ttu-id="ba70e-116">병렬로 다운로드할 파일 또는 청크 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="ba70e-117">기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba70e-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="ba70e-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="ba70e-119">폴더 다운로드에 대해 병렬로 다운로드할 최대 파일 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="ba70e-120">폴더 및 파일 크기에 기반 하 여 기본적으로 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="ba70e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba70e-121">-DefaultProfile</span></span>
<span data-ttu-id="ba70e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba70e-123">-대상</span><span class="sxs-lookup"><span data-stu-id="ba70e-123">-Destination</span></span>
<span data-ttu-id="ba70e-124">파일을 다운로드할 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba70e-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="ba70e-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="ba70e-126">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록 하는 데 사용할 진단 로그 수준을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="ba70e-127">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-127">Default is Error.</span></span>

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

### <span data-ttu-id="ba70e-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="ba70e-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="ba70e-129">파일 또는 폴더 가져오기 중에 진단 로그에서 이벤트를 기록 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="ba70e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ba70e-130">-Force</span></span>
<span data-ttu-id="ba70e-131">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba70e-132">-Path</span><span class="sxs-lookup"><span data-stu-id="ba70e-132">-Path</span></span>
<span data-ttu-id="ba70e-133">루트 디렉터리 (/)에서 시작 하 여 Data Lake Store에서 다운로드할 항목의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba70e-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="ba70e-134">-PerFileThreadCount</span></span>
<span data-ttu-id="ba70e-135">파일 당 사용할 최대 스레드 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="ba70e-136">폴더 및 파일 크기에 기반 하 여 기본적으로 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba70e-137">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="ba70e-137">-Recurse</span></span>
<span data-ttu-id="ba70e-138">폴더 다운로드가 재귀적 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="ba70e-139">-Resume</span><span class="sxs-lookup"><span data-stu-id="ba70e-139">-Resume</span></span>
<span data-ttu-id="ba70e-140">복사 중인 파일이 이전 다운로드의 연속 작업 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="ba70e-141">이렇게 하면 시스템이 완전히 다운로드 되지 않은 마지막 파일에서 다시 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="ba70e-142">-확인</span><span class="sxs-lookup"><span data-stu-id="ba70e-142">-Confirm</span></span>
<span data-ttu-id="ba70e-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba70e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba70e-144">-WhatIf</span></span>
<span data-ttu-id="ba70e-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba70e-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba70e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba70e-147">CommonParameters</span></span>
<span data-ttu-id="ba70e-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba70e-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba70e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba70e-150">입력</span><span class="sxs-lookup"><span data-stu-id="ba70e-150">INPUTS</span></span>

### <span data-ttu-id="ba70e-151">않아야</span><span class="sxs-lookup"><span data-stu-id="ba70e-151">None</span></span>
<span data-ttu-id="ba70e-152">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba70e-153">출력</span><span class="sxs-lookup"><span data-stu-id="ba70e-153">OUTPUTS</span></span>

### <span data-ttu-id="ba70e-154">이름</span><span class="sxs-lookup"><span data-stu-id="ba70e-154">string</span></span>
<span data-ttu-id="ba70e-155">파일 또는 폴더가 다운로드 된 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ba70e-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="ba70e-156">상속자</span><span class="sxs-lookup"><span data-stu-id="ba70e-156">NOTES</span></span>

## <span data-ttu-id="ba70e-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba70e-157">RELATED LINKS</span></span>

[<span data-ttu-id="ba70e-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba70e-159">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba70e-160">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba70e-161">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba70e-162">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba70e-163">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba70e-164">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba70e-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


