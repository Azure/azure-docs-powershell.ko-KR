---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033966"
---
# <span data-ttu-id="1cba3-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="1cba3-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="1cba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cba3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cba3-103">Data Lake Store의 폴더에 있는 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="1cba3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cba3-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cba3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1cba3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cba3-106">**AzDataLakeStoreChildItem** Cmdlet은 Data Lake store의 폴더에 있는 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="1cba3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1cba3-107">EXAMPLES</span></span>

### <span data-ttu-id="1cba3-108">예제 1: 폴더에 대 한 자식 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="1cba3-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="1cba3-109">이 명령은 MyFiles 폴더에 대 한 자식 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="1cba3-110">변수</span><span class="sxs-lookup"><span data-stu-id="1cba3-110">PARAMETERS</span></span>

### <span data-ttu-id="1cba3-111">-계정</span><span class="sxs-lookup"><span data-stu-id="1cba3-111">-Account</span></span>
<span data-ttu-id="1cba3-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1cba3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cba3-113">-DefaultProfile</span></span>
<span data-ttu-id="1cba3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cba3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1cba3-115">-Path</span></span>
<span data-ttu-id="1cba3-116">루트 디렉터리 (/)로 시작 하는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1cba3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cba3-117">CommonParameters</span></span>
<span data-ttu-id="1cba3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cba3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cba3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cba3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cba3-120">입력</span><span class="sxs-lookup"><span data-stu-id="1cba3-120">INPUTS</span></span>

### <span data-ttu-id="1cba3-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1cba3-121">System.String</span></span>

### <span data-ttu-id="1cba3-122">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="1cba3-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="1cba3-123">출력</span><span class="sxs-lookup"><span data-stu-id="1cba3-123">OUTPUTS</span></span>

### <span data-ttu-id="1cba3-124">DataLakeStore. DataLakeStoreItem/.</span><span class="sxs-lookup"><span data-stu-id="1cba3-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="1cba3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1cba3-125">NOTES</span></span>

## <span data-ttu-id="1cba3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cba3-126">RELATED LINKS</span></span>
