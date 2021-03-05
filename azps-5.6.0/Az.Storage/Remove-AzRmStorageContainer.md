---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 467fab7d2d7c344c3ffa2ca631addb538e790101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988717"
---
# <span data-ttu-id="cd552-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cd552-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="cd552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd552-102">SYNOPSIS</span></span>
<span data-ttu-id="cd552-103">Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="cd552-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="cd552-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd552-104">SYNTAX</span></span>

### <span data-ttu-id="cd552-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd552-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd552-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cd552-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd552-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="cd552-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd552-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd552-108">DESCRIPTION</span></span>
<span data-ttu-id="cd552-109">**Remove-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="cd552-110">예제</span><span class="sxs-lookup"><span data-stu-id="cd552-110">EXAMPLES</span></span>

### <span data-ttu-id="cd552-111">예제 1: Storage 계정 이름 및 컨테이너 이름으로 Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="cd552-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="cd552-112">이 명령은 Storage 계정 이름 및 컨테이너 이름이 있는 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="cd552-113">예제 2: Storage 계정 개체 및 컨테이너 이름으로 Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="cd552-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="cd552-114">이 명령은 Storage 계정 개체 및 컨테이너 이름이 있는 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="cd552-115">예제 3: 파이프라인을 사용하여 Storage 계정의 모든 Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="cd552-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="cd552-116">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="cd552-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd552-117">PARAMETERS</span></span>

### <span data-ttu-id="cd552-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd552-118">-DefaultProfile</span></span>
<span data-ttu-id="cd552-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd552-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cd552-120">-Force</span></span>
<span data-ttu-id="cd552-121">컨테이너 및 해당 컨테이너의 모든 콘텐츠를 제거하려면 강제로</span><span class="sxs-lookup"><span data-stu-id="cd552-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd552-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd552-122">-InputObject</span></span>
<span data-ttu-id="cd552-123">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="cd552-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd552-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cd552-124">-Name</span></span>
<span data-ttu-id="cd552-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="cd552-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd552-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd552-126">-PassThru</span></span>
<span data-ttu-id="cd552-127">이 cmdlet은 작업의 성공을 반영하는 **부울을** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cd552-128">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cd552-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd552-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd552-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd552-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd552-131">-StorageAccount</span></span>
<span data-ttu-id="cd552-132">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="cd552-132">Storage account object</span></span>

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

### <span data-ttu-id="cd552-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd552-133">-StorageAccountName</span></span>
<span data-ttu-id="cd552-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="cd552-135">-확인</span><span class="sxs-lookup"><span data-stu-id="cd552-135">-Confirm</span></span>
<span data-ttu-id="cd552-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd552-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd552-137">-WhatIf</span></span>
<span data-ttu-id="cd552-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd552-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd552-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd552-140">CommonParameters</span></span>
<span data-ttu-id="cd552-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd552-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd552-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd552-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd552-143">입력</span><span class="sxs-lookup"><span data-stu-id="cd552-143">INPUTS</span></span>

### <span data-ttu-id="cd552-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cd552-144">System.String</span></span>

### <span data-ttu-id="cd552-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd552-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cd552-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="cd552-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="cd552-147">출력</span><span class="sxs-lookup"><span data-stu-id="cd552-147">OUTPUTS</span></span>

### <span data-ttu-id="cd552-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd552-148">System.Boolean</span></span>

## <span data-ttu-id="cd552-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd552-149">NOTES</span></span>

## <span data-ttu-id="cd552-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd552-150">RELATED LINKS</span></span>
