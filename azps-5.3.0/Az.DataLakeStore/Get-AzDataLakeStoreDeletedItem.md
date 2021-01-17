---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489171"
---
# <span data-ttu-id="7a512-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="7a512-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="7a512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a512-102">SYNOPSIS</span></span>
<span data-ttu-id="7a512-103">필터와 일치하는 휴지통에서 삭제된 항목을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="7a512-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a512-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a512-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a512-105">DESCRIPTION</span></span>
<span data-ttu-id="7a512-106">**Get-AzDataLakeStoreDeletedItem** cmdlet은 주어진 필터와 일치하는 Data Lake Store에서 삭제된 파일 또는 폴더를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="7a512-107">삭제된 항목의 특성인 OriginalPath, TrashDirPath, Type, CreationTime이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="7a512-108">이 작업은 장기 실행 작업일 수 있습니다. 휴지통에 있는 수백만 파일을 검색해야 할 수 있으며 작업으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="7a512-109">주의: 파일을 삭제하지 않는 것이 가장 좋은 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="7a512-110">파일을 삭제한 후 복원할 수 있는 보장은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="7a512-111">이 API는 화이트리스트를 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="7a512-112">ADL 계정이 화이트리스트에 없는 경우 이 API를 사용하여 구현되지 않은 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="7a512-113">자세한 정보 및 지원은 Microsoft 지원에 문의하세요.</span><span class="sxs-lookup"><span data-stu-id="7a512-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="7a512-114">예제</span><span class="sxs-lookup"><span data-stu-id="7a512-114">EXAMPLES</span></span>

### <span data-ttu-id="7a512-115">예: Data Lake Store에서 파일의 세부 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="7a512-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="7a512-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a512-116">PARAMETERS</span></span>

### <span data-ttu-id="7a512-117">-Account</span><span class="sxs-lookup"><span data-stu-id="7a512-117">-Account</span></span>
<span data-ttu-id="7a512-118">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7a512-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a512-119">-AsJob</span></span>
<span data-ttu-id="7a512-120">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7a512-121">-Count</span><span class="sxs-lookup"><span data-stu-id="7a512-121">-Count</span></span>
<span data-ttu-id="7a512-122">사용자가 찾으하려는 결과 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="7a512-123">쿼리는 Count 결과를 찾거나 전체 휴지통을 검색할 때까지 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a512-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a512-124">-DefaultProfile</span></span>
<span data-ttu-id="7a512-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a512-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="7a512-126">-Filter</span></span>
<span data-ttu-id="7a512-127">검색 쿼리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-127">Specifies the search query.</span></span> <span data-ttu-id="7a512-128">보다 구체적인 값은 더 관련성이 높은 결과를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="7a512-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a512-129">CommonParameters</span></span>
<span data-ttu-id="7a512-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a512-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a512-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a512-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a512-132">입력</span><span class="sxs-lookup"><span data-stu-id="7a512-132">INPUTS</span></span>

### <span data-ttu-id="7a512-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7a512-133">System.String</span></span>

## <span data-ttu-id="7a512-134">출력</span><span class="sxs-lookup"><span data-stu-id="7a512-134">OUTPUTS</span></span>

### <span data-ttu-id="7a512-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="7a512-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="7a512-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a512-136">NOTES</span></span>

## <span data-ttu-id="7a512-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a512-137">RELATED LINKS</span></span>

[<span data-ttu-id="7a512-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="7a512-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)