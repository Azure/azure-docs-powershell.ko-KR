---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305627"
---
# <span data-ttu-id="98c6e-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="98c6e-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="98c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="98c6e-103">필터와 일치 하는 휴지통에서 삭제 된 항목을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="98c6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98c6e-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c6e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="98c6e-105">DESCRIPTION</span></span>
<span data-ttu-id="98c6e-106">**AzDataLakeStoreDeletedItem** cmdlet은 지정 된 필터와 일치 하는 데이터 호수 저장소에서 삭제 된 파일 또는 폴더를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="98c6e-107">삭제 된 항목-OriginalPath, TrashDirPath, Type, CreationTime의 다음 특성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="98c6e-108">휴지통에서 수백만 개의 파일을 검색 해야 할 수 있으므로 작업으로 실행할 수 있으므로 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="98c6e-109">주의: Undeleting 파일은 작업을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="98c6e-110">삭제 된 파일은 복원할 수 없다는 보장이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="98c6e-111">이 API의 사용은 whitelisting를 통해 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="98c6e-112">ADL 계정이 허용 목록이 아닌 경우이 api를 사용 하면 구현 되지 않은 예외가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="98c6e-113">자세한 정보 및 지원은 Microsoft 지원에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="98c6e-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="98c6e-114">예제의</span><span class="sxs-lookup"><span data-stu-id="98c6e-114">EXAMPLES</span></span>

### <span data-ttu-id="98c6e-115">예: Data Lake Store의 파일에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="98c6e-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="98c6e-116">변수</span><span class="sxs-lookup"><span data-stu-id="98c6e-116">PARAMETERS</span></span>

### <span data-ttu-id="98c6e-117">-계정</span><span class="sxs-lookup"><span data-stu-id="98c6e-117">-Account</span></span>
<span data-ttu-id="98c6e-118">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="98c6e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98c6e-119">-AsJob</span></span>
<span data-ttu-id="98c6e-120">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="98c6e-121">-카운트</span><span class="sxs-lookup"><span data-stu-id="98c6e-121">-Count</span></span>
<span data-ttu-id="98c6e-122">사용자가 찾으려고 하는 결과의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="98c6e-123">쿼리는 개수 결과를 찾을 때까지 실행 되거나 휴지통 전체를 검색 하 여 먼저 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="98c6e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c6e-124">-DefaultProfile</span></span>
<span data-ttu-id="98c6e-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c6e-126">-필터</span><span class="sxs-lookup"><span data-stu-id="98c6e-126">-Filter</span></span>
<span data-ttu-id="98c6e-127">검색 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-127">Specifies the search query.</span></span> <span data-ttu-id="98c6e-128">보다 구체적인 값을 통해 더 관련성이 높은 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="98c6e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c6e-129">CommonParameters</span></span>
<span data-ttu-id="98c6e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c6e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c6e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c6e-132">입력</span><span class="sxs-lookup"><span data-stu-id="98c6e-132">INPUTS</span></span>

### <span data-ttu-id="98c6e-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="98c6e-133">System.String</span></span>

## <span data-ttu-id="98c6e-134">출력</span><span class="sxs-lookup"><span data-stu-id="98c6e-134">OUTPUTS</span></span>

### <span data-ttu-id="98c6e-135">DataLakeStore를<목록에서 DataLakeStoreDeletedItem>를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c6e-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="98c6e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="98c6e-136">NOTES</span></span>

## <span data-ttu-id="98c6e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98c6e-137">RELATED LINKS</span></span>

[<span data-ttu-id="98c6e-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="98c6e-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)