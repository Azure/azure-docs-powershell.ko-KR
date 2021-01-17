---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335157"
---
# <span data-ttu-id="fcdae-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fcdae-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="fcdae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcdae-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdae-103">Storage Blob 컨테이너 수정</span><span class="sxs-lookup"><span data-stu-id="fcdae-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="fcdae-104">구문</span><span class="sxs-lookup"><span data-stu-id="fcdae-104">SYNTAX</span></span>

### <span data-ttu-id="fcdae-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fcdae-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdae-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fcdae-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdae-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="fcdae-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcdae-108">설명</span><span class="sxs-lookup"><span data-stu-id="fcdae-108">DESCRIPTION</span></span>
<span data-ttu-id="fcdae-109">**Update-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="fcdae-110">예제</span><span class="sxs-lookup"><span data-stu-id="fcdae-110">EXAMPLES</span></span>

### <span data-ttu-id="fcdae-111">예제 1: Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너의 메타데이터 및 공용 액세스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="fcdae-112">이 명령은 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너의 메타데이터 및 공용 액세스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="fcdae-113">예제 2: Storage 계정 개체 및 컨테이너 이름을 통해 Storage Blob 컨테이너에서 공용 액세스를 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="fcdae-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="fcdae-114">이 명령은 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너에서 공용 액세스를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fcdae-115">예제 3: 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너에 대한 공용 액세스를 Blob으로 설정</span><span class="sxs-lookup"><span data-stu-id="fcdae-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="fcdae-116">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너에 대한 공용 액세스를 Blob으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="fcdae-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcdae-117">PARAMETERS</span></span>

### <span data-ttu-id="fcdae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdae-118">-DefaultProfile</span></span>
<span data-ttu-id="fcdae-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcdae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcdae-120">-InputObject</span></span>
<span data-ttu-id="fcdae-121">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="fcdae-121">Storage container object</span></span>

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

### <span data-ttu-id="fcdae-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fcdae-122">-Metadata</span></span>
<span data-ttu-id="fcdae-123">컨테이너 메타데이터</span><span class="sxs-lookup"><span data-stu-id="fcdae-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdae-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fcdae-124">-Name</span></span>
<span data-ttu-id="fcdae-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="fcdae-125">Container Name</span></span>

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

### <span data-ttu-id="fcdae-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fcdae-126">-PublicAccess</span></span>
<span data-ttu-id="fcdae-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fcdae-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcdae-128">-ResourceGroupName</span></span>
<span data-ttu-id="fcdae-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcdae-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdae-130">-StorageAccount</span></span>
<span data-ttu-id="fcdae-131">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="fcdae-131">Storage account object</span></span>

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

### <span data-ttu-id="fcdae-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fcdae-132">-StorageAccountName</span></span>
<span data-ttu-id="fcdae-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="fcdae-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcdae-134">-Confirm</span></span>
<span data-ttu-id="fcdae-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcdae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcdae-136">-WhatIf</span></span>
<span data-ttu-id="fcdae-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fcdae-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcdae-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcdae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdae-139">CommonParameters</span></span>
<span data-ttu-id="fcdae-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdae-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fcdae-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdae-142">입력</span><span class="sxs-lookup"><span data-stu-id="fcdae-142">INPUTS</span></span>

### <span data-ttu-id="fcdae-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fcdae-143">System.String</span></span>

### <span data-ttu-id="fcdae-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdae-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fcdae-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="fcdae-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fcdae-146">출력</span><span class="sxs-lookup"><span data-stu-id="fcdae-146">OUTPUTS</span></span>

### <span data-ttu-id="fcdae-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="fcdae-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fcdae-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fcdae-148">NOTES</span></span>

## <span data-ttu-id="fcdae-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcdae-149">RELATED LINKS</span></span>
