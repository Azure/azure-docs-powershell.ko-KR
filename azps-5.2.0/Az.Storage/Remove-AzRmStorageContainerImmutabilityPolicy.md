---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349401"
---
# <span data-ttu-id="f362d-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f362d-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="f362d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f362d-102">SYNOPSIS</span></span>
<span data-ttu-id="f362d-103">잠금 해제된 정책을 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="f362d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f362d-104">SYNTAX</span></span>

### <span data-ttu-id="f362d-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f362d-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f362d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f362d-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f362d-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="f362d-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f362d-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f362d-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f362d-109">설명</span><span class="sxs-lookup"><span data-stu-id="f362d-109">DESCRIPTION</span></span>
<span data-ttu-id="f362d-110">**Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet은 잠금 해제된 정책을 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="f362d-111">예제</span><span class="sxs-lookup"><span data-stu-id="f362d-111">EXAMPLES</span></span>

### <span data-ttu-id="f362d-112">예제 1: Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="f362d-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="f362d-113">이 명령은 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f362d-114">예제 2: Storage 계정 개체를 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="f362d-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="f362d-115">이 명령은 Storage 계정 개체를 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="f362d-116">예제 3: 컨테이너 개체를 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="f362d-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="f362d-117">이 명령은 Storage 컨테이너 개체를 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="f362d-118">예제 4: ImmutabilityPolicy 개체를 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="f362d-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="f362d-119">이 명령은 ImmutabilityPolicy 개체를 사용하여 Storage Blob 컨테이너의 잠금 해제된 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="f362d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f362d-120">PARAMETERS</span></span>

### <span data-ttu-id="f362d-121">-Container</span><span class="sxs-lookup"><span data-stu-id="f362d-121">-Container</span></span>
<span data-ttu-id="f362d-122">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="f362d-122">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f362d-123">-ContainerName</span></span>
<span data-ttu-id="f362d-124">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="f362d-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f362d-125">-DefaultProfile</span></span>
<span data-ttu-id="f362d-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f362d-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="f362d-127">-Etag</span></span>
<span data-ttu-id="f362d-128">몰입성 정책 etag입니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f362d-129">-InputObject</span></span>
<span data-ttu-id="f362d-130">제거할 잠금 해제된 ImmutabilityPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="f362d-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f362d-131">-ResourceGroupName</span></span>
<span data-ttu-id="f362d-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f362d-133">-StorageAccount</span></span>
<span data-ttu-id="f362d-134">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="f362d-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f362d-135">-StorageAccountName</span></span>
<span data-ttu-id="f362d-136">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f362d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f362d-137">-Confirm</span></span>
<span data-ttu-id="f362d-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f362d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f362d-139">-WhatIf</span></span>
<span data-ttu-id="f362d-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f362d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f362d-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f362d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f362d-142">CommonParameters</span></span>
<span data-ttu-id="f362d-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f362d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f362d-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f362d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f362d-145">입력</span><span class="sxs-lookup"><span data-stu-id="f362d-145">INPUTS</span></span>

### <span data-ttu-id="f362d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f362d-146">System.String</span></span>

### <span data-ttu-id="f362d-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f362d-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f362d-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="f362d-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="f362d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f362d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f362d-150">출력</span><span class="sxs-lookup"><span data-stu-id="f362d-150">OUTPUTS</span></span>

### <span data-ttu-id="f362d-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f362d-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f362d-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f362d-152">NOTES</span></span>

## <span data-ttu-id="f362d-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f362d-153">RELATED LINKS</span></span>
