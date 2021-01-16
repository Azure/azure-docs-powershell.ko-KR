---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376125"
---
# <span data-ttu-id="99409-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="99409-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="99409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99409-102">SYNOPSIS</span></span>
<span data-ttu-id="99409-103">Storage 계정에서 지정된 개체 복제 정책을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="99409-104">구문</span><span class="sxs-lookup"><span data-stu-id="99409-104">SYNTAX</span></span>

### <span data-ttu-id="99409-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="99409-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99409-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="99409-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99409-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="99409-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99409-108">설명</span><span class="sxs-lookup"><span data-stu-id="99409-108">DESCRIPTION</span></span>
<span data-ttu-id="99409-109">**Set-AzStorageObjectReplicationPolicy** cmdlet은 Storage 계정에 지정된 개체 복제 정책을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="99409-110">예제</span><span class="sxs-lookup"><span data-stu-id="99409-110">EXAMPLES</span></span>

### <span data-ttu-id="99409-111">예제 1: 대상 및 원본 계정 모두에 개체 복제 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="99409-112">이 명령은 개체 복제 정책을 대상 및 원본 계정 모두로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="99409-113">먼저 2개 개체 복제 정책 규칙을 만들고 2개 규칙을 대상 계정에 설정하여 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="99409-114">그런 다음 대상 계정에서 원본 계정으로 개체 복제 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="99409-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99409-115">PARAMETERS</span></span>

### <span data-ttu-id="99409-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99409-116">-DefaultProfile</span></span>
<span data-ttu-id="99409-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99409-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99409-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="99409-118">-DestinationAccount</span></span>
<span data-ttu-id="99409-119">Object Replication Policy DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="99409-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99409-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99409-120">-InputObject</span></span>
<span data-ttu-id="99409-121">지정된 계정으로 설정할 개체 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="99409-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="99409-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="99409-122">-PolicyId</span></span>
<span data-ttu-id="99409-123">개체 복제 정책 ID입니다. GUID 또는 '기본값'입니다.</span><span class="sxs-lookup"><span data-stu-id="99409-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="99409-124">PolicyId를 입력하지 않는 경우 'default'를 사용하여 새 정책을 만들고 새 정책의 ID가 생성된 정책에 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="99409-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99409-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99409-125">-ResourceGroupName</span></span>
<span data-ttu-id="99409-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99409-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99409-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="99409-127">-Rule</span></span>
<span data-ttu-id="99409-128">개체 복제 정책 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="99409-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99409-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="99409-129">-SourceAccount</span></span>
<span data-ttu-id="99409-130">개체 복제 정책 SourceAccount.</span><span class="sxs-lookup"><span data-stu-id="99409-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="99409-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="99409-131">-StorageAccount</span></span>
<span data-ttu-id="99409-132">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="99409-132">Storage account object</span></span>

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

### <span data-ttu-id="99409-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="99409-133">-StorageAccountName</span></span>
<span data-ttu-id="99409-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99409-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99409-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99409-135">-Confirm</span></span>
<span data-ttu-id="99409-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99409-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99409-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99409-137">-WhatIf</span></span>
<span data-ttu-id="99409-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="99409-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99409-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99409-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99409-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99409-140">CommonParameters</span></span>
<span data-ttu-id="99409-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99409-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99409-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99409-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99409-143">입력</span><span class="sxs-lookup"><span data-stu-id="99409-143">INPUTS</span></span>

### <span data-ttu-id="99409-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="99409-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="99409-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="99409-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="99409-146">출력</span><span class="sxs-lookup"><span data-stu-id="99409-146">OUTPUTS</span></span>

### <span data-ttu-id="99409-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="99409-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="99409-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99409-148">NOTES</span></span>

## <span data-ttu-id="99409-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99409-149">RELATED LINKS</span></span>
