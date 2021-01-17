---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491295"
---
# <span data-ttu-id="25e0b-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="25e0b-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="25e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="25e0b-103">Storage 계정에서 지정된 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="25e0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="25e0b-104">SYNTAX</span></span>

### <span data-ttu-id="25e0b-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="25e0b-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25e0b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="25e0b-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e0b-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="25e0b-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e0b-108">설명</span><span class="sxs-lookup"><span data-stu-id="25e0b-108">DESCRIPTION</span></span>
<span data-ttu-id="25e0b-109">**Remove-AzStorageObjectReplicationPolicy** cmdlet은 Storage 계정에서 지정된 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="25e0b-110">예제</span><span class="sxs-lookup"><span data-stu-id="25e0b-110">EXAMPLES</span></span>

### <span data-ttu-id="25e0b-111">예제 1: 저장소 계정에서 특정 policyId를 사용하여 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="25e0b-112">이 명령은 저장소 계정에서 특정 policyId를 사용하여 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="25e0b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e0b-113">PARAMETERS</span></span>

### <span data-ttu-id="25e0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e0b-114">-DefaultProfile</span></span>
<span data-ttu-id="25e0b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e0b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e0b-116">-InputObject</span></span>
<span data-ttu-id="25e0b-117">삭제할 개체 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e0b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e0b-118">-PassThru</span></span>
<span data-ttu-id="25e0b-119">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="25e0b-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="25e0b-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="25e0b-120">-PolicyId</span></span>
<span data-ttu-id="25e0b-121">개체 복제 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e0b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e0b-122">-ResourceGroupName</span></span>
<span data-ttu-id="25e0b-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e0b-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="25e0b-124">-StorageAccount</span></span>
<span data-ttu-id="25e0b-125">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="25e0b-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e0b-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25e0b-126">-StorageAccountName</span></span>
<span data-ttu-id="25e0b-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e0b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e0b-128">-Confirm</span></span>
<span data-ttu-id="25e0b-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e0b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e0b-130">-WhatIf</span></span>
<span data-ttu-id="25e0b-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25e0b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e0b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e0b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e0b-133">CommonParameters</span></span>
<span data-ttu-id="25e0b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25e0b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e0b-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25e0b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e0b-136">입력</span><span class="sxs-lookup"><span data-stu-id="25e0b-136">INPUTS</span></span>

### <span data-ttu-id="25e0b-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="25e0b-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="25e0b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="25e0b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="25e0b-139">출력</span><span class="sxs-lookup"><span data-stu-id="25e0b-139">OUTPUTS</span></span>

### <span data-ttu-id="25e0b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0b-140">System.Boolean</span></span>

## <span data-ttu-id="25e0b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25e0b-141">NOTES</span></span>

## <span data-ttu-id="25e0b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25e0b-142">RELATED LINKS</span></span>
