---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002592"
---
# <span data-ttu-id="6eb39-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="6eb39-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="6eb39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb39-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb39-103">Storage 계정을 복원하는 Blob Range 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="6eb39-104">구문</span><span class="sxs-lookup"><span data-stu-id="6eb39-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eb39-105">설명</span><span class="sxs-lookup"><span data-stu-id="6eb39-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb39-106">**New-AzStorageBlobRangeToRestore** cmdlet은 Restore-AzStorageBlobRange에서 사용할 수 있는 Blob 범위 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="6eb39-107">예제</span><span class="sxs-lookup"><span data-stu-id="6eb39-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb39-108">예제 1: 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="6eb39-109">이 명령은 컨테이너1/Blob1(포함)에서 시작하고 container2/Blob2(제외)에서 끝나는 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="6eb39-110">예제 2: 사전순으로 첫 번째 Blob에서 특정 Blob(제외)으로 복원되는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="6eb39-111">이 명령은 사전순의 첫 번째 Blob에서 특정 Blob container2/Blob2(제외)로 복원되는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="6eb39-112">예제 3: 특정 Blob(포함)에서 사전순으로 마지막 Blob으로 복원되는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="6eb39-113">이 명령은 특정 Blob container1/blob1(포함)에서 사전순으로 마지막 Blob으로 복원되는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="6eb39-114">예제 4: 모든 Blob을 복원하는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="6eb39-115">이 명령은 모든 Blob을 복원하는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="6eb39-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6eb39-116">PARAMETERS</span></span>

### <span data-ttu-id="6eb39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb39-117">-DefaultProfile</span></span>
<span data-ttu-id="6eb39-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb39-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="6eb39-119">-EndRange</span></span>
<span data-ttu-id="6eb39-120">Blob 복원 종료 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="6eb39-121">종료 범위는 Blob 복원에서 제외됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="6eb39-122">빈 strng로 설정하여 끝까지 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="6eb39-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="6eb39-123">-StartRange</span></span>
<span data-ttu-id="6eb39-124">Blob 복원 시작 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="6eb39-125">시작 범위는 Blob 복원에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="6eb39-126">시작부터 복원할 빈 문자열로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="6eb39-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb39-127">CommonParameters</span></span>
<span data-ttu-id="6eb39-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb39-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb39-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6eb39-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb39-130">입력</span><span class="sxs-lookup"><span data-stu-id="6eb39-130">INPUTS</span></span>

### <span data-ttu-id="6eb39-131">없음</span><span class="sxs-lookup"><span data-stu-id="6eb39-131">None</span></span>

## <span data-ttu-id="6eb39-132">출력</span><span class="sxs-lookup"><span data-stu-id="6eb39-132">OUTPUTS</span></span>

### <span data-ttu-id="6eb39-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="6eb39-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="6eb39-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6eb39-134">NOTES</span></span>

## <span data-ttu-id="6eb39-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eb39-135">RELATED LINKS</span></span>
