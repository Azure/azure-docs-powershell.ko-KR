---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489164"
---
# <span data-ttu-id="dc839-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="dc839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc839-102">SYNOPSIS</span></span>
<span data-ttu-id="dc839-103">Data Lake Store에서 파일 또는 폴더의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="dc839-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc839-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc839-105">설명</span><span class="sxs-lookup"><span data-stu-id="dc839-105">DESCRIPTION</span></span>
<span data-ttu-id="dc839-106">**Get-AzDataLakeStoreItem** cmdlet은 Data Lake Store의 파일 또는 폴더에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="dc839-107">예제</span><span class="sxs-lookup"><span data-stu-id="dc839-107">EXAMPLES</span></span>

### <span data-ttu-id="dc839-108">예제 1: Data Lake Store에서 파일의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="dc839-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="dc839-109">이 명령은 Data Lake Store에서 Test.csv 파일의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="dc839-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc839-110">PARAMETERS</span></span>

### <span data-ttu-id="dc839-111">-Account</span><span class="sxs-lookup"><span data-stu-id="dc839-111">-Account</span></span>
<span data-ttu-id="dc839-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="dc839-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc839-113">-DefaultProfile</span></span>
<span data-ttu-id="dc839-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc839-115">-Path</span><span class="sxs-lookup"><span data-stu-id="dc839-115">-Path</span></span>
<span data-ttu-id="dc839-116">루트 디렉터리(/)로 시작하는 항목의 세부 정보를 얻을 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="dc839-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc839-117">CommonParameters</span></span>
<span data-ttu-id="dc839-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc839-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc839-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dc839-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc839-120">입력</span><span class="sxs-lookup"><span data-stu-id="dc839-120">INPUTS</span></span>

### <span data-ttu-id="dc839-121">System.String</span><span class="sxs-lookup"><span data-stu-id="dc839-121">System.String</span></span>

### <span data-ttu-id="dc839-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="dc839-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="dc839-123">출력</span><span class="sxs-lookup"><span data-stu-id="dc839-123">OUTPUTS</span></span>

### <span data-ttu-id="dc839-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="dc839-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc839-125">NOTES</span></span>

## <span data-ttu-id="dc839-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc839-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc839-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc839-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="dc839-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="dc839-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc839-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc839-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc839-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc839-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc839-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc839-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


