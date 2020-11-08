---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212054"
---
# <span data-ttu-id="5a7c8-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5a7c8-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="5a7c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7c8-103">저장소 계정에서 지정 된 개체 복제 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="5a7c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a7c8-104">SYNTAX</span></span>

### <span data-ttu-id="5a7c8-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a7c8-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a7c8-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="5a7c8-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a7c8-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5a7c8-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7c8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5a7c8-108">DESCRIPTION</span></span>
<span data-ttu-id="5a7c8-109">**Set-AzStorageObjectReplicationPolicy** Cmdlet은 저장소 계정에서 지정 된 개체 복제 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="5a7c8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5a7c8-110">EXAMPLES</span></span>

### <span data-ttu-id="5a7c8-111">예제 1: 대상 계정과 원본 계정 모두에 대해 개체 복제 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-111">Example 1: Set object replication policy to both destination and source account.</span></span>
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

<span data-ttu-id="5a7c8-112">이 명령은 개체 복제 정책을 대상과 원본 계정 모두로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="5a7c8-113">먼저 2 개의 개체 복제 정책 규칙을 만들고 두 개의 규칙이 있는 정책을 대상 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="5a7c8-114">그런 다음 대상 계정에서 원본 계정으로 개체 복제 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="5a7c8-115">변수</span><span class="sxs-lookup"><span data-stu-id="5a7c8-115">PARAMETERS</span></span>

### <span data-ttu-id="5a7c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7c8-116">-DefaultProfile</span></span>
<span data-ttu-id="5a7c8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7c8-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="5a7c8-118">-DestinationAccount</span></span>
<span data-ttu-id="5a7c8-119">개체 복제 정책 DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-119">Object Replication Policy DestinationAccount.</span></span>

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

### <span data-ttu-id="5a7c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a7c8-120">-InputObject</span></span>
<span data-ttu-id="5a7c8-121">지정 된 계정에 설정할 개체 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="5a7c8-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="5a7c8-122">-PolicyId</span></span>
<span data-ttu-id="5a7c8-123">개체 복제 정책 Id입니다. GUID 또는 ' default ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="5a7c8-124">PolicyId를 입력 하지 않으면 ' default '를 사용 하 여 새 정책을 만들고 새 정책의 Id가 생성 된 정책에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

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

### <span data-ttu-id="5a7c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a7c8-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="5a7c8-127">-규칙</span><span class="sxs-lookup"><span data-stu-id="5a7c8-127">-Rule</span></span>
<span data-ttu-id="5a7c8-128">개체 복제 정책 규칙</span><span class="sxs-lookup"><span data-stu-id="5a7c8-128">Object Replication Policy Rules.</span></span>

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

### <span data-ttu-id="5a7c8-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="5a7c8-129">-SourceAccount</span></span>
<span data-ttu-id="5a7c8-130">개체 복제 정책 원본 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="5a7c8-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a7c8-131">-StorageAccount</span></span>
<span data-ttu-id="5a7c8-132">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="5a7c8-132">Storage account object</span></span>

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

### <span data-ttu-id="5a7c8-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a7c8-133">-StorageAccountName</span></span>
<span data-ttu-id="5a7c8-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="5a7c8-135">-확인</span><span class="sxs-lookup"><span data-stu-id="5a7c8-135">-Confirm</span></span>
<span data-ttu-id="5a7c8-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7c8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7c8-137">-WhatIf</span></span>
<span data-ttu-id="5a7c8-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7c8-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7c8-140">CommonParameters</span></span>
<span data-ttu-id="5a7c8-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7c8-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7c8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7c8-143">입력</span><span class="sxs-lookup"><span data-stu-id="5a7c8-143">INPUTS</span></span>

### <span data-ttu-id="5a7c8-144">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a7c8-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5a7c8-145">PSObjectReplicationPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="5a7c8-146">출력</span><span class="sxs-lookup"><span data-stu-id="5a7c8-146">OUTPUTS</span></span>

### <span data-ttu-id="5a7c8-147">PSObjectReplicationPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7c8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="5a7c8-148">상속자</span><span class="sxs-lookup"><span data-stu-id="5a7c8-148">NOTES</span></span>

## <span data-ttu-id="5a7c8-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a7c8-149">RELATED LINKS</span></span>
