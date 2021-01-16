---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349526"
---
# <span data-ttu-id="127d4-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="127d4-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="127d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="127d4-102">SYNOPSIS</span></span>
<span data-ttu-id="127d4-103">Storage Blob 컨테이너의 ImmutabilityPolicy 잠금</span><span class="sxs-lookup"><span data-stu-id="127d4-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="127d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="127d4-104">SYNTAX</span></span>

### <span data-ttu-id="127d4-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="127d4-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127d4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="127d4-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127d4-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="127d4-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127d4-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="127d4-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="127d4-109">설명</span><span class="sxs-lookup"><span data-stu-id="127d4-109">DESCRIPTION</span></span>
<span data-ttu-id="127d4-110">**Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet은 Storage Blob 컨테이너의 ImmutabilityPolicy를 잠급습니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="127d4-111">예제</span><span class="sxs-lookup"><span data-stu-id="127d4-111">EXAMPLES</span></span>

### <span data-ttu-id="127d4-112">예제 1: Storage 계정 이름 및 컨테이너 이름으로 Storage Blob 컨테이너의 ImmutabilityPolicy 잠금</span><span class="sxs-lookup"><span data-stu-id="127d4-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="127d4-113">이 명령은 Storage 계정 이름 및 컨테이너 이름으로 Storage Blob 컨테이너의 ImmutabilityPolicy를 잠글 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="127d4-114">예제 2: Storage 계정 개체를 통해 Storage Blob 컨테이너의 ImmutabilityPolicy 잠금</span><span class="sxs-lookup"><span data-stu-id="127d4-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="127d4-115">이 명령은 Storage 계정 개체를 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 잠글 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="127d4-116">예제 3: 컨테이너 개체를 통해 Storage Blob 컨테이너에 ImmutabilityPolicyof 잠금</span><span class="sxs-lookup"><span data-stu-id="127d4-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="127d4-117">이 명령은 Storage 컨테이너 개체를 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 잠글 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="127d4-118">예제 4: ImmutabilityPolicy 개체를 통해 Storage Blob 컨테이너의 ImmutabilityPolicy 잠금</span><span class="sxs-lookup"><span data-stu-id="127d4-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="127d4-119">이 명령은 ImmutabilityPolicy 개체를 사용하여 Storage Blob 컨테이너의 ImmutabilityPolicy를 잠글 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="127d4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="127d4-120">PARAMETERS</span></span>

### <span data-ttu-id="127d4-121">-Container</span><span class="sxs-lookup"><span data-stu-id="127d4-121">-Container</span></span>
<span data-ttu-id="127d4-122">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="127d4-122">Storage container object</span></span>

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

### <span data-ttu-id="127d4-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="127d4-123">-ContainerName</span></span>
<span data-ttu-id="127d4-124">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="127d4-124">Container Name</span></span>

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

### <span data-ttu-id="127d4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127d4-125">-DefaultProfile</span></span>
<span data-ttu-id="127d4-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="127d4-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="127d4-127">-Etag</span></span>
<span data-ttu-id="127d4-128">몰입성 정책 etag입니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="127d4-129">-Force</span><span class="sxs-lookup"><span data-stu-id="127d4-129">-Force</span></span>
<span data-ttu-id="127d4-130">강제로 ImmutabilityPolicy를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="127d4-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="127d4-131">-InputObject</span></span>
<span data-ttu-id="127d4-132">제거할 ImmutabilityPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="127d4-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="127d4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127d4-133">-ResourceGroupName</span></span>
<span data-ttu-id="127d4-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="127d4-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="127d4-135">-StorageAccount</span></span>
<span data-ttu-id="127d4-136">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="127d4-136">Storage account object</span></span>

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

### <span data-ttu-id="127d4-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="127d4-137">-StorageAccountName</span></span>
<span data-ttu-id="127d4-138">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="127d4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="127d4-139">-Confirm</span></span>
<span data-ttu-id="127d4-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127d4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127d4-141">-WhatIf</span></span>
<span data-ttu-id="127d4-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="127d4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="127d4-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127d4-144">CommonParameters</span></span>
<span data-ttu-id="127d4-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="127d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127d4-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="127d4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127d4-147">입력</span><span class="sxs-lookup"><span data-stu-id="127d4-147">INPUTS</span></span>

### <span data-ttu-id="127d4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="127d4-148">System.String</span></span>

### <span data-ttu-id="127d4-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="127d4-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="127d4-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="127d4-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="127d4-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="127d4-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="127d4-152">출력</span><span class="sxs-lookup"><span data-stu-id="127d4-152">OUTPUTS</span></span>

### <span data-ttu-id="127d4-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="127d4-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="127d4-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="127d4-154">NOTES</span></span>

## <span data-ttu-id="127d4-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="127d4-155">RELATED LINKS</span></span>
