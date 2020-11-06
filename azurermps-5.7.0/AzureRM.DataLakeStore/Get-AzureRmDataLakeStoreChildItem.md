---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 6477a9f8c3830fa8ca8a74780db560455eb61dfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531728"
---
# <span data-ttu-id="dbeaf-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="dbeaf-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="dbeaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbeaf-102">SYNOPSIS</span></span>
<span data-ttu-id="dbeaf-103">Data Lake Store의 폴더에 있는 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbeaf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbeaf-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbeaf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbeaf-105">DESCRIPTION</span></span>
<span data-ttu-id="dbeaf-106">**AzureRmDataLakeStoreChildItem** Cmdlet은 Data Lake store의 폴더에 있는 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="dbeaf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbeaf-107">EXAMPLES</span></span>

### <span data-ttu-id="dbeaf-108">예제 1: 폴더에 대 한 자식 항목 가져오기</span><span class="sxs-lookup"><span data-stu-id="dbeaf-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="dbeaf-109">이 명령은 MyFiles 폴더에 대 한 자식 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="dbeaf-110">변수</span><span class="sxs-lookup"><span data-stu-id="dbeaf-110">PARAMETERS</span></span>

### <span data-ttu-id="dbeaf-111">-계정</span><span class="sxs-lookup"><span data-stu-id="dbeaf-111">-Account</span></span>
<span data-ttu-id="dbeaf-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbeaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbeaf-113">-DefaultProfile</span></span>
<span data-ttu-id="dbeaf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbeaf-115">-Path</span><span class="sxs-lookup"><span data-stu-id="dbeaf-115">-Path</span></span>
<span data-ttu-id="dbeaf-116">루트 디렉터리 (/)로 시작 하는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbeaf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbeaf-117">CommonParameters</span></span>
<span data-ttu-id="dbeaf-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbeaf-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbeaf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbeaf-120">입력</span><span class="sxs-lookup"><span data-stu-id="dbeaf-120">INPUTS</span></span>

### <span data-ttu-id="dbeaf-121">않아야</span><span class="sxs-lookup"><span data-stu-id="dbeaf-121">None</span></span>
<span data-ttu-id="dbeaf-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbeaf-123">출력</span><span class="sxs-lookup"><span data-stu-id="dbeaf-123">OUTPUTS</span></span>

### <span data-ttu-id="dbeaf-124">IEnumerable<DataLakeStoreItem></span><span class="sxs-lookup"><span data-stu-id="dbeaf-124">IEnumerable<DataLakeStoreItem></span></span>
<span data-ttu-id="dbeaf-125">지정 된 경로 아래에 있는 Data Lake Store 파일 및 폴더의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="dbeaf-125">The list of Data Lake Store files and folders under the specified path.</span></span>

## <span data-ttu-id="dbeaf-126">상속자</span><span class="sxs-lookup"><span data-stu-id="dbeaf-126">NOTES</span></span>

## <span data-ttu-id="dbeaf-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbeaf-127">RELATED LINKS</span></span>

