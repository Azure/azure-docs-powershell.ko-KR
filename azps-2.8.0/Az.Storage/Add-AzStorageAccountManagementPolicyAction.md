---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 73384827b5af2b3370eca1eee5a90066a89b8e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874065"
---
# <span data-ttu-id="822cb-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="822cb-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="822cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="822cb-102">SYNOPSIS</span></span>
<span data-ttu-id="822cb-103">입력 관리 정책 작업 그룹 개체에 작업을 추가 하거나 작업을 사용 하 여 ManagementPolicy Action Group 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="822cb-104">이 개체는 New-AzStorageAccountManagementPolicyRule에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="822cb-105">구문과</span><span class="sxs-lookup"><span data-stu-id="822cb-105">SYNTAX</span></span>

### <span data-ttu-id="822cb-106">BaseBlob (기본값)</span><span class="sxs-lookup"><span data-stu-id="822cb-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="822cb-107">스냅샷은</span><span class="sxs-lookup"><span data-stu-id="822cb-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="822cb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="822cb-108">DESCRIPTION</span></span>
<span data-ttu-id="822cb-109">**AzStorageAccountManagementPolicyAction** cmdlet은 입력 Managementpolicy 작업 그룹 개체에 작업을 추가 하거나 작업을 사용 하 여 Managementpolicy action group 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="822cb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="822cb-110">EXAMPLES</span></span>

### <span data-ttu-id="822cb-111">예제 1:4 개의 작업을 포함 하는 ManagementPolicy Action Group 개체를 만든 다음 관리 정책 규칙에 추가 하 고 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="822cb-112">첫 번째 명령은 ManagementPolicy 작업 그룹 개체를 만들고 다음 세 개의 명령은 개체에 세 개의 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="822cb-113">그런 다음 관리 정책 규칙에 추가 하 고 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="822cb-114">변수</span><span class="sxs-lookup"><span data-stu-id="822cb-114">PARAMETERS</span></span>

### <span data-ttu-id="822cb-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="822cb-115">-BaseBlobAction</span></span>
<span data-ttu-id="822cb-116">Baseblob에 대 한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="822cb-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="822cb-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="822cb-118">생성 후 보존 기간 (일)을 나타내는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-118">Integer value indicating the age in days after creation.</span></span>

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

### <span data-ttu-id="822cb-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="822cb-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="822cb-120">마지막 수정 이후 보존 기간 (일)을 나타내는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="822cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822cb-121">-DefaultProfile</span></span>
<span data-ttu-id="822cb-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="822cb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="822cb-123">-InputObject</span></span>
<span data-ttu-id="822cb-124">ManagementPolicy Action 개체를 입력 하는 경우 동작을 입력 동작 개체에 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="822cb-125">입력 하지 않으면 새 동작 개체가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="822cb-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="822cb-126">-SnapshotAction</span></span>
<span data-ttu-id="822cb-127">스냅숏에 대 한 관리 정책 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-127">The management policy action for snapshot.</span></span>

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

### <span data-ttu-id="822cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822cb-128">CommonParameters</span></span>
<span data-ttu-id="822cb-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="822cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822cb-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822cb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822cb-131">입력</span><span class="sxs-lookup"><span data-stu-id="822cb-131">INPUTS</span></span>

### <span data-ttu-id="822cb-132">Microsoft. a. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="822cb-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="822cb-133">출력</span><span class="sxs-lookup"><span data-stu-id="822cb-133">OUTPUTS</span></span>

### <span data-ttu-id="822cb-134">Microsoft. a. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="822cb-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="822cb-135">상속자</span><span class="sxs-lookup"><span data-stu-id="822cb-135">NOTES</span></span>

## <span data-ttu-id="822cb-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="822cb-136">RELATED LINKS</span></span>
