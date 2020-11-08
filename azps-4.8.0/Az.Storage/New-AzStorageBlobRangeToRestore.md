---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213799"
---
# <span data-ttu-id="a3fac-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="a3fac-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="a3fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3fac-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fac-103">저장소 계정을 복원 하는 Blob Range 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="a3fac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3fac-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3fac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3fac-105">DESCRIPTION</span></span>
<span data-ttu-id="a3fac-106">**AzStorageBlobRangeToRestore** Cmdlet은 Restore-AzStorageBlobRange에서 사용할 수 있는 Blob range 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="a3fac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a3fac-107">EXAMPLES</span></span>

### <span data-ttu-id="a3fac-108">예제 1: 복원할 blob 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="a3fac-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="a3fac-109">이 명령은 container1/blob1 (포함)에서 시작 하 고 container2/blob2 (exclude)에서 끝나는 blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="a3fac-110">예제 2: 사전순으로 첫 번째 blob에서 특정 blob (제외)로 복원 하는 blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="a3fac-111">이 명령은 사전순의 첫 번째 blob에서 특정 blob container2/blob2 (exclude)으로 복원 하는 blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="a3fac-112">예제 3: 특정 blob (포함)에서 마지막 blob까지 사전순으로 복원 하는 blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="a3fac-113">이 명령은 특정 blob container1/blob1 (포함)에서 마지막 blob까지 사전순으로 복원 하는 blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="a3fac-114">예제 4: 모든 blob을 복원 하는 blob 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="a3fac-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="a3fac-115">이 명령은 모든 blob을 복원 하는 blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="a3fac-116">변수</span><span class="sxs-lookup"><span data-stu-id="a3fac-116">PARAMETERS</span></span>

### <span data-ttu-id="a3fac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fac-117">-DefaultProfile</span></span>
<span data-ttu-id="a3fac-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3fac-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="a3fac-119">-EndRange</span></span>
<span data-ttu-id="a3fac-120">Blob 복원 종료 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="a3fac-121">Restore blob에서 End 범위가 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="a3fac-122">이를 빈 strng로 설정 하 여 끝까지 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fac-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="a3fac-123">-StartRange</span></span>
<span data-ttu-id="a3fac-124">Blob 복원 시작 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="a3fac-125">시작 범위는 복원 blob에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="a3fac-126">처음부터 복원할 수 있도록 빈 문자열로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fac-127">CommonParameters</span></span>
<span data-ttu-id="a3fac-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fac-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3fac-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fac-130">입력</span><span class="sxs-lookup"><span data-stu-id="a3fac-130">INPUTS</span></span>

### <span data-ttu-id="a3fac-131">않아야</span><span class="sxs-lookup"><span data-stu-id="a3fac-131">None</span></span>

## <span data-ttu-id="a3fac-132">출력</span><span class="sxs-lookup"><span data-stu-id="a3fac-132">OUTPUTS</span></span>

### <span data-ttu-id="a3fac-133">PSBlobRestoreRange를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3fac-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="a3fac-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a3fac-134">NOTES</span></span>

## <span data-ttu-id="a3fac-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3fac-135">RELATED LINKS</span></span>
