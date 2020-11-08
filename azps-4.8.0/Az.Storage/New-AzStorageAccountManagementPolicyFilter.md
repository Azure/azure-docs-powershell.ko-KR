---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213802"
---
# <span data-ttu-id="9f1ef-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="9f1ef-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="9f1ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1ef-103">새 AzStorageAccountManagementPolicyRule에서 사용할 수 있는 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="9f1ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f1ef-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f1ef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9f1ef-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1ef-106">**AzStorageAccountManagementPolicyFilter** Cmdlet은 새 AzStorageAccountManagementPolicyRule에서 사용할 수 있는 managementpolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="9f1ef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9f1ef-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1ef-108">예제 1: ManagementPolicy 규칙 필터 개체를 만든 다음 관리 정책 규칙에 추가 하 고 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="9f1ef-109">이 명령은 ManagementPolicy 규칙 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="9f1ef-110">그런 다음 관리 정책 규칙에 추가 하 고 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="9f1ef-111">변수</span><span class="sxs-lookup"><span data-stu-id="9f1ef-111">PARAMETERS</span></span>

### <span data-ttu-id="9f1ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1ef-112">-DefaultProfile</span></span>
<span data-ttu-id="9f1ef-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f1ef-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="9f1ef-114">-PrefixMatch</span></span>
<span data-ttu-id="9f1ef-115">일치 시킬 접두사에 대 한 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="9f1ef-116">접두사 문자열은 컨테이너 이름으로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="9f1ef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1ef-117">CommonParameters</span></span>
<span data-ttu-id="9f1ef-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f1ef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1ef-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f1ef-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1ef-120">입력</span><span class="sxs-lookup"><span data-stu-id="9f1ef-120">INPUTS</span></span>

### <span data-ttu-id="9f1ef-121">않아야</span><span class="sxs-lookup"><span data-stu-id="9f1ef-121">None</span></span>

## <span data-ttu-id="9f1ef-122">출력</span><span class="sxs-lookup"><span data-stu-id="9f1ef-122">OUTPUTS</span></span>

### <span data-ttu-id="9f1ef-123">Microsoft. a. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="9f1ef-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="9f1ef-124">상속자</span><span class="sxs-lookup"><span data-stu-id="9f1ef-124">NOTES</span></span>

## <span data-ttu-id="9f1ef-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f1ef-125">RELATED LINKS</span></span>
