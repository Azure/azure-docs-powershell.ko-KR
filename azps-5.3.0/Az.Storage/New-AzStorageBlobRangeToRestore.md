---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493140"
---
# <span data-ttu-id="66db4-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="66db4-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="66db4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66db4-102">SYNOPSIS</span></span>
<span data-ttu-id="66db4-103">Storage 계정을 복원하는 Blob 범위 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="66db4-104">구문</span><span class="sxs-lookup"><span data-stu-id="66db4-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66db4-105">설명</span><span class="sxs-lookup"><span data-stu-id="66db4-105">DESCRIPTION</span></span>
<span data-ttu-id="66db4-106">**New-AzStorageBlobRangeToRestore** cmdlet은 Restore-AzStorageBlobRange에서 사용할 수 있는 Blob 범위 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="66db4-107">예제</span><span class="sxs-lookup"><span data-stu-id="66db4-107">EXAMPLES</span></span>

### <span data-ttu-id="66db4-108">예제 1: 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="66db4-109">이 명령은 container1/blob1(포함)에서 시작하여 container2/blob2(제외)에서 끝나는 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="66db4-110">예제 2: 첫 번째 Blob에서 사전순으로 특정 Blob으로 복원할 Blob 범위를 만듭니다(제외).</span><span class="sxs-lookup"><span data-stu-id="66db4-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="66db4-111">이 명령은 사전순의 첫 번째 Blob에서 특정 Blob container2/blob2(제외)로 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="66db4-112">예제 3: 특정 Blob(포함)에서 사전순으로 마지막 Blob으로 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="66db4-113">이 명령은 특정 Blob container1/blob1(포함)에서 사전순으로 마지막 Blob으로 복원할 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="66db4-114">예제 4: 모든 Blob을 복원하는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="66db4-115">이 명령은 모든 Blob을 복원하는 Blob 범위를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="66db4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66db4-116">PARAMETERS</span></span>

### <span data-ttu-id="66db4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66db4-117">-DefaultProfile</span></span>
<span data-ttu-id="66db4-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66db4-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="66db4-119">-EndRange</span></span>
<span data-ttu-id="66db4-120">Blob 복원 종료 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="66db4-121">끝 범위는 복원 Blob에서 제외됩니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="66db4-122">빈 strng로 설정하여 끝으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="66db4-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="66db4-123">-StartRange</span></span>
<span data-ttu-id="66db4-124">Blob 복원 시작 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="66db4-125">시작 범위는 Blob 복원에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="66db4-126">빈 문자열로 설정하여 원래 상태로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="66db4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66db4-127">CommonParameters</span></span>
<span data-ttu-id="66db4-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66db4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66db4-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66db4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66db4-130">입력</span><span class="sxs-lookup"><span data-stu-id="66db4-130">INPUTS</span></span>

### <span data-ttu-id="66db4-131">없음</span><span class="sxs-lookup"><span data-stu-id="66db4-131">None</span></span>

## <span data-ttu-id="66db4-132">출력</span><span class="sxs-lookup"><span data-stu-id="66db4-132">OUTPUTS</span></span>

### <span data-ttu-id="66db4-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="66db4-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="66db4-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66db4-134">NOTES</span></span>

## <span data-ttu-id="66db4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66db4-135">RELATED LINKS</span></span>
