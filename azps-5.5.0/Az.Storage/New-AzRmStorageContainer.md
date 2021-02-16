---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197561"
---
# <span data-ttu-id="883f0-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="883f0-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="883f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="883f0-102">SYNOPSIS</span></span>
<span data-ttu-id="883f0-103">Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="883f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="883f0-104">SYNTAX</span></span>

### <span data-ttu-id="883f0-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="883f0-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883f0-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="883f0-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883f0-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="883f0-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883f0-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="883f0-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="883f0-109">설명</span><span class="sxs-lookup"><span data-stu-id="883f0-109">DESCRIPTION</span></span>
<span data-ttu-id="883f0-110">**New-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="883f0-111">예제</span><span class="sxs-lookup"><span data-stu-id="883f0-111">EXAMPLES</span></span>

### <span data-ttu-id="883f0-112">예제 1: 메타데이터를 사용하여 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="883f0-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="883f0-113">이 명령은 메타데이터를 사용하여 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="883f0-114">예제 2: Blob으로 공용 액세스가 있는 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="883f0-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="883f0-115">이 명령은 공용 액세스를 Blob으로 사용하여 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="883f0-116">예제 3: EncryptionScope 설정을 사용하여 저장소 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="883f0-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
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

<span data-ttu-id="883f0-117">이 명령은 defalt encryptionScope를 사용하여 저장소 컨테이너를 만들고, 컨테이너 기본값에서 암호화 범위를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="883f0-118">그런 다음 관련 컨테이너 속성을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="883f0-118">Then show the related container properties.</span></span>

## <span data-ttu-id="883f0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="883f0-119">PARAMETERS</span></span>

### <span data-ttu-id="883f0-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="883f0-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="883f0-121">기본적으로 컨테이너는 모든 쓰기에 대해 지정된 암호화 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-121">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="883f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883f0-122">-DefaultProfile</span></span>
<span data-ttu-id="883f0-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="883f0-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="883f0-124">-Metadata</span></span>
<span data-ttu-id="883f0-125">컨테이너 메타데이터</span><span class="sxs-lookup"><span data-stu-id="883f0-125">Container Metadata</span></span>

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

### <span data-ttu-id="883f0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="883f0-126">-Name</span></span>
<span data-ttu-id="883f0-127">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="883f0-127">Container Name</span></span>

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

### <span data-ttu-id="883f0-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="883f0-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="883f0-129">컨테이너 기본값에서 암호화 범위를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-129">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="883f0-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="883f0-130">-PublicAccess</span></span>
<span data-ttu-id="883f0-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="883f0-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="883f0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883f0-132">-ResourceGroupName</span></span>
<span data-ttu-id="883f0-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="883f0-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="883f0-134">-StorageAccount</span></span>
<span data-ttu-id="883f0-135">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="883f0-135">Storage account object</span></span>

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

### <span data-ttu-id="883f0-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="883f0-136">-StorageAccountName</span></span>
<span data-ttu-id="883f0-137">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="883f0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="883f0-138">-Confirm</span></span>
<span data-ttu-id="883f0-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883f0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883f0-140">-WhatIf</span></span>
<span data-ttu-id="883f0-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="883f0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="883f0-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883f0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883f0-143">CommonParameters</span></span>
<span data-ttu-id="883f0-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="883f0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883f0-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="883f0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883f0-146">입력</span><span class="sxs-lookup"><span data-stu-id="883f0-146">INPUTS</span></span>

### <span data-ttu-id="883f0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="883f0-147">System.String</span></span>

### <span data-ttu-id="883f0-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="883f0-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="883f0-149">출력</span><span class="sxs-lookup"><span data-stu-id="883f0-149">OUTPUTS</span></span>

### <span data-ttu-id="883f0-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="883f0-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="883f0-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="883f0-151">NOTES</span></span>

## <span data-ttu-id="883f0-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="883f0-152">RELATED LINKS</span></span>
