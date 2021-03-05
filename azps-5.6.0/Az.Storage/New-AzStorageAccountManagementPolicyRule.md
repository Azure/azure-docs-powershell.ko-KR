---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 73606a2af9ff0c5e948d407dd5da1f21df5d14b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002619"
---
# <span data-ttu-id="13399-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="13399-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="13399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13399-102">SYNOPSIS</span></span>
<span data-ttu-id="13399-103">Set-AzStorageAccountManagementPolicy에서 사용할 수 있는 ManagementPolicy 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13399-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="13399-104">구문</span><span class="sxs-lookup"><span data-stu-id="13399-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13399-105">설명</span><span class="sxs-lookup"><span data-stu-id="13399-105">DESCRIPTION</span></span>
<span data-ttu-id="13399-106">**New-AzStorageAccountManagementPolicyRule** cmdlet은 Set-AzStorageAccountManagementPolicy에서 사용할 수 있는 ManagementPolicy 규칙 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13399-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="13399-107">예제</span><span class="sxs-lookup"><span data-stu-id="13399-107">EXAMPLES</span></span>

### <span data-ttu-id="13399-108">예제 1: ManagementPolicy 규칙 개체를 만든 다음 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="13399-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="13399-109">이 명령은 ManagementPolicy 작업 그룹 개체에 4개 작업, ManagementPolicy 규칙 필터 개체가 포함된 ManagementPolicy 규칙 개체를 만든 다음 저장소 계정으로 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="13399-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="13399-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="13399-110">PARAMETERS</span></span>

### <span data-ttu-id="13399-111">-Action</span><span class="sxs-lookup"><span data-stu-id="13399-111">-Action</span></span>
<span data-ttu-id="13399-112">작업 집합을 정의하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13399-112">An object that defines the action set.</span></span>
<span data-ttu-id="13399-113">cmdlet을 Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="13399-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="13399-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13399-114">-DefaultProfile</span></span>
<span data-ttu-id="13399-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13399-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13399-116">-사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="13399-116">-Disabled</span></span>
<span data-ttu-id="13399-117">규칙을 설정하면 규칙이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="13399-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="13399-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="13399-118">-Filter</span></span>
<span data-ttu-id="13399-119">필터 집합을 정의하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13399-119">An object that defines the filter set.</span></span>
<span data-ttu-id="13399-120">cmdlet을 New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="13399-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="13399-121">-Name</span><span class="sxs-lookup"><span data-stu-id="13399-121">-Name</span></span>
<span data-ttu-id="13399-122">규칙 이름은 알파 숫자 문자의 조합을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13399-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="13399-123">규칙 이름은 대소문자 구분입니다.</span><span class="sxs-lookup"><span data-stu-id="13399-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="13399-124">정책 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13399-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="13399-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13399-125">CommonParameters</span></span>
<span data-ttu-id="13399-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13399-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13399-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13399-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13399-128">입력</span><span class="sxs-lookup"><span data-stu-id="13399-128">INPUTS</span></span>

### <span data-ttu-id="13399-129">없음</span><span class="sxs-lookup"><span data-stu-id="13399-129">None</span></span>

## <span data-ttu-id="13399-130">출력</span><span class="sxs-lookup"><span data-stu-id="13399-130">OUTPUTS</span></span>

### <span data-ttu-id="13399-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="13399-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="13399-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13399-132">NOTES</span></span>

## <span data-ttu-id="13399-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13399-133">RELATED LINKS</span></span>
