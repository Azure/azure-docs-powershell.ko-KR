---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: afe19fed7cd8de43cb28b7b3f73b01312cdd42fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995680"
---
# <span data-ttu-id="caa0d-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="caa0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caa0d-102">SYNOPSIS</span></span>
<span data-ttu-id="caa0d-103">Data Lake Store에 로컬 파일 또는 디렉터리를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="caa0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="caa0d-104">SYNTAX</span></span>

### <span data-ttu-id="caa0d-105">NoDiagnosticLogging(기본값)</span><span class="sxs-lookup"><span data-stu-id="caa0d-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caa0d-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="caa0d-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caa0d-107">설명</span><span class="sxs-lookup"><span data-stu-id="caa0d-107">DESCRIPTION</span></span>
<span data-ttu-id="caa0d-108">**Import-AzDataLakeStoreItem** cmdlet은 Data Lake Store에 로컬 파일 또는 디렉터리를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="caa0d-109">예제</span><span class="sxs-lookup"><span data-stu-id="caa0d-109">EXAMPLES</span></span>

### <span data-ttu-id="caa0d-110">예제 1: 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="caa0d-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="caa0d-111">이 명령은 파일을 SrcFile.csv 4의 동시성으로 데이터 레이크 저장소의 MyFiles 폴더에 File.csv 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="caa0d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="caa0d-112">PARAMETERS</span></span>

### <span data-ttu-id="caa0d-113">-Account</span><span class="sxs-lookup"><span data-stu-id="caa0d-113">-Account</span></span>
<span data-ttu-id="caa0d-114">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="caa0d-115">-동시성</span><span class="sxs-lookup"><span data-stu-id="caa0d-115">-Concurrency</span></span>
<span data-ttu-id="caa0d-116">병렬로 업로드할 파일 또는 청크 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="caa0d-117">기본값은 시스템 사양에 따라 최상의 노력으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="caa0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa0d-118">-DefaultProfile</span></span>
<span data-ttu-id="caa0d-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caa0d-120">-대상</span><span class="sxs-lookup"><span data-stu-id="caa0d-120">-Destination</span></span>
<span data-ttu-id="caa0d-121">루트 디렉터리(/)로 시작하여 파일 또는 폴더를 업로드할 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="caa0d-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="caa0d-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="caa0d-123">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록하는 데 사용할 진단 로그 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="caa0d-124">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-124">Default is Error.</span></span>

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

### <span data-ttu-id="caa0d-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="caa0d-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="caa0d-126">파일 또는 폴더 가져오기 중에 이벤트를 기록하는 진단 로그의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="caa0d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="caa0d-127">-Force</span></span>
<span data-ttu-id="caa0d-128">이 작업이 이미 있는 경우 대상 파일을 덮어써도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="caa0d-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="caa0d-129">-ForceBinary</span></span>
<span data-ttu-id="caa0d-130">복사되는 파일이 추가 전반에 걸쳐 새 줄 보존에 대한 염려가 없는 복사해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="caa0d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="caa0d-131">-Path</span></span>
<span data-ttu-id="caa0d-132">업로드할 파일 또는 폴더의 로컬 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="caa0d-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="caa0d-133">-Recurse</span></span>
<span data-ttu-id="caa0d-134">이 작업은 모든 하위폴더에 모든 항목을 업로드해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="caa0d-135">-다시 시작</span><span class="sxs-lookup"><span data-stu-id="caa0d-135">-Resume</span></span>
<span data-ttu-id="caa0d-136">복사되는 파일이 이전 업로드의 연속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="caa0d-137">이렇게 하면 시스템이 완전히 업로드되지 않은 마지막 파일에서 다시 시작하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="caa0d-138">-확인</span><span class="sxs-lookup"><span data-stu-id="caa0d-138">-Confirm</span></span>
<span data-ttu-id="caa0d-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa0d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa0d-140">-WhatIf</span></span>
<span data-ttu-id="caa0d-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa0d-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa0d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa0d-143">CommonParameters</span></span>
<span data-ttu-id="caa0d-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="caa0d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa0d-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="caa0d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa0d-146">입력</span><span class="sxs-lookup"><span data-stu-id="caa0d-146">INPUTS</span></span>

### <span data-ttu-id="caa0d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="caa0d-147">System.String</span></span>

### <span data-ttu-id="caa0d-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="caa0d-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="caa0d-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="caa0d-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="caa0d-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="caa0d-150">System.Int32</span></span>

### <span data-ttu-id="caa0d-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="caa0d-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="caa0d-152">출력</span><span class="sxs-lookup"><span data-stu-id="caa0d-152">OUTPUTS</span></span>

### <span data-ttu-id="caa0d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="caa0d-153">System.String</span></span>

## <span data-ttu-id="caa0d-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="caa0d-154">NOTES</span></span>

## <span data-ttu-id="caa0d-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="caa0d-155">RELATED LINKS</span></span>

[<span data-ttu-id="caa0d-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="caa0d-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="caa0d-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="caa0d-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="caa0d-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="caa0d-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="caa0d-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="caa0d-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


