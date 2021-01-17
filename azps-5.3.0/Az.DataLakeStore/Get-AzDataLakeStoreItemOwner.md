---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489143"
---
# <span data-ttu-id="5804f-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="5804f-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="5804f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5804f-102">SYNOPSIS</span></span>
<span data-ttu-id="5804f-103">Data Lake Store에서 파일 또는 폴더의 소유자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5804f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5804f-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5804f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5804f-105">DESCRIPTION</span></span>
<span data-ttu-id="5804f-106">**Get-AzDataLakeStoreItemOwner** cmdlet은 Data Lake Store에서 파일 또는 폴더의 소유자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5804f-107">예제</span><span class="sxs-lookup"><span data-stu-id="5804f-107">EXAMPLES</span></span>

### <span data-ttu-id="5804f-108">예제 1: 디렉터리의 소유자를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="5804f-109">이 명령은 ContosoADL 계정의 루트 디렉터리에 대한 사용자 소유자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="5804f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5804f-110">PARAMETERS</span></span>

### <span data-ttu-id="5804f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5804f-111">-Account</span></span>
<span data-ttu-id="5804f-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5804f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5804f-113">-DefaultProfile</span></span>
<span data-ttu-id="5804f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5804f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="5804f-115">-Path</span></span>
<span data-ttu-id="5804f-116">루트 디렉터리(/)로 시작하는 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5804f-117">-Type</span><span class="sxs-lookup"><span data-stu-id="5804f-117">-Type</span></span>
<span data-ttu-id="5804f-118">얻을 소유자의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="5804f-119">이 매개 변수에 허용되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="5804f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5804f-120">CommonParameters</span></span>
<span data-ttu-id="5804f-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5804f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5804f-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5804f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5804f-123">입력</span><span class="sxs-lookup"><span data-stu-id="5804f-123">INPUTS</span></span>

### <span data-ttu-id="5804f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5804f-124">System.String</span></span>

### <span data-ttu-id="5804f-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5804f-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5804f-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="5804f-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="5804f-127">출력</span><span class="sxs-lookup"><span data-stu-id="5804f-127">OUTPUTS</span></span>

### <span data-ttu-id="5804f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5804f-128">System.String</span></span>

## <span data-ttu-id="5804f-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5804f-129">NOTES</span></span>

## <span data-ttu-id="5804f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5804f-130">RELATED LINKS</span></span>

[<span data-ttu-id="5804f-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="5804f-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


