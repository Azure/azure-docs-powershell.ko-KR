---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348333"
---
# <span data-ttu-id="13b97-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13b97-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="13b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b97-102">SYNOPSIS</span></span>
<span data-ttu-id="13b97-103">Storage Blob 컨테이너의 ImmutabilityPolicy를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="13b97-104">구문</span><span class="sxs-lookup"><span data-stu-id="13b97-104">SYNTAX</span></span>

### <span data-ttu-id="13b97-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="13b97-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b97-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="13b97-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b97-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="13b97-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b97-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="13b97-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b97-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="13b97-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b97-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="13b97-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13b97-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="13b97-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13b97-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="13b97-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13b97-113">설명</span><span class="sxs-lookup"><span data-stu-id="13b97-113">DESCRIPTION</span></span>
<span data-ttu-id="13b97-114">**Set-AzRmStorageContainerImmutabilityPolicy** cmdlet은 Storage Blob 컨테이너의 ImmutabilityPolicy를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="13b97-115">예제</span><span class="sxs-lookup"><span data-stu-id="13b97-115">EXAMPLES</span></span>

### <span data-ttu-id="13b97-116">예제 1: Storage 계정 이름 및 컨테이너 이름으로 Storage Blob 컨테이너의 ImmutabilityPolicy 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="13b97-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="13b97-117">이 명령은 Storage 계정 이름 및 컨테이너 이름으로 Storage Blob 컨테이너의 ImmutabilityPolicy를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="13b97-118">예제 2: Storage 계정 개체를 통해 Storage Blob 컨테이너의 ImmutabilityPolicy 확장</span><span class="sxs-lookup"><span data-stu-id="13b97-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="13b97-119">이 명령은 Storage 계정 개체를 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="13b97-120">확장 ImmutabilityPolicy는 ImmutabilityPolicy가 잠긴 후에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="13b97-121">예제 3: Storage Blob 컨테이너의 ImmutabilityPolicy 업데이트</span><span class="sxs-lookup"><span data-stu-id="13b97-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="13b97-122">이 명령은 Storage 컨테이너 개체로 Storage Blob 컨테이너의 ImmutabilityPolicy를 3번 업데이트합니다. 먼저 etag 없이 ImmutabilityPeriod 12일로, etag를 사용하여 ImmutabilityPeriod 9일로, 마지막으로 AllowProtectedAppendWrite를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="13b97-123">예제 4: ImmutabilityPolicy 개체를 통해 Storage Blob 컨테이너의 ImmutabilityPolicy 확장</span><span class="sxs-lookup"><span data-stu-id="13b97-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="13b97-124">이 명령은 ImmutabilityPolicy 개체를 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="13b97-125">확장 ImmutabilityPolicy는 ImmutabilityPolicy가 잠긴 후에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="13b97-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b97-126">PARAMETERS</span></span>

### <span data-ttu-id="13b97-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="13b97-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="13b97-128">이 속성은 잠금 해제된 시간 기반 보존 정책에만 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="13b97-129">이 속성을 사용하도록 설정하면 불연속성 보호 및 규정 준수를 유지하면서 추가 Blob에 새 블록을 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="13b97-130">새 블록만 추가할 수 있으며 기존 블록은 수정하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-131">-Container</span><span class="sxs-lookup"><span data-stu-id="13b97-131">-Container</span></span>
<span data-ttu-id="13b97-132">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="13b97-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="13b97-133">-ContainerName</span></span>
<span data-ttu-id="13b97-134">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="13b97-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b97-135">-DefaultProfile</span></span>
<span data-ttu-id="13b97-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13b97-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="13b97-137">-Etag</span></span>
<span data-ttu-id="13b97-138">몰입성 정책 etag입니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-138">Immutability policy etag.</span></span> <span data-ttu-id="13b97-139">-ExtendPolicy를 지정하지 않으면 Etag는 선택 사항입니다. else Etag가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="13b97-140">-ExtendPolicy</span></span>
<span data-ttu-id="13b97-141">기존 ImmutabilityPolicy를 확장하는 ExtendPolicy를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="13b97-142">ImmutabilityPolicy가 잠긴 후에만 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="13b97-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="13b97-144">생성 이후의 일수에 대한 몰입성 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13b97-145">-InputObject</span></span>
<span data-ttu-id="13b97-146">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="13b97-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b97-147">-ResourceGroupName</span></span>
<span data-ttu-id="13b97-148">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="13b97-149">-StorageAccount</span></span>
<span data-ttu-id="13b97-150">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="13b97-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="13b97-151">-StorageAccountName</span></span>
<span data-ttu-id="13b97-152">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13b97-153">-Confirm</span></span>
<span data-ttu-id="13b97-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13b97-155">-WhatIf</span></span>
<span data-ttu-id="13b97-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="13b97-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13b97-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b97-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b97-158">CommonParameters</span></span>
<span data-ttu-id="13b97-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13b97-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b97-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13b97-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b97-161">입력</span><span class="sxs-lookup"><span data-stu-id="13b97-161">INPUTS</span></span>

### <span data-ttu-id="13b97-162">System.String</span><span class="sxs-lookup"><span data-stu-id="13b97-162">System.String</span></span>

### <span data-ttu-id="13b97-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13b97-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="13b97-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="13b97-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="13b97-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13b97-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="13b97-166">출력</span><span class="sxs-lookup"><span data-stu-id="13b97-166">OUTPUTS</span></span>

### <span data-ttu-id="13b97-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13b97-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="13b97-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13b97-168">NOTES</span></span>

## <span data-ttu-id="13b97-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13b97-169">RELATED LINKS</span></span>
