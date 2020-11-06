---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531193"
---
# <span data-ttu-id="fe9b0-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="fe9b0-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="fe9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9b0-103">일괄 계산 노드에 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe9b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe9b0-104">SYNTAX</span></span>

### <span data-ttu-id="fe9b0-105">I</span><span class="sxs-lookup"><span data-stu-id="fe9b0-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe9b0-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="fe9b0-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe9b0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fe9b0-107">DESCRIPTION</span></span>
<span data-ttu-id="fe9b0-108">**AzureBatchComputeNodeUser** Cmdlet은 Azure Batch compute 노드에서 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="fe9b0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fe9b0-109">EXAMPLES</span></span>

### <span data-ttu-id="fe9b0-110">예제 1: 관리 자격 증명을 사용 하는 사용자 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fe9b0-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="fe9b0-111">이 명령은 ID ComputeNode01를 가진 계산 노드에 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="fe9b0-112">노드가 ID MyPool01를 가진 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="fe9b0-113">사용자 이름은 TestUser 비밀 번호, 계정이 7 일 후 만료 되며 계정에 관리 자격 증명이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="fe9b0-114">예제 2: 파이프라인을 사용 하 여 계산 노드에 사용자 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="fe9b0-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="fe9b0-115">이 명령은 **AzureBatchComputeNode** cmdlet을 사용 하 여 ComputeNode01 라는 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="fe9b0-116">해당 노드는 ID MyPool01가 있는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="fe9b0-117">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 대 한 계산 노드를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fe9b0-118">이 명령은 사용자 이름 TestUserand 암호 암호가 있는 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="fe9b0-119">변수</span><span class="sxs-lookup"><span data-stu-id="fe9b0-119">PARAMETERS</span></span>

### <span data-ttu-id="fe9b0-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fe9b0-120">-BatchContext</span></span>
<span data-ttu-id="fe9b0-121">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fe9b0-122">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fe9b0-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe9b0-123">-ComputeNode</span></span>
<span data-ttu-id="fe9b0-124">이 cmdlet에서 사용자 계정을 만드는 **PSComputeNode** 개체로 계산 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="fe9b0-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="fe9b0-125">-ComputeNodeId</span></span>
<span data-ttu-id="fe9b0-126">이 cmdlet에서 사용자 계정을 만드는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="fe9b0-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fe9b0-127">-ExpiryTime</span></span>
<span data-ttu-id="fe9b0-128">새 사용자 계정의 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="fe9b0-129">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="fe9b0-129">-IsAdmin</span></span>
<span data-ttu-id="fe9b0-130">Cmdlet에서 관리 자격 증명을 사용 하는 사용자 계정을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="fe9b0-131">-이름</span><span class="sxs-lookup"><span data-stu-id="fe9b0-131">-Name</span></span>
<span data-ttu-id="fe9b0-132">새 로컬 Windows 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="fe9b0-133">-암호</span><span class="sxs-lookup"><span data-stu-id="fe9b0-133">-Password</span></span>
<span data-ttu-id="fe9b0-134">사용자 계정 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="fe9b0-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="fe9b0-135">-PoolId</span></span>
<span data-ttu-id="fe9b0-136">사용자 계정을 만들 계산 노드가 포함 된 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="fe9b0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9b0-137">-DefaultProfile</span></span>
<span data-ttu-id="fe9b0-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9b0-139">CommonParameters</span></span>
<span data-ttu-id="fe9b0-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9b0-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9b0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9b0-142">입력</span><span class="sxs-lookup"><span data-stu-id="fe9b0-142">INPUTS</span></span>

### <span data-ttu-id="fe9b0-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fe9b0-143">BatchAccountContext</span></span>
<span data-ttu-id="fe9b0-144">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fe9b0-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe9b0-145">PSComputeNode</span></span>
<span data-ttu-id="fe9b0-146">' ComputeNode ' 매개 변수는 파이프라인에서 ' PSComputeNode ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe9b0-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="fe9b0-147">출력</span><span class="sxs-lookup"><span data-stu-id="fe9b0-147">OUTPUTS</span></span>

## <span data-ttu-id="fe9b0-148">상속자</span><span class="sxs-lookup"><span data-stu-id="fe9b0-148">NOTES</span></span>

## <span data-ttu-id="fe9b0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe9b0-149">RELATED LINKS</span></span>

[<span data-ttu-id="fe9b0-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fe9b0-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fe9b0-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="fe9b0-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="fe9b0-152">제거-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="fe9b0-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="fe9b0-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe9b0-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


