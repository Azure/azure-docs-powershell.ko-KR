---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a7b47425aad152d8851ff90717698b4c25ef026d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703755"
---
# <span data-ttu-id="6cf8f-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6cf8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf8f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf8f-103">Data Lake Store의 파일 또는 폴더에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cf8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cf8f-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf8f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6cf8f-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf8f-106">**AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store의 파일 또는 폴더에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6cf8f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6cf8f-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf8f-108">예제 1: Data Lake Store의 파일에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6cf8f-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="6cf8f-109">이 명령은 Data Lake Store에서 Test.csv 파일의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="6cf8f-110">변수</span><span class="sxs-lookup"><span data-stu-id="6cf8f-110">PARAMETERS</span></span>

### <span data-ttu-id="6cf8f-111">-계정</span><span class="sxs-lookup"><span data-stu-id="6cf8f-111">-Account</span></span>
<span data-ttu-id="6cf8f-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6cf8f-113">-Path</span><span class="sxs-lookup"><span data-stu-id="6cf8f-113">-Path</span></span>
<span data-ttu-id="6cf8f-114">루트 디렉터리 (/)부터 시작 하 여 항목의 세부 정보를 가져올 데이터 호수 상점 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-114">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6cf8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf8f-115">-DefaultProfile</span></span>
<span data-ttu-id="6cf8f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cf8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf8f-117">CommonParameters</span></span>
<span data-ttu-id="6cf8f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf8f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf8f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf8f-120">입력</span><span class="sxs-lookup"><span data-stu-id="6cf8f-120">INPUTS</span></span>

## <span data-ttu-id="6cf8f-121">출력</span><span class="sxs-lookup"><span data-stu-id="6cf8f-121">OUTPUTS</span></span>

### <span data-ttu-id="6cf8f-122">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-122">DataLakeStoreItem</span></span>
<span data-ttu-id="6cf8f-123">지정 된 경로의 파일 또는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="6cf8f-123">The file or folder at the path specified.</span></span>

## <span data-ttu-id="6cf8f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="6cf8f-124">NOTES</span></span>

## <span data-ttu-id="6cf8f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cf8f-125">RELATED LINKS</span></span>

[<span data-ttu-id="6cf8f-126">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-126">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6cf8f-127">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-127">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="6cf8f-128">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-128">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6cf8f-129">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-129">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6cf8f-130">이동-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-130">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6cf8f-131">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-131">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6cf8f-132">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-132">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6cf8f-133">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6cf8f-133">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


