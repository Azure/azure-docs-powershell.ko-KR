---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 17ccb6e41e826ffd6b522c353ff51cf360b5af0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961323"
---
# <span data-ttu-id="7b6b9-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7b6b9-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="7b6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6b9-103">Storage 계정에서 지정된 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="7b6b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b6b9-104">SYNTAX</span></span>

### <span data-ttu-id="7b6b9-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7b6b9-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b6b9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7b6b9-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b6b9-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="7b6b9-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b6b9-108">설명</span><span class="sxs-lookup"><span data-stu-id="7b6b9-108">DESCRIPTION</span></span>
<span data-ttu-id="7b6b9-109">**Remove-AzStorageObjectReplicationPolicy** cmdlet은 Storage 계정에서 지정된 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="7b6b9-110">예제</span><span class="sxs-lookup"><span data-stu-id="7b6b9-110">EXAMPLES</span></span>

### <span data-ttu-id="7b6b9-111">예제 1: 저장소 계정에서 특정 policyId를 사용하여 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="7b6b9-112">이 명령은 저장소 계정에서 특정 policyId를 사용하여 개체 복제 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="7b6b9-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b6b9-113">PARAMETERS</span></span>

### <span data-ttu-id="7b6b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6b9-114">-DefaultProfile</span></span>
<span data-ttu-id="7b6b9-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b6b9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b6b9-116">-InputObject</span></span>
<span data-ttu-id="7b6b9-117">삭제할 개체 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="7b6b9-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b6b9-118">-PassThru</span></span>
<span data-ttu-id="7b6b9-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7b6b9-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7b6b9-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="7b6b9-120">-PolicyId</span></span>
<span data-ttu-id="7b6b9-121">개체 복제 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="7b6b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b6b9-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b6b9-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b6b9-124">-StorageAccount</span></span>
<span data-ttu-id="7b6b9-125">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="7b6b9-125">Storage account object</span></span>

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

### <span data-ttu-id="7b6b9-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7b6b9-126">-StorageAccountName</span></span>
<span data-ttu-id="7b6b9-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="7b6b9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="7b6b9-128">-Confirm</span></span>
<span data-ttu-id="7b6b9-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b6b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6b9-130">-WhatIf</span></span>
<span data-ttu-id="7b6b9-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b6b9-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b6b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6b9-133">CommonParameters</span></span>
<span data-ttu-id="7b6b9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6b9-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b6b9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6b9-136">입력</span><span class="sxs-lookup"><span data-stu-id="7b6b9-136">INPUTS</span></span>

### <span data-ttu-id="7b6b9-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b6b9-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7b6b9-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7b6b9-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="7b6b9-139">출력</span><span class="sxs-lookup"><span data-stu-id="7b6b9-139">OUTPUTS</span></span>

### <span data-ttu-id="7b6b9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b6b9-140">System.Boolean</span></span>

## <span data-ttu-id="7b6b9-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b6b9-141">NOTES</span></span>

## <span data-ttu-id="7b6b9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b6b9-142">RELATED LINKS</span></span>
