---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532023"
---
# <span data-ttu-id="298cb-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="298cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="298cb-102">SYNOPSIS</span></span>
<span data-ttu-id="298cb-103">Data Lake Store에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="298cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="298cb-104">SYNTAX</span></span>

### <span data-ttu-id="298cb-105">NoDiagnosticLogging (기본값)</span><span class="sxs-lookup"><span data-stu-id="298cb-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="298cb-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="298cb-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="298cb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="298cb-107">DESCRIPTION</span></span>
<span data-ttu-id="298cb-108">**Export-AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="298cb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="298cb-109">EXAMPLES</span></span>

### <span data-ttu-id="298cb-110">예제 1: Data Lake Store에서 항목 다운로드</span><span class="sxs-lookup"><span data-stu-id="298cb-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="298cb-111">이 명령은 데이터 호수 저장소에서 파일 TestSource.csv를 동시성이 4 인 C:\Test.csv으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="298cb-112">변수</span><span class="sxs-lookup"><span data-stu-id="298cb-112">PARAMETERS</span></span>

### <span data-ttu-id="298cb-113">-계정</span><span class="sxs-lookup"><span data-stu-id="298cb-113">-Account</span></span>
<span data-ttu-id="298cb-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="298cb-115">-동시성</span><span class="sxs-lookup"><span data-stu-id="298cb-115">-Concurrency</span></span>
<span data-ttu-id="298cb-116">병렬로 다운로드할 파일 또는 청크 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="298cb-117">기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="298cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298cb-118">-DefaultProfile</span></span>
<span data-ttu-id="298cb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="298cb-120">-대상</span><span class="sxs-lookup"><span data-stu-id="298cb-120">-Destination</span></span>
<span data-ttu-id="298cb-121">파일을 다운로드할 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="298cb-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="298cb-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="298cb-123">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록 하는 데 사용할 진단 로그 수준을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="298cb-124">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-124">Default is Error.</span></span>

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

### <span data-ttu-id="298cb-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="298cb-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="298cb-126">파일 또는 폴더 가져오기 중에 진단 로그에서 이벤트를 기록 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="298cb-127">-Force</span><span class="sxs-lookup"><span data-stu-id="298cb-127">-Force</span></span>
<span data-ttu-id="298cb-128">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="298cb-129">-Path</span><span class="sxs-lookup"><span data-stu-id="298cb-129">-Path</span></span>
<span data-ttu-id="298cb-130">루트 디렉터리 (/)에서 시작 하 여 Data Lake Store에서 다운로드할 항목의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="298cb-131">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="298cb-131">-Recurse</span></span>
<span data-ttu-id="298cb-132">폴더 다운로드가 재귀적 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="298cb-133">-Resume</span><span class="sxs-lookup"><span data-stu-id="298cb-133">-Resume</span></span>
<span data-ttu-id="298cb-134">복사 중인 파일이 이전 다운로드의 연속 작업 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="298cb-135">이렇게 하면 시스템이 완전히 다운로드 되지 않은 마지막 파일에서 다시 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="298cb-136">-확인</span><span class="sxs-lookup"><span data-stu-id="298cb-136">-Confirm</span></span>
<span data-ttu-id="298cb-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="298cb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="298cb-138">-WhatIf</span></span>
<span data-ttu-id="298cb-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="298cb-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="298cb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298cb-141">CommonParameters</span></span>
<span data-ttu-id="298cb-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298cb-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="298cb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298cb-144">입력</span><span class="sxs-lookup"><span data-stu-id="298cb-144">INPUTS</span></span>

### <span data-ttu-id="298cb-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="298cb-145">System.String</span></span>

### <span data-ttu-id="298cb-146">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="298cb-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="298cb-147">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="298cb-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="298cb-148">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="298cb-148">System.Int32</span></span>

### <span data-ttu-id="298cb-149">DataLakeStore. m a m</span><span class="sxs-lookup"><span data-stu-id="298cb-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="298cb-150">출력</span><span class="sxs-lookup"><span data-stu-id="298cb-150">OUTPUTS</span></span>

### <span data-ttu-id="298cb-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="298cb-151">System.String</span></span>
<span data-ttu-id="298cb-152">파일 또는 폴더가 다운로드 된 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="298cb-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="298cb-153">상속자</span><span class="sxs-lookup"><span data-stu-id="298cb-153">NOTES</span></span>

## <span data-ttu-id="298cb-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="298cb-154">RELATED LINKS</span></span>

[<span data-ttu-id="298cb-155">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="298cb-156">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="298cb-157">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="298cb-158">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="298cb-159">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="298cb-160">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="298cb-161">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="298cb-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


