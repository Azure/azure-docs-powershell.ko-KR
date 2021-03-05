---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976187"
---
# <span data-ttu-id="3caf3-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3caf3-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="3caf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3caf3-102">SYNOPSIS</span></span>
<span data-ttu-id="3caf3-103">Input ManagementPolicy 작업 그룹 개체에 작업을 추가하거나 작업으로 ManagementPolicy 작업 그룹 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="3caf3-104">이 개체는 New-AzStorageAccountManagementPolicyRule에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="3caf3-105">구문</span><span class="sxs-lookup"><span data-stu-id="3caf3-105">SYNTAX</span></span>

### <span data-ttu-id="3caf3-106">BaseBlob(기본값)</span><span class="sxs-lookup"><span data-stu-id="3caf3-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3caf3-107">스냅숏</span><span class="sxs-lookup"><span data-stu-id="3caf3-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3caf3-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="3caf3-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3caf3-109">설명</span><span class="sxs-lookup"><span data-stu-id="3caf3-109">DESCRIPTION</span></span>
<span data-ttu-id="3caf3-110">**Add-AzStorageAccountManagementPolicyAction** cmdlet은 Input ManagementPolicy 작업 그룹 개체에 작업을 추가하거나 작업과 함께 ManagementPolicy 작업 그룹 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="3caf3-111">예제</span><span class="sxs-lookup"><span data-stu-id="3caf3-111">EXAMPLES</span></span>

### <span data-ttu-id="3caf3-112">예제 1: 4개 작업이 있는 ManagementPolicy 작업 그룹 개체를 만든 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="3caf3-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="3caf3-113">첫 번째 명령은 ManagementPolicy 작업 그룹 개체를 만들고 다음 3개 명령은 개체에 3 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="3caf3-114">그런 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="3caf3-115">예제 2: 스냅숏 및 Blob 버전에 대한 6개 작업으로 ManagementPolicy 작업 그룹 개체를 만든 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="3caf3-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="3caf3-116">첫 번째 명령은 ManagementPolicy 작업 그룹 개체를 만들고, 다음 5개 명령은 스냅숏 및 Blob 버전에서 5개 작업을 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="3caf3-117">그런 다음 관리 정책 규칙에 추가하고 Storage 계정으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="3caf3-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3caf3-118">PARAMETERS</span></span>

### <span data-ttu-id="3caf3-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="3caf3-119">-BaseBlobAction</span></span>
<span data-ttu-id="3caf3-120">baseblob에 대한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-120">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="3caf3-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="3caf3-121">-BlobVersionAction</span></span>
<span data-ttu-id="3caf3-122">Blob 버전에 대한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caf3-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3caf3-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="3caf3-124">생성 후 일의 나이를 나타내는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caf3-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3caf3-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="3caf3-126">마지막 수정 후 일의 나이를 나타내는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-126">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="3caf3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caf3-127">-DefaultProfile</span></span>
<span data-ttu-id="3caf3-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3caf3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3caf3-129">-InputObject</span></span>
<span data-ttu-id="3caf3-130">ManagementPolicy 작업 개체를 입력하면 입력 작업 개체로 작업을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="3caf3-131">입력하지 않은 경우 새 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-131">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="3caf3-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="3caf3-132">-SnapshotAction</span></span>
<span data-ttu-id="3caf3-133">스냅숏에 대한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caf3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caf3-134">CommonParameters</span></span>
<span data-ttu-id="3caf3-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3caf3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caf3-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3caf3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caf3-137">입력</span><span class="sxs-lookup"><span data-stu-id="3caf3-137">INPUTS</span></span>

### <span data-ttu-id="3caf3-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3caf3-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3caf3-139">출력</span><span class="sxs-lookup"><span data-stu-id="3caf3-139">OUTPUTS</span></span>

### <span data-ttu-id="3caf3-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3caf3-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3caf3-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3caf3-141">NOTES</span></span>

## <span data-ttu-id="3caf3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3caf3-142">RELATED LINKS</span></span>
