---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: cf783e708f4e37de209681e65d19f51ea6aea80b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963520"
---
# <span data-ttu-id="66c04-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66c04-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="66c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c04-102">SYNOPSIS</span></span>
<span data-ttu-id="66c04-103">Azure Storage 테이블에 대한 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="66c04-104">구문</span><span class="sxs-lookup"><span data-stu-id="66c04-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c04-105">설명</span><span class="sxs-lookup"><span data-stu-id="66c04-105">DESCRIPTION</span></span>
<span data-ttu-id="66c04-106">**New-AzStorageTableStoredAccessPolicy** cmdlet은 Azure Storage 테이블에 대한 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="66c04-107">예제</span><span class="sxs-lookup"><span data-stu-id="66c04-107">EXAMPLES</span></span>

### <span data-ttu-id="66c04-108">예제 1: 테이블에 저장된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="66c04-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="66c04-109">이 명령은 MyTable이라는 저장소 테이블에 Policy02라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="66c04-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66c04-110">PARAMETERS</span></span>

### <span data-ttu-id="66c04-111">-Context</span><span class="sxs-lookup"><span data-stu-id="66c04-111">-Context</span></span>
<span data-ttu-id="66c04-112">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="66c04-113">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66c04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c04-114">-DefaultProfile</span></span>
<span data-ttu-id="66c04-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c04-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="66c04-116">-ExpiryTime</span></span>
<span data-ttu-id="66c04-117">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c04-118">-권한</span><span class="sxs-lookup"><span data-stu-id="66c04-118">-Permission</span></span>
<span data-ttu-id="66c04-119">저장소 테이블에 액세스하기 위해 저장된 액세스 정책에서 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="66c04-120">이 문자열은 읽기, 추가, 업데이트 및 삭제와 같은 `raud` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-120">It is important to note that this is a string, like `raud` (for Read, Add, Update and Delete).</span></span>

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

### <span data-ttu-id="66c04-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="66c04-121">-Policy</span></span>
<span data-ttu-id="66c04-122">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c04-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="66c04-123">-StartTime</span></span>
<span data-ttu-id="66c04-124">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c04-125">-Table</span><span class="sxs-lookup"><span data-stu-id="66c04-125">-Table</span></span>
<span data-ttu-id="66c04-126">Azure Storage 테이블 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66c04-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c04-127">CommonParameters</span></span>
<span data-ttu-id="66c04-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66c04-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c04-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66c04-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c04-130">입력</span><span class="sxs-lookup"><span data-stu-id="66c04-130">INPUTS</span></span>

### <span data-ttu-id="66c04-131">System.String</span><span class="sxs-lookup"><span data-stu-id="66c04-131">System.String</span></span>

### <span data-ttu-id="66c04-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="66c04-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66c04-133">출력</span><span class="sxs-lookup"><span data-stu-id="66c04-133">OUTPUTS</span></span>

### <span data-ttu-id="66c04-134">System.String</span><span class="sxs-lookup"><span data-stu-id="66c04-134">System.String</span></span>

## <span data-ttu-id="66c04-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66c04-135">NOTES</span></span>

## <span data-ttu-id="66c04-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66c04-136">RELATED LINKS</span></span>

[<span data-ttu-id="66c04-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66c04-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="66c04-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="66c04-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="66c04-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66c04-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="66c04-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66c04-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


