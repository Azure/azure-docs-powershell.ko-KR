---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878370"
---
# <span data-ttu-id="24ab7-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="24ab7-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="24ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="24ab7-103">Data Lake Store에서 파일 또는 폴더의 소유자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="24ab7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24ab7-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ab7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="24ab7-106">**AzDataLakeStoreItemOwner** Cmdlet은 Data Lake store에서 파일 또는 폴더의 소유자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="24ab7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="24ab7-108">예제 1: 디렉터리 소유자 가져오기</span><span class="sxs-lookup"><span data-stu-id="24ab7-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="24ab7-109">이 명령은 ContosoADL account의 루트 디렉터리에 대 한 사용자 소유자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="24ab7-110">변수</span><span class="sxs-lookup"><span data-stu-id="24ab7-110">PARAMETERS</span></span>

### <span data-ttu-id="24ab7-111">-계정</span><span class="sxs-lookup"><span data-stu-id="24ab7-111">-Account</span></span>
<span data-ttu-id="24ab7-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="24ab7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ab7-113">-DefaultProfile</span></span>
<span data-ttu-id="24ab7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24ab7-115">-Path</span><span class="sxs-lookup"><span data-stu-id="24ab7-115">-Path</span></span>
<span data-ttu-id="24ab7-116">루트 디렉터리 (/)부터 시작 하 여 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="24ab7-117">-Type</span><span class="sxs-lookup"><span data-stu-id="24ab7-117">-Type</span></span>
<span data-ttu-id="24ab7-118">가져올 소유자의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="24ab7-119">이 매개 변수에 허용 되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="24ab7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ab7-120">CommonParameters</span></span>
<span data-ttu-id="24ab7-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ab7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ab7-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ab7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ab7-123">입력</span><span class="sxs-lookup"><span data-stu-id="24ab7-123">INPUTS</span></span>

### <span data-ttu-id="24ab7-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24ab7-124">System.String</span></span>

### <span data-ttu-id="24ab7-125">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="24ab7-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="24ab7-126">DataLakeStore DataLakeStoreEnums + Owner (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="24ab7-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="24ab7-127">출력</span><span class="sxs-lookup"><span data-stu-id="24ab7-127">OUTPUTS</span></span>

### <span data-ttu-id="24ab7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24ab7-128">System.String</span></span>

## <span data-ttu-id="24ab7-129">상속자</span><span class="sxs-lookup"><span data-stu-id="24ab7-129">NOTES</span></span>

## <span data-ttu-id="24ab7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24ab7-130">RELATED LINKS</span></span>

[<span data-ttu-id="24ab7-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="24ab7-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


