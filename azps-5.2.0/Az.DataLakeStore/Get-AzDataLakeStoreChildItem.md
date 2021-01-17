---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352881"
---
# <span data-ttu-id="03ab0-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="03ab0-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="03ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="03ab0-103">Data Lake Store의 폴더에 있는 항목 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="03ab0-104">구문</span><span class="sxs-lookup"><span data-stu-id="03ab0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ab0-105">설명</span><span class="sxs-lookup"><span data-stu-id="03ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="03ab0-106">**Get-AzDataLakeStoreChildItem** cmdlet은 Data Lake Store의 폴더에 있는 항목 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="03ab0-107">예제</span><span class="sxs-lookup"><span data-stu-id="03ab0-107">EXAMPLES</span></span>

### <span data-ttu-id="03ab0-108">예제 1: 폴더의 자식 항목 얻기</span><span class="sxs-lookup"><span data-stu-id="03ab0-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="03ab0-109">이 명령은 MyFiles 폴더에 대한 자식 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="03ab0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03ab0-110">PARAMETERS</span></span>

### <span data-ttu-id="03ab0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="03ab0-111">-Account</span></span>
<span data-ttu-id="03ab0-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="03ab0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ab0-113">-DefaultProfile</span></span>
<span data-ttu-id="03ab0-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ab0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="03ab0-115">-Path</span></span>
<span data-ttu-id="03ab0-116">루트 디렉터리(/)로 시작하는 폴더의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="03ab0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ab0-117">CommonParameters</span></span>
<span data-ttu-id="03ab0-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03ab0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ab0-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03ab0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ab0-120">입력</span><span class="sxs-lookup"><span data-stu-id="03ab0-120">INPUTS</span></span>

### <span data-ttu-id="03ab0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="03ab0-121">System.String</span></span>

### <span data-ttu-id="03ab0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="03ab0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="03ab0-123">출력</span><span class="sxs-lookup"><span data-stu-id="03ab0-123">OUTPUTS</span></span>

### <span data-ttu-id="03ab0-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03ab0-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="03ab0-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03ab0-125">NOTES</span></span>

## <span data-ttu-id="03ab0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03ab0-126">RELATED LINKS</span></span>
