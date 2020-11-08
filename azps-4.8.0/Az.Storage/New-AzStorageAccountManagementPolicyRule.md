---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213804"
---
# <span data-ttu-id="2766c-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2766c-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="2766c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2766c-102">SYNOPSIS</span></span>
<span data-ttu-id="2766c-103">AzStorageAccountManagementPolicy에서 사용할 수 있는 ManagementPolicy rule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="2766c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2766c-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2766c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2766c-105">DESCRIPTION</span></span>
<span data-ttu-id="2766c-106">**AzStorageAccountManagementPolicyRule** Cmdlet은 집합-AzStorageAccountManagementPolicy에서 사용할 수 있는 managementpolicy rule 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="2766c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2766c-107">EXAMPLES</span></span>

### <span data-ttu-id="2766c-108">예제 1: ManagementPolicy rule 개체를 만든 다음 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="2766c-109">이 명령은 managementpolicy action 그룹 개체에 4 개의 작업, ManagementPolicy 규칙 필터 개체를 포함 하 고, 규칙을 저장소 계정으로 설정 하 여 관리 정책 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="2766c-110">변수</span><span class="sxs-lookup"><span data-stu-id="2766c-110">PARAMETERS</span></span>

### <span data-ttu-id="2766c-111">-작업</span><span class="sxs-lookup"><span data-stu-id="2766c-111">-Action</span></span>
<span data-ttu-id="2766c-112">작업 집합을 정의 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-112">An object that defines the action set.</span></span>
<span data-ttu-id="2766c-113">Cmdlet을 사용 하 여 개체 가져오기 Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2766c-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2766c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2766c-114">-DefaultProfile</span></span>
<span data-ttu-id="2766c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2766c-116">-사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2766c-116">-Disabled</span></span>
<span data-ttu-id="2766c-117">규칙이 설정 된 경우 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-117">The rule is disabled if set it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2766c-118">-필터</span><span class="sxs-lookup"><span data-stu-id="2766c-118">-Filter</span></span>
<span data-ttu-id="2766c-119">필터 집합을 정의 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-119">An object that defines the filter set.</span></span>
<span data-ttu-id="2766c-120">Cmdlet을 사용 하 여 개체 가져오기 New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2766c-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2766c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="2766c-121">-Name</span></span>
<span data-ttu-id="2766c-122">규칙 이름에는 영숫자 문자를 임의로 조합 하 여 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="2766c-123">규칙 이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="2766c-124">정책 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2766c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2766c-125">CommonParameters</span></span>
<span data-ttu-id="2766c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2766c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2766c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2766c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2766c-128">입력</span><span class="sxs-lookup"><span data-stu-id="2766c-128">INPUTS</span></span>

### <span data-ttu-id="2766c-129">않아야</span><span class="sxs-lookup"><span data-stu-id="2766c-129">None</span></span>

## <span data-ttu-id="2766c-130">출력</span><span class="sxs-lookup"><span data-stu-id="2766c-130">OUTPUTS</span></span>

### <span data-ttu-id="2766c-131">Microsoft. a. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2766c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="2766c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2766c-132">NOTES</span></span>

## <span data-ttu-id="2766c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2766c-133">RELATED LINKS</span></span>
