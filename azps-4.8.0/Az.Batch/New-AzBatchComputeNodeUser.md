---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5695f0bf0a7cc65b1eb032be33116cc40ec0618e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049197"
---
# <span data-ttu-id="d1ec2-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="d1ec2-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="d1ec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ec2-103">일괄 계산 노드에 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="d1ec2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1ec2-104">SYNTAX</span></span>

### <span data-ttu-id="d1ec2-105">I</span><span class="sxs-lookup"><span data-stu-id="d1ec2-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1ec2-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1ec2-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1ec2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ec2-108">**AzBatchComputeNodeUser** Cmdlet은 Azure Batch compute 노드에서 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="d1ec2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d1ec2-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ec2-110">예제 1: 관리 자격 증명을 사용 하는 사용자 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="d1ec2-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="d1ec2-111">이 명령은 ID ComputeNode01를 가진 계산 노드에 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="d1ec2-112">노드가 ID MyPool01를 가진 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="d1ec2-113">사용자 이름은 TestUser 비밀 번호, 계정이 7 일 후 만료 되며 계정에 관리 자격 증명이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="d1ec2-114">예제 2: 파이프라인을 사용 하 여 계산 노드에 사용자 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="d1ec2-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="d1ec2-115">이 명령은 **AzBatchComputeNode** cmdlet을 사용 하 여 ComputeNode01 라는 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="d1ec2-116">해당 노드는 ID MyPool01가 있는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="d1ec2-117">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 대 한 계산 노드를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d1ec2-118">이 명령은 사용자 이름 TestUser와 암호 암호가 있는 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="d1ec2-119">변수</span><span class="sxs-lookup"><span data-stu-id="d1ec2-119">PARAMETERS</span></span>

### <span data-ttu-id="d1ec2-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d1ec2-120">-BatchContext</span></span>
<span data-ttu-id="d1ec2-121">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d1ec2-122">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d1ec2-123">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d1ec2-124">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d1ec2-125">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d1ec2-126">-ComputeNode</span></span>
<span data-ttu-id="d1ec2-127">이 cmdlet에서 사용자 계정을 만드는 **PSComputeNode** 개체로 계산 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-128">-ComputeNodeId</span></span>
<span data-ttu-id="d1ec2-129">이 cmdlet에서 사용자 계정을 만드는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ec2-130">-DefaultProfile</span></span>
<span data-ttu-id="d1ec2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ec2-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d1ec2-132">-ExpiryTime</span></span>
<span data-ttu-id="d1ec2-133">새 사용자 계정의 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="d1ec2-134">-IsAdmin</span></span>
<span data-ttu-id="d1ec2-135">Cmdlet에서 관리 자격 증명을 사용 하는 사용자 계정을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="d1ec2-136">-이름</span><span class="sxs-lookup"><span data-stu-id="d1ec2-136">-Name</span></span>
<span data-ttu-id="d1ec2-137">새 로컬 Windows 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-138">-암호</span><span class="sxs-lookup"><span data-stu-id="d1ec2-138">-Password</span></span>
<span data-ttu-id="d1ec2-139">사용자 계정 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-140">-PoolId</span></span>
<span data-ttu-id="d1ec2-141">사용자 계정을 만들 계산 노드가 포함 된 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ec2-142">CommonParameters</span></span>
<span data-ttu-id="d1ec2-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ec2-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ec2-145">입력</span><span class="sxs-lookup"><span data-stu-id="d1ec2-145">INPUTS</span></span>

### <span data-ttu-id="d1ec2-146">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d1ec2-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d1ec2-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d1ec2-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d1ec2-148">출력</span><span class="sxs-lookup"><span data-stu-id="d1ec2-148">OUTPUTS</span></span>

### <span data-ttu-id="d1ec2-149">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d1ec2-149">System.Void</span></span>

## <span data-ttu-id="d1ec2-150">상속자</span><span class="sxs-lookup"><span data-stu-id="d1ec2-150">NOTES</span></span>

## <span data-ttu-id="d1ec2-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1ec2-151">RELATED LINKS</span></span>

[<span data-ttu-id="d1ec2-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d1ec2-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d1ec2-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d1ec2-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d1ec2-154">제거-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="d1ec2-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="d1ec2-155">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d1ec2-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
