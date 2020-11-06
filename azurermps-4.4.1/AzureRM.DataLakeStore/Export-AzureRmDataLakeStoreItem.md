---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534139"
---
# <span data-ttu-id="6143a-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6143a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6143a-102">SYNOPSIS</span></span>
<span data-ttu-id="6143a-103">Data Lake Store에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6143a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6143a-104">SYNTAX</span></span>

### <span data-ttu-id="6143a-105">진단 로깅 없음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6143a-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6143a-106">진단 로깅 포함</span><span class="sxs-lookup"><span data-stu-id="6143a-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6143a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6143a-107">DESCRIPTION</span></span>
<span data-ttu-id="6143a-108">**Export-AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="6143a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6143a-109">EXAMPLES</span></span>

### <span data-ttu-id="6143a-110">예제 1: Data Lake Store에서 항목 다운로드</span><span class="sxs-lookup"><span data-stu-id="6143a-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="6143a-111">이 명령은 Data Lake Store에서 TestSource.csv 파일을 C:\Test.csv으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="6143a-112">변수</span><span class="sxs-lookup"><span data-stu-id="6143a-112">PARAMETERS</span></span>

### <span data-ttu-id="6143a-113">-계정</span><span class="sxs-lookup"><span data-stu-id="6143a-113">-Account</span></span>
<span data-ttu-id="6143a-114">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6143a-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="6143a-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="6143a-116">폴더 다운로드에 대해 병렬로 다운로드할 최대 파일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="6143a-117">기본 값은 5입니다 (5).</span><span class="sxs-lookup"><span data-stu-id="6143a-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="6143a-118">-대상</span><span class="sxs-lookup"><span data-stu-id="6143a-118">-Destination</span></span>
<span data-ttu-id="6143a-119">파일을 다운로드할 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="6143a-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="6143a-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="6143a-121">선택적으로 파일 또는 폴더 가져오기 중에 이벤트를 기록 하는 데 사용할 진단 로그 수준을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="6143a-122">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-122">Default is Error.</span></span>

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

### <span data-ttu-id="6143a-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="6143a-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="6143a-124">파일 또는 폴더 가져오기 중에 진단 로그에서 이벤트를 기록 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="6143a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6143a-125">-Force</span></span>
<span data-ttu-id="6143a-126">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6143a-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6143a-127">-Path</span></span>
<span data-ttu-id="6143a-128">루트 디렉터리 (/)에서 시작 하 여 Data Lake Store에서 다운로드할 항목의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="6143a-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="6143a-129">-PerFileThreadCount</span></span>
<span data-ttu-id="6143a-130">파일 당 사용할 최대 스레드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="6143a-131">기본값은 10 (10)입니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6143a-132">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="6143a-132">-Recurse</span></span>
<span data-ttu-id="6143a-133">폴더 다운로드가 재귀적 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="6143a-134">-Resume</span><span class="sxs-lookup"><span data-stu-id="6143a-134">-Resume</span></span>
<span data-ttu-id="6143a-135">복사 중인 파일이 이전 다운로드를 계속 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="6143a-136">다운로드는 완전히 다운로드 되지 않은 마지막 파일에서 다시 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="6143a-137">-확인</span><span class="sxs-lookup"><span data-stu-id="6143a-137">-Confirm</span></span>
<span data-ttu-id="6143a-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6143a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6143a-139">-WhatIf</span></span>
<span data-ttu-id="6143a-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6143a-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6143a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6143a-142">-DefaultProfile</span></span>
<span data-ttu-id="6143a-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6143a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6143a-144">CommonParameters</span></span>
<span data-ttu-id="6143a-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6143a-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6143a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6143a-147">입력</span><span class="sxs-lookup"><span data-stu-id="6143a-147">INPUTS</span></span>

## <span data-ttu-id="6143a-148">출력</span><span class="sxs-lookup"><span data-stu-id="6143a-148">OUTPUTS</span></span>

### <span data-ttu-id="6143a-149">이름</span><span class="sxs-lookup"><span data-stu-id="6143a-149">string</span></span>
<span data-ttu-id="6143a-150">파일 또는 폴더가 다운로드 된 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6143a-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="6143a-151">상속자</span><span class="sxs-lookup"><span data-stu-id="6143a-151">NOTES</span></span>

## <span data-ttu-id="6143a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6143a-152">RELATED LINKS</span></span>

[<span data-ttu-id="6143a-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6143a-154">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6143a-155">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6143a-156">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6143a-157">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6143a-158">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6143a-159">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6143a-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


