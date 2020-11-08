---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213789"
---
# <span data-ttu-id="d87d7-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d87d7-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d87d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d87d7-103">저장소 blob 컨테이너의 ImmutabilityPolicy를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d87d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d87d7-104">SYNTAX</span></span>

### <span data-ttu-id="d87d7-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d87d7-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d7-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="d87d7-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d7-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d7-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d7-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d7-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d7-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d87d7-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87d7-113">설명은</span><span class="sxs-lookup"><span data-stu-id="d87d7-113">DESCRIPTION</span></span>
<span data-ttu-id="d87d7-114">**AzRmStorageContainerImmutabilityPolicy** Cmdlet은 저장소 blob 컨테이너의 ImmutabilityPolicy를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d87d7-115">예제의</span><span class="sxs-lookup"><span data-stu-id="d87d7-115">EXAMPLES</span></span>

### <span data-ttu-id="d87d7-116">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d87d7-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="d87d7-117">이 명령은 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d87d7-118">예제 2: 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 확장</span><span class="sxs-lookup"><span data-stu-id="d87d7-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="d87d7-119">이 명령은 저장소 blob 컨테이너의 ImmutabilityPolicy를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="d87d7-120">ImmutabilityPolicy Extend는 ImmutabilityPolicy이 잠긴 후에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="d87d7-121">예제 3: 저장소 blob 컨테이너의 ImmutabilityPolicy 업데이트</span><span class="sxs-lookup"><span data-stu-id="d87d7-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="d87d7-122">이 명령은 저장소 컨테이너 개체가 3 번 인 저장소 blob 컨테이너의 ImmutabilityPolicy를 업데이트 합니다. 먼저 etag 없이 12 일을 ImmutabilityPeriod 다음 etag를 사용 하 여 9 일간 ImmutabilityPeriod 합니다. 마지막으로 사용 가능 AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="d87d7-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="d87d7-123">예제 4: ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 확장</span><span class="sxs-lookup"><span data-stu-id="d87d7-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="d87d7-124">이 명령은 ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="d87d7-125">ImmutabilityPolicy Extend는 ImmutabilityPolicy이 잠긴 후에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="d87d7-126">변수</span><span class="sxs-lookup"><span data-stu-id="d87d7-126">PARAMETERS</span></span>

### <span data-ttu-id="d87d7-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="d87d7-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="d87d7-128">이 속성은 잠기지 않은 시간 기반 보존 정책에 대해서만 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="d87d7-129">이 속성을 사용 하도록 설정 하면 불변성 보호 및 준수를 유지 하면서 추가 blob에 새 블록을 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="d87d7-130">새 블록만 추가할 수 있으며 기존 블록은 수정 하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="d87d7-131">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="d87d7-131">-Container</span></span>
<span data-ttu-id="d87d7-132">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="d87d7-132">Storage container object</span></span>

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

### <span data-ttu-id="d87d7-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d87d7-133">-ContainerName</span></span>
<span data-ttu-id="d87d7-134">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="d87d7-134">Container Name</span></span>

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

### <span data-ttu-id="d87d7-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87d7-135">-DefaultProfile</span></span>
<span data-ttu-id="d87d7-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d87d7-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="d87d7-137">-Etag</span></span>
<span data-ttu-id="d87d7-138">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="d87d7-138">Immutability policy etag.</span></span> <span data-ttu-id="d87d7-139">-ExtendPolicy가 지정 되지 않은 경우 Etag는 선택 사항입니다. 사용자 Etag가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="d87d7-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="d87d7-140">-ExtendPolicy</span></span>
<span data-ttu-id="d87d7-141">ExtendPolicy를 표시 하 여 기존 ImmutabilityPolicy를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="d87d7-142">ImmutabilityPolicy이 잠긴 후에만 연장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="d87d7-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="d87d7-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="d87d7-144">일 단위로 만든 후의 불변성 기간.</span><span class="sxs-lookup"><span data-stu-id="d87d7-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="d87d7-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d87d7-145">-InputObject</span></span>
<span data-ttu-id="d87d7-146">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="d87d7-146">Container Name</span></span>

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

### <span data-ttu-id="d87d7-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87d7-147">-ResourceGroupName</span></span>
<span data-ttu-id="d87d7-148">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="d87d7-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d87d7-149">-StorageAccount</span></span>
<span data-ttu-id="d87d7-150">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d87d7-150">Storage account object</span></span>

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

### <span data-ttu-id="d87d7-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d87d7-151">-StorageAccountName</span></span>
<span data-ttu-id="d87d7-152">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="d87d7-153">-확인</span><span class="sxs-lookup"><span data-stu-id="d87d7-153">-Confirm</span></span>
<span data-ttu-id="d87d7-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d87d7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87d7-155">-WhatIf</span></span>
<span data-ttu-id="d87d7-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d87d7-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d87d7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87d7-158">CommonParameters</span></span>
<span data-ttu-id="d87d7-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87d7-160">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d87d7-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87d7-161">입력</span><span class="sxs-lookup"><span data-stu-id="d87d7-161">INPUTS</span></span>

### <span data-ttu-id="d87d7-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d87d7-162">System.String</span></span>

### <span data-ttu-id="d87d7-163">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d87d7-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d87d7-164">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d87d7-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="d87d7-165">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d87d7-166">출력</span><span class="sxs-lookup"><span data-stu-id="d87d7-166">OUTPUTS</span></span>

### <span data-ttu-id="d87d7-167">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d87d7-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d87d7-168">상속자</span><span class="sxs-lookup"><span data-stu-id="d87d7-168">NOTES</span></span>

## <span data-ttu-id="d87d7-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d87d7-169">RELATED LINKS</span></span>
