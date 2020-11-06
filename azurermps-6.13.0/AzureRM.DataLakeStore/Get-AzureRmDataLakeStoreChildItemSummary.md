---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535192"
---
# <span data-ttu-id="b9403-101">Get-AzureRmDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="b9403-101">Get-AzureRmDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="b9403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9403-102">SYNOPSIS</span></span>
<span data-ttu-id="b9403-103">지정한 경로에 포함 된 전체 크기, 파일 및 디렉터리에 대 한 요약 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9403-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9403-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9403-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9403-105">DESCRIPTION</span></span>
<span data-ttu-id="b9403-106">**AzureRmDataLakeStoreChildItemSummary** 는 지정 된 경로에 대 한 콘텐츠 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-106">The **Get-AzureRmDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="b9403-107">지정 된 경로에 있는 모든 파일의 총 파일 수, 디렉터리 및 총 크기를 재귀적으로 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="b9403-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b9403-108">EXAMPLES</span></span>

### <span data-ttu-id="b9403-109">예제 1: 폴더의 콘텐츠 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="b9403-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="b9403-110">이 섹션에는/a 아래에 포함 된 총 디렉터리, 파일 및 해당 크기의 개수가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="b9403-111">변수</span><span class="sxs-lookup"><span data-stu-id="b9403-111">PARAMETERS</span></span>

### <span data-ttu-id="b9403-112">-계정</span><span class="sxs-lookup"><span data-stu-id="b9403-112">-Account</span></span>
<span data-ttu-id="b9403-113">파일 시스템 작업을 실행 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="b9403-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="b9403-114">-동시성</span><span class="sxs-lookup"><span data-stu-id="b9403-114">-Concurrency</span></span>
<span data-ttu-id="b9403-115">병렬로 처리 된 파일/디렉터리 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="b9403-116">기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="b9403-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9403-117">-DefaultProfile</span></span>
<span data-ttu-id="b9403-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9403-119">-Path</span><span class="sxs-lookup"><span data-stu-id="b9403-119">-Path</span></span>
<span data-ttu-id="b9403-120">지정 된 Data Lake account에서 검색 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="b9403-121">'/Folder/file.txt ' 형식으로 된 파일 또는 폴더 일 수 있으며, 여기에서 DNS 뒤의 첫 번째 '/'는 파일 시스템의 루트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="b9403-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b9403-122">-Confirm</span></span>
<span data-ttu-id="b9403-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9403-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9403-124">-WhatIf</span></span>
<span data-ttu-id="b9403-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9403-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9403-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9403-127">CommonParameters</span></span>
<span data-ttu-id="b9403-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9403-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9403-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9403-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9403-130">입력</span><span class="sxs-lookup"><span data-stu-id="b9403-130">INPUTS</span></span>

### <span data-ttu-id="b9403-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b9403-131">System.String</span></span>

### <span data-ttu-id="b9403-132">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="b9403-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b9403-133">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b9403-133">System.Int32</span></span>

## <span data-ttu-id="b9403-134">출력</span><span class="sxs-lookup"><span data-stu-id="b9403-134">OUTPUTS</span></span>

### <span data-ttu-id="b9403-135">DataLakeStore. DataLakeStoreChildItemSummary/.</span><span class="sxs-lookup"><span data-stu-id="b9403-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="b9403-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b9403-136">NOTES</span></span>

## <span data-ttu-id="b9403-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9403-137">RELATED LINKS</span></span>
