---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217178"
---
# <span data-ttu-id="56e01-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="56e01-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="56e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e01-102">SYNOPSIS</span></span>
<span data-ttu-id="56e01-103">AzStorageBlobQueryResult에서 사용할 수 있는 blob 쿼리 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="56e01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56e01-104">SYNTAX</span></span>

### <span data-ttu-id="56e01-105">Csv (기본값)</span><span class="sxs-lookup"><span data-stu-id="56e01-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="56e01-106">Json</span><span class="sxs-lookup"><span data-stu-id="56e01-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="56e01-107">설명은</span><span class="sxs-lookup"><span data-stu-id="56e01-107">DESCRIPTION</span></span>
<span data-ttu-id="56e01-108">**AzStorageBlobQueryConfig** Cmdlet은 Get-AzStorageBlobQueryResult에서 사용할 수 있는 blob 쿼리 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="56e01-109">예제의</span><span class="sxs-lookup"><span data-stu-id="56e01-109">EXAMPLES</span></span>

### <span data-ttu-id="56e01-110">예제 1: blob 쿼리 만들기 구성 및 blob 쿼리</span><span class="sxs-lookup"><span data-stu-id="56e01-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="56e01-111">이 명령은 먼저 입력 구성 개체를 csv로 만들고 구성 개체를 json으로 출력 한 다음 2 개의 구성을 사용 하 여 blob을 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="56e01-112">변수</span><span class="sxs-lookup"><span data-stu-id="56e01-112">PARAMETERS</span></span>

### <span data-ttu-id="56e01-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="56e01-113">-AsCsv</span></span>
<span data-ttu-id="56e01-114">CSV에 대 한 Blob 쿼리 구성을 만들도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="56e01-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56e01-115">-AsJob</span></span>
<span data-ttu-id="56e01-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="56e01-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56e01-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="56e01-117">-AsJson</span></span>
<span data-ttu-id="56e01-118">Json에 대 한 Blob 쿼리 구성을 만들도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="56e01-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="56e01-119">-ColumnSeparator</span></span>
<span data-ttu-id="56e01-120">).</span><span class="sxs-lookup"><span data-stu-id="56e01-120">Optional.</span></span>
<span data-ttu-id="56e01-121">열을 구분 하는 데 사용 되는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="56e01-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="56e01-122">-EscapeCharacter</span></span>
<span data-ttu-id="56e01-123">).</span><span class="sxs-lookup"><span data-stu-id="56e01-123">Optional.</span></span>
<span data-ttu-id="56e01-124">이스케이프 문자로 사용 되는 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="56e01-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="56e01-125">-HasHeader</span></span>
<span data-ttu-id="56e01-126">).</span><span class="sxs-lookup"><span data-stu-id="56e01-126">Optional.</span></span>
<span data-ttu-id="56e01-127">데이터에 머리글이 있음을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="56e01-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="56e01-128">-QuotationCharacter</span></span>
<span data-ttu-id="56e01-129">).</span><span class="sxs-lookup"><span data-stu-id="56e01-129">Optional.</span></span>
<span data-ttu-id="56e01-130">특정 필드를 인용 하는 데 사용 되는 문자입니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="56e01-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="56e01-131">-RecordSeparator</span></span>
<span data-ttu-id="56e01-132">).</span><span class="sxs-lookup"><span data-stu-id="56e01-132">Optional.</span></span>
<span data-ttu-id="56e01-133">레코드를 구분 하는 데 사용 되는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="56e01-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e01-134">CommonParameters</span></span>
<span data-ttu-id="56e01-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e01-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e01-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e01-137">입력</span><span class="sxs-lookup"><span data-stu-id="56e01-137">INPUTS</span></span>

### <span data-ttu-id="56e01-138">않아야</span><span class="sxs-lookup"><span data-stu-id="56e01-138">None</span></span>

## <span data-ttu-id="56e01-139">출력</span><span class="sxs-lookup"><span data-stu-id="56e01-139">OUTPUTS</span></span>

### <span data-ttu-id="56e01-140">WindowsAzure. ResourceModel Blobquerytextconfiguration을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e01-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="56e01-141">상속자</span><span class="sxs-lookup"><span data-stu-id="56e01-141">NOTES</span></span>

## <span data-ttu-id="56e01-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56e01-142">RELATED LINKS</span></span>
