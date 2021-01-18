---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494673"
---
# <span data-ttu-id="07cf7-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07cf7-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="07cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="07cf7-103">Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="07cf7-104">구문</span><span class="sxs-lookup"><span data-stu-id="07cf7-104">SYNTAX</span></span>

### <span data-ttu-id="07cf7-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="07cf7-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="07cf7-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf7-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="07cf7-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07cf7-108">설명</span><span class="sxs-lookup"><span data-stu-id="07cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="07cf7-109">**Remove-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="07cf7-110">예제</span><span class="sxs-lookup"><span data-stu-id="07cf7-110">EXAMPLES</span></span>

### <span data-ttu-id="07cf7-111">예제 1: Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="07cf7-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="07cf7-112">이 명령은 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="07cf7-113">예제 2: Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="07cf7-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="07cf7-114">이 명령은 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="07cf7-115">예제 3: 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="07cf7-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="07cf7-116">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="07cf7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07cf7-117">PARAMETERS</span></span>

### <span data-ttu-id="07cf7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cf7-118">-DefaultProfile</span></span>
<span data-ttu-id="07cf7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07cf7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="07cf7-120">-Force</span></span>
<span data-ttu-id="07cf7-121">컨테이너 및 컨테이너의 모든 콘텐츠를 강제로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="07cf7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07cf7-122">-InputObject</span></span>
<span data-ttu-id="07cf7-123">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="07cf7-123">Storage container object</span></span>

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

### <span data-ttu-id="07cf7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="07cf7-124">-Name</span></span>
<span data-ttu-id="07cf7-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="07cf7-125">Container Name</span></span>

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

### <span data-ttu-id="07cf7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07cf7-126">-PassThru</span></span>
<span data-ttu-id="07cf7-127">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="07cf7-128">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="07cf7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07cf7-129">-ResourceGroupName</span></span>
<span data-ttu-id="07cf7-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="07cf7-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="07cf7-131">-StorageAccount</span></span>
<span data-ttu-id="07cf7-132">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="07cf7-132">Storage account object</span></span>

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

### <span data-ttu-id="07cf7-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07cf7-133">-StorageAccountName</span></span>
<span data-ttu-id="07cf7-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="07cf7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07cf7-135">-Confirm</span></span>
<span data-ttu-id="07cf7-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07cf7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07cf7-137">-WhatIf</span></span>
<span data-ttu-id="07cf7-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="07cf7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07cf7-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07cf7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cf7-140">CommonParameters</span></span>
<span data-ttu-id="07cf7-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07cf7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cf7-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07cf7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cf7-143">입력</span><span class="sxs-lookup"><span data-stu-id="07cf7-143">INPUTS</span></span>

### <span data-ttu-id="07cf7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="07cf7-144">System.String</span></span>

### <span data-ttu-id="07cf7-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07cf7-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="07cf7-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="07cf7-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="07cf7-147">출력</span><span class="sxs-lookup"><span data-stu-id="07cf7-147">OUTPUTS</span></span>

### <span data-ttu-id="07cf7-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07cf7-148">System.Boolean</span></span>

## <span data-ttu-id="07cf7-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07cf7-149">NOTES</span></span>

## <span data-ttu-id="07cf7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07cf7-150">RELATED LINKS</span></span>
