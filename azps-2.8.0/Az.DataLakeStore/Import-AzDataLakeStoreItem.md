---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ccb538446e7cb179e15f3af17d0cde03c4ab44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696839"
---
# <span data-ttu-id="2ee2c-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="2ee2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee2c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee2c-103">로컬 파일 또는 디렉터리를 Data Lake Store에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="2ee2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ee2c-104">SYNTAX</span></span>

### <span data-ttu-id="2ee2c-105">NoDiagnosticLogging (기본값)</span><span class="sxs-lookup"><span data-stu-id="2ee2c-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee2c-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="2ee2c-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ee2c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2ee2c-107">DESCRIPTION</span></span>
<span data-ttu-id="2ee2c-108">**AzDataLakeStoreItem** cmdlet은 로컬 파일 또는 디렉터리를 Data Lake store에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="2ee2c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2ee2c-109">EXAMPLES</span></span>

### <span data-ttu-id="2ee2c-110">예제 1: 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="2ee2c-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="2ee2c-111">이 명령은 SrcFile.csv 파일을 업로드 하 고 File.csv을 4의 concurrency와 함께 Data Lake Store의 MyFiles 폴더에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="2ee2c-112">변수</span><span class="sxs-lookup"><span data-stu-id="2ee2c-112">PARAMETERS</span></span>

### <span data-ttu-id="2ee2c-113">-계정</span><span class="sxs-lookup"><span data-stu-id="2ee2c-113">-Account</span></span>
<span data-ttu-id="2ee2c-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2ee2c-115">-동시성</span><span class="sxs-lookup"><span data-stu-id="2ee2c-115">-Concurrency</span></span>
<span data-ttu-id="2ee2c-116">병렬로 업로드할 파일 또는 청크 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="2ee2c-117">기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee2c-118">-DefaultProfile</span></span>
<span data-ttu-id="2ee2c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee2c-120">-대상</span><span class="sxs-lookup"><span data-stu-id="2ee2c-120">-Destination</span></span>
<span data-ttu-id="2ee2c-121">루트 디렉터리 (/)로 시작 하 여 파일이 나 폴더를 업로드할 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2ee2c-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="2ee2c-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="2ee2c-123">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록 하는 데 사용할 진단 로그 수준을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="2ee2c-124">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee2c-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="2ee2c-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="2ee2c-126">파일 또는 폴더 가져오기 중에 진단 로그에서 이벤트를 기록 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee2c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2ee2c-127">-Force</span></span>
<span data-ttu-id="2ee2c-128">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="2ee2c-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="2ee2c-129">-ForceBinary</span></span>
<span data-ttu-id="2ee2c-130">추가 된 새 줄 유지에 대 한 고려 없이 복사 되는 파일을 복사 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="2ee2c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="2ee2c-131">-Path</span></span>
<span data-ttu-id="2ee2c-132">업로드할 파일 또는 폴더의 로컬 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="2ee2c-133">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="2ee2c-133">-Recurse</span></span>
<span data-ttu-id="2ee2c-134">이 작업이 모든 하위 폴더의 모든 항목을 업로드 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="2ee2c-135">-Resume</span><span class="sxs-lookup"><span data-stu-id="2ee2c-135">-Resume</span></span>
<span data-ttu-id="2ee2c-136">복사 되는 파일이 이전 업로드의 연속 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="2ee2c-137">이렇게 하면 시스템이 완전히 업로드 되지 않은 마지막 파일에서 다시 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="2ee2c-138">-확인</span><span class="sxs-lookup"><span data-stu-id="2ee2c-138">-Confirm</span></span>
<span data-ttu-id="2ee2c-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee2c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee2c-140">-WhatIf</span></span>
<span data-ttu-id="2ee2c-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee2c-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee2c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee2c-143">CommonParameters</span></span>
<span data-ttu-id="2ee2c-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee2c-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee2c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee2c-146">입력</span><span class="sxs-lookup"><span data-stu-id="2ee2c-146">INPUTS</span></span>

### <span data-ttu-id="2ee2c-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ee2c-147">System.String</span></span>

### <span data-ttu-id="2ee2c-148">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2ee2c-149">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ee2c-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2ee2c-150">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="2ee2c-150">System.Int32</span></span>

### <span data-ttu-id="2ee2c-151">DataLakeStore. m a m</span><span class="sxs-lookup"><span data-stu-id="2ee2c-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="2ee2c-152">출력</span><span class="sxs-lookup"><span data-stu-id="2ee2c-152">OUTPUTS</span></span>

### <span data-ttu-id="2ee2c-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ee2c-153">System.String</span></span>

## <span data-ttu-id="2ee2c-154">상속자</span><span class="sxs-lookup"><span data-stu-id="2ee2c-154">NOTES</span></span>

## <span data-ttu-id="2ee2c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ee2c-155">RELATED LINKS</span></span>

[<span data-ttu-id="2ee2c-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="2ee2c-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="2ee2c-158">참가-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="2ee2c-159">이동-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="2ee2c-160">새로운 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="2ee2c-161">제거-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="2ee2c-162">테스트-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2ee2c-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


