---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 654703a3c5cf1fc18e0f8fbb227b608e91c379bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986827"
---
# <span data-ttu-id="fe120-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="fe120-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="fe120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe120-102">SYNOPSIS</span></span>
<span data-ttu-id="fe120-103">Data Lake Store에서 파일 또는 폴더의 소유자를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fe120-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe120-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe120-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe120-105">DESCRIPTION</span></span>
<span data-ttu-id="fe120-106">**Get-AzDataLakeStoreItemOwner cmdlet은** Data Lake Store에서 파일 또는 폴더의 소유자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fe120-107">예제</span><span class="sxs-lookup"><span data-stu-id="fe120-107">EXAMPLES</span></span>

### <span data-ttu-id="fe120-108">예제 1: 디렉터리의 소유자를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="fe120-109">이 명령은 ContosoADL 계정의 루트 디렉터리에 대한 사용자 소유자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="fe120-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe120-110">PARAMETERS</span></span>

### <span data-ttu-id="fe120-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fe120-111">-Account</span></span>
<span data-ttu-id="fe120-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fe120-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe120-113">-DefaultProfile</span></span>
<span data-ttu-id="fe120-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe120-115">-Path</span><span class="sxs-lookup"><span data-stu-id="fe120-115">-Path</span></span>
<span data-ttu-id="fe120-116">루트 디렉터리(/)로 시작하여 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fe120-117">-Type</span><span class="sxs-lookup"><span data-stu-id="fe120-117">-Type</span></span>
<span data-ttu-id="fe120-118">얻을 소유자 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="fe120-119">이 매개 변수에 대해 허용되는 값은 사용자 및 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="fe120-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe120-120">CommonParameters</span></span>
<span data-ttu-id="fe120-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe120-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe120-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe120-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe120-123">입력</span><span class="sxs-lookup"><span data-stu-id="fe120-123">INPUTS</span></span>

### <span data-ttu-id="fe120-124">System.String</span><span class="sxs-lookup"><span data-stu-id="fe120-124">System.String</span></span>

### <span data-ttu-id="fe120-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fe120-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fe120-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="fe120-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="fe120-127">출력</span><span class="sxs-lookup"><span data-stu-id="fe120-127">OUTPUTS</span></span>

### <span data-ttu-id="fe120-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fe120-128">System.String</span></span>

## <span data-ttu-id="fe120-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe120-129">NOTES</span></span>

## <span data-ttu-id="fe120-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe120-130">RELATED LINKS</span></span>

[<span data-ttu-id="fe120-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="fe120-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


