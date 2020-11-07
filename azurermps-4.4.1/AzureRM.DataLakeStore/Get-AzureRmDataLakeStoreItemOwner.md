---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703752"
---
# <span data-ttu-id="858cb-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="858cb-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="858cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858cb-102">SYNOPSIS</span></span>
<span data-ttu-id="858cb-103">Data Lake Store에서 파일 또는 폴더의 소유자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="858cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="858cb-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="858cb-105">DESCRIPTION</span></span>
<span data-ttu-id="858cb-106">**AzureRmDataLakeStoreItemOwner** Cmdlet은 Data Lake store에서 파일 또는 폴더의 소유자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="858cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="858cb-107">EXAMPLES</span></span>

### <span data-ttu-id="858cb-108">예제 1: 디렉터리 소유자 가져오기</span><span class="sxs-lookup"><span data-stu-id="858cb-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="858cb-109">이 명령은 ContosoADL account의 루트 디렉터리에 대 한 사용자 소유자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="858cb-110">변수</span><span class="sxs-lookup"><span data-stu-id="858cb-110">PARAMETERS</span></span>

### <span data-ttu-id="858cb-111">-계정</span><span class="sxs-lookup"><span data-stu-id="858cb-111">-Account</span></span>
<span data-ttu-id="858cb-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="858cb-113">-Path</span><span class="sxs-lookup"><span data-stu-id="858cb-113">-Path</span></span>
<span data-ttu-id="858cb-114">루트 디렉터리 (/)부터 시작 하 여 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="858cb-115">-Type</span><span class="sxs-lookup"><span data-stu-id="858cb-115">-Type</span></span>
<span data-ttu-id="858cb-116">가져올 소유자의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="858cb-117">이 매개 변수에 허용 되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-117">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858cb-118">-DefaultProfile</span></span>
<span data-ttu-id="858cb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="858cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858cb-120">CommonParameters</span></span>
<span data-ttu-id="858cb-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858cb-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858cb-123">입력</span><span class="sxs-lookup"><span data-stu-id="858cb-123">INPUTS</span></span>

## <span data-ttu-id="858cb-124">출력</span><span class="sxs-lookup"><span data-stu-id="858cb-124">OUTPUTS</span></span>

### <span data-ttu-id="858cb-125">이름</span><span class="sxs-lookup"><span data-stu-id="858cb-125">string</span></span>
<span data-ttu-id="858cb-126">지정 된 항목의 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="858cb-126">The owner of the specified item.</span></span>

## <span data-ttu-id="858cb-127">상속자</span><span class="sxs-lookup"><span data-stu-id="858cb-127">NOTES</span></span>

## <span data-ttu-id="858cb-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="858cb-128">RELATED LINKS</span></span>

[<span data-ttu-id="858cb-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="858cb-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


