---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176660"
---
# <span data-ttu-id="b56f7-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b56f7-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="b56f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b56f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b56f7-103">입력 ManagementPolicy 작업 그룹 개체에 작업을 추가하거나 작업을 사용하여 ManagementPolicy 작업 그룹 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="b56f7-104">이 개체는 New-AzStorageAccountManagementPolicyRule에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="b56f7-105">구문</span><span class="sxs-lookup"><span data-stu-id="b56f7-105">SYNTAX</span></span>

### <span data-ttu-id="b56f7-106">BaseBlob(기본값)</span><span class="sxs-lookup"><span data-stu-id="b56f7-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b56f7-107">스냅숏</span><span class="sxs-lookup"><span data-stu-id="b56f7-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b56f7-108">설명</span><span class="sxs-lookup"><span data-stu-id="b56f7-108">DESCRIPTION</span></span>
<span data-ttu-id="b56f7-109">**Add-AzStorageAccountManagementPolicyAction** cmdlet은 입력 ManagementPolicy 작업 그룹 개체에 작업을 추가하거나 작업으로 ManagementPolicy 작업 그룹 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="b56f7-110">예제</span><span class="sxs-lookup"><span data-stu-id="b56f7-110">EXAMPLES</span></span>

### <span data-ttu-id="b56f7-111">예제 1: 4개 작업이 있는 ManagementPolicy 작업 그룹 개체를 만든 다음 관리 정책 규칙에 추가하고 Storage 계정에 설정</span><span class="sxs-lookup"><span data-stu-id="b56f7-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="b56f7-112">첫 번째 명령은 ManagementPolicy 작업 그룹 개체를 만들고, 다음 3개 명령은 개체에 3개 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="b56f7-113">그런 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="b56f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b56f7-114">PARAMETERS</span></span>

### <span data-ttu-id="b56f7-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="b56f7-115">-BaseBlobAction</span></span>
<span data-ttu-id="b56f7-116">baseblob에 대한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-116">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f7-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b56f7-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="b56f7-118">생성 후 일수의 나이를 나타내는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f7-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b56f7-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="b56f7-120">마지막으로 수정한 날의 나이를 나타내는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-120">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56f7-121">-DefaultProfile</span></span>
<span data-ttu-id="b56f7-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b56f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b56f7-123">-InputObject</span></span>
<span data-ttu-id="b56f7-124">ManagementPolicy 작업 개체를 입력하는 경우 작업을 입력 작업 개체로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="b56f7-125">입력하지 않은 경우 새 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-125">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b56f7-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="b56f7-126">-SnapshotAction</span></span>
<span data-ttu-id="b56f7-127">스냅숏에 대한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56f7-128">CommonParameters</span></span>
<span data-ttu-id="b56f7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b56f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56f7-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b56f7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56f7-131">입력</span><span class="sxs-lookup"><span data-stu-id="b56f7-131">INPUTS</span></span>

### <span data-ttu-id="b56f7-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="b56f7-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="b56f7-133">출력</span><span class="sxs-lookup"><span data-stu-id="b56f7-133">OUTPUTS</span></span>

### <span data-ttu-id="b56f7-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="b56f7-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="b56f7-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b56f7-135">NOTES</span></span>

## <span data-ttu-id="b56f7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b56f7-136">RELATED LINKS</span></span>
