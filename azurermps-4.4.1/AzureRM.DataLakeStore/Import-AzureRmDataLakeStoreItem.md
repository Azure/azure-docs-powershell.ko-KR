---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703745"
---
# <span data-ttu-id="cec50-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="cec50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cec50-102">SYNOPSIS</span></span>
<span data-ttu-id="cec50-103">로컬 파일 또는 디렉터리를 Data Lake Store에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cec50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cec50-104">SYNTAX</span></span>

### <span data-ttu-id="cec50-105">진단 로깅 없음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cec50-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cec50-106">진단 로깅 포함</span><span class="sxs-lookup"><span data-stu-id="cec50-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cec50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cec50-107">DESCRIPTION</span></span>
<span data-ttu-id="cec50-108">**AzureRmDataLakeStoreItem** cmdlet은 로컬 파일 또는 디렉터리를 Data Lake store에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="cec50-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cec50-109">EXAMPLES</span></span>

### <span data-ttu-id="cec50-110">예제 1: 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="cec50-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="cec50-111">이 명령은 SrcFile.csv 파일을 업로드 하 고 File.csv을 Data Lake Store의 MyFiles 폴더에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="cec50-112">변수</span><span class="sxs-lookup"><span data-stu-id="cec50-112">PARAMETERS</span></span>

### <span data-ttu-id="cec50-113">-계정</span><span class="sxs-lookup"><span data-stu-id="cec50-113">-Account</span></span>
<span data-ttu-id="cec50-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="cec50-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="cec50-116">폴더 업로드에 대해 병렬로 업로드할 최대 파일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="cec50-117">기본 값은 5입니다 (5).</span><span class="sxs-lookup"><span data-stu-id="cec50-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-118">-대상</span><span class="sxs-lookup"><span data-stu-id="cec50-118">-Destination</span></span>
<span data-ttu-id="cec50-119">루트 디렉터리 (/)로 시작 하 여 파일이 나 폴더를 업로드할 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="cec50-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="cec50-121">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록 하는 데 사용할 진단 로그 수준을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="cec50-122">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="cec50-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="cec50-124">파일 또는 폴더 가져오기 중에 진단 로그에서 이벤트를 기록 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cec50-125">-Force</span></span>
<span data-ttu-id="cec50-126">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="cec50-127">-ForceBinary</span></span>
<span data-ttu-id="cec50-128">이 작업이 파일을 이진 파일로 업로드 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-128">Indicates that this operation uploads the file as a binary file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-129">-Path</span><span class="sxs-lookup"><span data-stu-id="cec50-129">-Path</span></span>
<span data-ttu-id="cec50-130">업로드할 파일 또는 폴더의 로컬 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-130">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="cec50-131">-PerFileThreadCount</span></span>
<span data-ttu-id="cec50-132">파일 당 사용할 최대 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="cec50-133">기본값은 10 (10)입니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-134">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="cec50-134">-Recurse</span></span>
<span data-ttu-id="cec50-135">이 작업이 모든 하위 폴더의 모든 항목을 업로드 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-135">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-136">-Resume</span><span class="sxs-lookup"><span data-stu-id="cec50-136">-Resume</span></span>
<span data-ttu-id="cec50-137">이 작업이 이전에 취소 또는 실패 한 업로드를 다시 시작 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cec50-138">-확인</span><span class="sxs-lookup"><span data-stu-id="cec50-138">-Confirm</span></span>
<span data-ttu-id="cec50-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cec50-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cec50-140">-WhatIf</span></span>
<span data-ttu-id="cec50-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cec50-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cec50-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec50-143">-DefaultProfile</span></span>
<span data-ttu-id="cec50-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cec50-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec50-145">CommonParameters</span></span>
<span data-ttu-id="cec50-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec50-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec50-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec50-148">입력</span><span class="sxs-lookup"><span data-stu-id="cec50-148">INPUTS</span></span>

## <span data-ttu-id="cec50-149">출력</span><span class="sxs-lookup"><span data-stu-id="cec50-149">OUTPUTS</span></span>

### <span data-ttu-id="cec50-150">이름</span><span class="sxs-lookup"><span data-stu-id="cec50-150">string</span></span>
<span data-ttu-id="cec50-151">업로드 된 파일 또는 폴더에 대 한 Data Lake Store 계정의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cec50-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="cec50-152">상속자</span><span class="sxs-lookup"><span data-stu-id="cec50-152">NOTES</span></span>

## <span data-ttu-id="cec50-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cec50-153">RELATED LINKS</span></span>

[<span data-ttu-id="cec50-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cec50-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cec50-156">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cec50-157">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cec50-158">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cec50-159">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cec50-160">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cec50-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


