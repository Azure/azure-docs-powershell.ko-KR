---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305618"
---
# <span data-ttu-id="57b5d-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="57b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="57b5d-103">Data Lake Store의 파일 또는 폴더에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="57b5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57b5d-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="57b5d-106">**AzDataLakeStoreItem** Cmdlet은 Data Lake store의 파일 또는 폴더에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="57b5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="57b5d-108">예제 1: Data Lake Store의 파일에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="57b5d-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="57b5d-109">이 명령은 Data Lake Store에서 Test.csv 파일의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="57b5d-110">변수</span><span class="sxs-lookup"><span data-stu-id="57b5d-110">PARAMETERS</span></span>

### <span data-ttu-id="57b5d-111">-계정</span><span class="sxs-lookup"><span data-stu-id="57b5d-111">-Account</span></span>
<span data-ttu-id="57b5d-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="57b5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b5d-113">-DefaultProfile</span></span>
<span data-ttu-id="57b5d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57b5d-115">-Path</span><span class="sxs-lookup"><span data-stu-id="57b5d-115">-Path</span></span>
<span data-ttu-id="57b5d-116">루트 디렉터리 (/)부터 시작 하 여 항목의 세부 정보를 가져올 데이터 호수 상점 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="57b5d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b5d-117">CommonParameters</span></span>
<span data-ttu-id="57b5d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57b5d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b5d-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57b5d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b5d-120">입력</span><span class="sxs-lookup"><span data-stu-id="57b5d-120">INPUTS</span></span>

### <span data-ttu-id="57b5d-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57b5d-121">System.String</span></span>

### <span data-ttu-id="57b5d-122">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="57b5d-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="57b5d-123">출력</span><span class="sxs-lookup"><span data-stu-id="57b5d-123">OUTPUTS</span></span>

### <span data-ttu-id="57b5d-124">DataLakeStore. DataLakeStoreItem/.</span><span class="sxs-lookup"><span data-stu-id="57b5d-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="57b5d-125">상속자</span><span class="sxs-lookup"><span data-stu-id="57b5d-125">NOTES</span></span>

## <span data-ttu-id="57b5d-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57b5d-126">RELATED LINKS</span></span>

[<span data-ttu-id="57b5d-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="57b5d-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="57b5d-129">가져오기-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="57b5d-130">참가-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="57b5d-131">이동-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="57b5d-132">새로운 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="57b5d-133">제거-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="57b5d-134">테스트-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57b5d-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


