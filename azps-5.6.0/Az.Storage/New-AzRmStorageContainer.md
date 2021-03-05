---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: c85b482ff077263d20ae770e6ec6d91b497153e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994756"
---
# <span data-ttu-id="e5f80-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e5f80-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="e5f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f80-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f80-103">Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="e5f80-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5f80-104">SYNTAX</span></span>

### <span data-ttu-id="e5f80-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5f80-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f80-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e5f80-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f80-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e5f80-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f80-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e5f80-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f80-109">설명</span><span class="sxs-lookup"><span data-stu-id="e5f80-109">DESCRIPTION</span></span>
<span data-ttu-id="e5f80-110">**New-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="e5f80-111">예제</span><span class="sxs-lookup"><span data-stu-id="e5f80-111">EXAMPLES</span></span>

### <span data-ttu-id="e5f80-112">예제 1: 메타데이터를 사용하여 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="e5f80-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="e5f80-113">이 명령은 메타데이터를 사용하여 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="e5f80-114">예제 2: Blob으로 공용 액세스가 있는 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="e5f80-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="e5f80-115">이 명령은 공용 액세스를 Blob으로 사용하여 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="e5f80-116">예제 3: EncryptionScope 설정을 사용하여 저장소 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="e5f80-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="e5f80-117">이 명령은 디폴트 암호화Scope를 사용하여 저장소 컨테이너를 만들고, 컨테이너 기본값에서 암호화 범위를 오버라이드하는 것을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="e5f80-118">그런 다음 관련 컨테이너 속성을 보여 웁니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-118">Then show the related container properties.</span></span>

## <span data-ttu-id="e5f80-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5f80-119">PARAMETERS</span></span>

### <span data-ttu-id="e5f80-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="e5f80-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="e5f80-121">모든 쓰기에 대해 지정된 암호화 범위를 사용하기 위해 컨테이너를 기본값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f80-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f80-122">-DefaultProfile</span></span>
<span data-ttu-id="e5f80-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5f80-124">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="e5f80-124">-Metadata</span></span>
<span data-ttu-id="e5f80-125">컨테이너 메타데이터</span><span class="sxs-lookup"><span data-stu-id="e5f80-125">Container Metadata</span></span>

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

### <span data-ttu-id="e5f80-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e5f80-126">-Name</span></span>
<span data-ttu-id="e5f80-127">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="e5f80-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f80-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="e5f80-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="e5f80-129">컨테이너 기본값에서 암호화 범위의 오버라이드를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f80-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="e5f80-130">-PublicAccess</span></span>
<span data-ttu-id="e5f80-131">Container PublicAccesss</span><span class="sxs-lookup"><span data-stu-id="e5f80-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="e5f80-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f80-132">-ResourceGroupName</span></span>
<span data-ttu-id="e5f80-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f80-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5f80-134">-StorageAccount</span></span>
<span data-ttu-id="e5f80-135">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="e5f80-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f80-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5f80-136">-StorageAccountName</span></span>
<span data-ttu-id="e5f80-137">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f80-138">-확인</span><span class="sxs-lookup"><span data-stu-id="e5f80-138">-Confirm</span></span>
<span data-ttu-id="e5f80-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f80-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f80-140">-WhatIf</span></span>
<span data-ttu-id="e5f80-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5f80-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f80-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f80-143">CommonParameters</span></span>
<span data-ttu-id="e5f80-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f80-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f80-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e5f80-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f80-146">입력</span><span class="sxs-lookup"><span data-stu-id="e5f80-146">INPUTS</span></span>

### <span data-ttu-id="e5f80-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e5f80-147">System.String</span></span>

### <span data-ttu-id="e5f80-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5f80-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e5f80-149">출력</span><span class="sxs-lookup"><span data-stu-id="e5f80-149">OUTPUTS</span></span>

### <span data-ttu-id="e5f80-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="e5f80-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e5f80-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5f80-151">NOTES</span></span>

## <span data-ttu-id="e5f80-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5f80-152">RELATED LINKS</span></span>
