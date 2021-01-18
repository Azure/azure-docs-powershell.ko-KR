---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492736"
---
# <span data-ttu-id="285c0-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="285c0-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="285c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285c0-102">SYNOPSIS</span></span>
<span data-ttu-id="285c0-103">Get-AzStorageBlobQueryResult에서 사용할 수 있는 Blob 쿼리 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="285c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="285c0-104">SYNTAX</span></span>

### <span data-ttu-id="285c0-105">Csv(기본값)</span><span class="sxs-lookup"><span data-stu-id="285c0-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="285c0-106">Json</span><span class="sxs-lookup"><span data-stu-id="285c0-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="285c0-107">설명</span><span class="sxs-lookup"><span data-stu-id="285c0-107">DESCRIPTION</span></span>
<span data-ttu-id="285c0-108">**New-AzStorageBlobQueryConfig** cmdlet은 Get-AzStorageBlobQueryResult에서 사용할 수 있는 Blob 쿼리 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="285c0-109">예제</span><span class="sxs-lookup"><span data-stu-id="285c0-109">EXAMPLES</span></span>

### <span data-ttu-id="285c0-110">예제 1: Blob 쿼리 구성 만들기 및 Blob 쿼리</span><span class="sxs-lookup"><span data-stu-id="285c0-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="285c0-111">이 명령은 먼저 csv로 입력 구성 개체를 만들고, 출력 구성 개체를 json으로 만든 다음, 2개 구성을 사용하여 Blob을 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="285c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="285c0-112">PARAMETERS</span></span>

### <span data-ttu-id="285c0-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="285c0-113">-AsCsv</span></span>
<span data-ttu-id="285c0-114">CSV에 대한 Blob 쿼리 구성을 만들 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="285c0-115">-AsJob</span></span>
<span data-ttu-id="285c0-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="285c0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="285c0-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="285c0-117">-AsJson</span></span>
<span data-ttu-id="285c0-118">Json에 대한 Blob 쿼리 구성을 만들 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="285c0-119">-ColumnSeparator</span></span>
<span data-ttu-id="285c0-120">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-120">Optional.</span></span>
<span data-ttu-id="285c0-121">열을 구분하는 데 사용되는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="285c0-122">-EscapeCharacter</span></span>
<span data-ttu-id="285c0-123">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-123">Optional.</span></span>
<span data-ttu-id="285c0-124">이스케이프 문자로 사용되는 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="285c0-125">-HasHeader</span></span>
<span data-ttu-id="285c0-126">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-126">Optional.</span></span>
<span data-ttu-id="285c0-127">데이터에 헤더가 있는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="285c0-128">-QuotationCharacter</span></span>
<span data-ttu-id="285c0-129">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-129">Optional.</span></span>
<span data-ttu-id="285c0-130">특정 필드를 인용하는 데 사용되는 char입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="285c0-131">-RecordSeparator</span></span>
<span data-ttu-id="285c0-132">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-132">Optional.</span></span>
<span data-ttu-id="285c0-133">레코드를 구분하는 데 사용되는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-133">The string used to separate records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="285c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285c0-134">CommonParameters</span></span>
<span data-ttu-id="285c0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="285c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285c0-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="285c0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285c0-137">입력</span><span class="sxs-lookup"><span data-stu-id="285c0-137">INPUTS</span></span>

### <span data-ttu-id="285c0-138">없음</span><span class="sxs-lookup"><span data-stu-id="285c0-138">None</span></span>

## <span data-ttu-id="285c0-139">출력</span><span class="sxs-lookup"><span data-stu-id="285c0-139">OUTPUTS</span></span>

### <span data-ttu-id="285c0-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="285c0-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="285c0-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="285c0-141">NOTES</span></span>

## <span data-ttu-id="285c0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="285c0-142">RELATED LINKS</span></span>
