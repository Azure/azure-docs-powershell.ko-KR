---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002635"
---
# <span data-ttu-id="237ba-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="237ba-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="237ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="237ba-102">SYNOPSIS</span></span>
<span data-ttu-id="237ba-103">New-AzStorageAccountManagementPolicyRule에서 사용할 수 있는 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="237ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="237ba-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="237ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="237ba-105">DESCRIPTION</span></span>
<span data-ttu-id="237ba-106">**New-AzStorageAccountManagementPolicyFilter** cmdlet은 New-AzStorageAccountManagementPolicyRule에서 사용할 수 있는 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="237ba-107">예제</span><span class="sxs-lookup"><span data-stu-id="237ba-107">EXAMPLES</span></span>

### <span data-ttu-id="237ba-108">예제 1: ManagementPolicy 규칙 필터 개체를 만든 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="237ba-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="237ba-109">이 명령은 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="237ba-110">그런 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="237ba-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="237ba-111">PARAMETERS</span></span>

### <span data-ttu-id="237ba-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="237ba-112">-BlobType</span></span>
<span data-ttu-id="237ba-113">일치할 Blobtype에 대한 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="237ba-114">현재 blockBlob은 모든 계층화 및 삭제 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="237ba-115">추가Blob에 대해 삭제 작업만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237ba-116">-DefaultProfile</span></span>
<span data-ttu-id="237ba-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="237ba-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="237ba-118">-PrefixMatch</span></span>
<span data-ttu-id="237ba-119">일치할 도두사에 대한 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="237ba-120">연결선 문자열은 컨테이너 이름으로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-120">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237ba-121">CommonParameters</span></span>
<span data-ttu-id="237ba-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="237ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237ba-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="237ba-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237ba-124">입력</span><span class="sxs-lookup"><span data-stu-id="237ba-124">INPUTS</span></span>

### <span data-ttu-id="237ba-125">없음</span><span class="sxs-lookup"><span data-stu-id="237ba-125">None</span></span>

## <span data-ttu-id="237ba-126">출력</span><span class="sxs-lookup"><span data-stu-id="237ba-126">OUTPUTS</span></span>

### <span data-ttu-id="237ba-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="237ba-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="237ba-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="237ba-128">NOTES</span></span>

## <span data-ttu-id="237ba-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="237ba-129">RELATED LINKS</span></span>
