---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492747"
---
# <span data-ttu-id="82261-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="82261-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="82261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82261-102">SYNOPSIS</span></span>
<span data-ttu-id="82261-103">New-AzStorageAccountManagementPolicyRule에서 사용할 수 있는 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82261-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="82261-104">구문</span><span class="sxs-lookup"><span data-stu-id="82261-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82261-105">설명</span><span class="sxs-lookup"><span data-stu-id="82261-105">DESCRIPTION</span></span>
<span data-ttu-id="82261-106">**New-AzStorageAccountManagementPolicyFilter** cmdlet은 New-AzStorageAccountManagementPolicyRule에서 사용할 수 있는 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82261-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="82261-107">예제</span><span class="sxs-lookup"><span data-stu-id="82261-107">EXAMPLES</span></span>

### <span data-ttu-id="82261-108">예제 1: ManagementPolicy 규칙 필터 개체를 만든 다음 관리 정책 규칙에 추가하고 Storage 계정에 설정</span><span class="sxs-lookup"><span data-stu-id="82261-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="82261-109">이 명령은 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82261-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="82261-110">그런 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="82261-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="82261-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82261-111">PARAMETERS</span></span>

### <span data-ttu-id="82261-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82261-112">-DefaultProfile</span></span>
<span data-ttu-id="82261-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82261-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82261-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="82261-114">-PrefixMatch</span></span>
<span data-ttu-id="82261-115">일치할 연결에 대한 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="82261-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="82261-116">연결 문자열은 컨테이너 이름으로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82261-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="82261-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82261-117">CommonParameters</span></span>
<span data-ttu-id="82261-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82261-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82261-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82261-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82261-120">입력</span><span class="sxs-lookup"><span data-stu-id="82261-120">INPUTS</span></span>

### <span data-ttu-id="82261-121">없음</span><span class="sxs-lookup"><span data-stu-id="82261-121">None</span></span>

## <span data-ttu-id="82261-122">출력</span><span class="sxs-lookup"><span data-stu-id="82261-122">OUTPUTS</span></span>

### <span data-ttu-id="82261-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="82261-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="82261-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82261-124">NOTES</span></span>

## <span data-ttu-id="82261-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82261-125">RELATED LINKS</span></span>
