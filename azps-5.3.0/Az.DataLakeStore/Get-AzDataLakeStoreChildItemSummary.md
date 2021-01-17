---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: b86b3f070a28de45039ebeb5ed0090f69756639f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489172"
---
# <span data-ttu-id="9ee2f-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="9ee2f-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="9ee2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee2f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee2f-103">지정된 경로에 포함된 총 크기, 파일 및 원장의 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="9ee2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ee2f-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ee2f-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ee2f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee2f-106">**Get-AzDataLakeStoreChildItemSummary는** 주어진 경로에 대한 콘텐츠 요약을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="9ee2f-107">주어진 경로에 있는 모든 파일의 총 파일 수, 감독 및 총 크기를 재발적으로 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="9ee2f-108">예제</span><span class="sxs-lookup"><span data-stu-id="9ee2f-108">EXAMPLES</span></span>

### <span data-ttu-id="9ee2f-109">예제 1: 폴더의 콘텐츠 요약을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="9ee2f-110">/a 아래에 포함된 총 감독, 파일 및 크기 수를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="9ee2f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee2f-111">PARAMETERS</span></span>

### <span data-ttu-id="9ee2f-112">-Account</span><span class="sxs-lookup"><span data-stu-id="9ee2f-112">-Account</span></span>
<span data-ttu-id="9ee2f-113">파일 프로그램 작업을 실행할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="9ee2f-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="9ee2f-114">-동시성</span><span class="sxs-lookup"><span data-stu-id="9ee2f-114">-Concurrency</span></span>
<span data-ttu-id="9ee2f-115">병렬로 처리된 파일/감독의 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="9ee2f-116">기본값은 시스템 사양에 따라 최상의 노력으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="9ee2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee2f-117">-DefaultProfile</span></span>
<span data-ttu-id="9ee2f-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee2f-119">-Path</span><span class="sxs-lookup"><span data-stu-id="9ee2f-119">-Path</span></span>
<span data-ttu-id="9ee2f-120">검색해야 하는 지정된 Data Lake 계정의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="9ee2f-121">'/folder/file.txt' 형식의 파일 또는 폴더일 수 있습니다. 여기서 DNS 뒤의 첫 번째 '/'는 파일 시스템의 루트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ee2f-122">-Confirm</span></span>
<span data-ttu-id="9ee2f-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee2f-124">-WhatIf</span></span>
<span data-ttu-id="9ee2f-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9ee2f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee2f-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee2f-127">CommonParameters</span></span>
<span data-ttu-id="9ee2f-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee2f-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ee2f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee2f-130">입력</span><span class="sxs-lookup"><span data-stu-id="9ee2f-130">INPUTS</span></span>

### <span data-ttu-id="9ee2f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9ee2f-131">System.String</span></span>

### <span data-ttu-id="9ee2f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9ee2f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9ee2f-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9ee2f-133">System.Int32</span></span>

## <span data-ttu-id="9ee2f-134">출력</span><span class="sxs-lookup"><span data-stu-id="9ee2f-134">OUTPUTS</span></span>

### <span data-ttu-id="9ee2f-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="9ee2f-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="9ee2f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ee2f-136">NOTES</span></span>

## <span data-ttu-id="9ee2f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ee2f-137">RELATED LINKS</span></span>
