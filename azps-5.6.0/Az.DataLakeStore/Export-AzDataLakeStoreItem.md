---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 72fcb1ecd78b2682fe678af8b75b36032ff58b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957307"
---
# <span data-ttu-id="55388-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="55388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55388-102">SYNOPSIS</span></span>
<span data-ttu-id="55388-103">Data Lake Store에서 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="55388-104">구문</span><span class="sxs-lookup"><span data-stu-id="55388-104">SYNTAX</span></span>

### <span data-ttu-id="55388-105">NoDiagnosticLogging(기본값)</span><span class="sxs-lookup"><span data-stu-id="55388-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55388-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="55388-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55388-107">설명</span><span class="sxs-lookup"><span data-stu-id="55388-107">DESCRIPTION</span></span>
<span data-ttu-id="55388-108">**Export-AzDataLakeStoreItem** cmdlet은 Data Lake Store에서 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="55388-109">예제</span><span class="sxs-lookup"><span data-stu-id="55388-109">EXAMPLES</span></span>

### <span data-ttu-id="55388-110">예제 1: Data Lake Store에서 항목 다운로드</span><span class="sxs-lookup"><span data-stu-id="55388-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="55388-111">이 명령은 data Lake Store에서 TestSource.csv 파일을 다운로드하여 C:\Test.csv 4의 동시성으로 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="55388-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="55388-112">PARAMETERS</span></span>

### <span data-ttu-id="55388-113">-Account</span><span class="sxs-lookup"><span data-stu-id="55388-113">-Account</span></span>
<span data-ttu-id="55388-114">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="55388-115">-동시성</span><span class="sxs-lookup"><span data-stu-id="55388-115">-Concurrency</span></span>
<span data-ttu-id="55388-116">병렬로 다운로드할 파일 또는 청크 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55388-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="55388-117">기본값은 시스템 사양에 따라 최상의 노력으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="55388-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="55388-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55388-118">-DefaultProfile</span></span>
<span data-ttu-id="55388-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55388-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55388-120">-대상</span><span class="sxs-lookup"><span data-stu-id="55388-120">-Destination</span></span>
<span data-ttu-id="55388-121">파일을 다운로드할 로컬 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55388-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="55388-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="55388-123">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록하는 데 사용할 진단 로그 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55388-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="55388-124">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="55388-124">Default is Error.</span></span>

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

### <span data-ttu-id="55388-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="55388-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="55388-126">파일 또는 폴더 가져오기 중에 이벤트를 기록하는 진단 로그의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="55388-127">-Force</span><span class="sxs-lookup"><span data-stu-id="55388-127">-Force</span></span>
<span data-ttu-id="55388-128">이 작업이 이미 있는 경우 대상 파일을 덮어써도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="55388-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55388-129">-Path</span><span class="sxs-lookup"><span data-stu-id="55388-129">-Path</span></span>
<span data-ttu-id="55388-130">루트 디렉터리(/)에서 시작하여 Data Lake Store에서 다운로드할 항목의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55388-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="55388-131">-Recurse</span></span>
<span data-ttu-id="55388-132">폴더 다운로드가 재발하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55388-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="55388-133">-다시 시작</span><span class="sxs-lookup"><span data-stu-id="55388-133">-Resume</span></span>
<span data-ttu-id="55388-134">복사되는 파일이 이전 다운로드의 연속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="55388-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="55388-135">이렇게 하면 시스템이 완전히 다운로드되지 않은 마지막 파일에서 다시 시작하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="55388-136">-확인</span><span class="sxs-lookup"><span data-stu-id="55388-136">-Confirm</span></span>
<span data-ttu-id="55388-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55388-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55388-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55388-138">-WhatIf</span></span>
<span data-ttu-id="55388-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="55388-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55388-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55388-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55388-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55388-141">CommonParameters</span></span>
<span data-ttu-id="55388-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55388-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55388-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="55388-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55388-144">입력</span><span class="sxs-lookup"><span data-stu-id="55388-144">INPUTS</span></span>

### <span data-ttu-id="55388-145">System.String</span><span class="sxs-lookup"><span data-stu-id="55388-145">System.String</span></span>

### <span data-ttu-id="55388-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="55388-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="55388-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55388-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="55388-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="55388-148">System.Int32</span></span>

### <span data-ttu-id="55388-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="55388-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="55388-150">출력</span><span class="sxs-lookup"><span data-stu-id="55388-150">OUTPUTS</span></span>

### <span data-ttu-id="55388-151">System.String</span><span class="sxs-lookup"><span data-stu-id="55388-151">System.String</span></span>

## <span data-ttu-id="55388-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55388-152">NOTES</span></span>

## <span data-ttu-id="55388-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55388-153">RELATED LINKS</span></span>

[<span data-ttu-id="55388-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="55388-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="55388-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="55388-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="55388-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="55388-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="55388-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="55388-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


