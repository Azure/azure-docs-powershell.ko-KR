---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: c76c10d282d7a2b50cf0b35793cdda080d944740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004624"
---
# <span data-ttu-id="376b5-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="376b5-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="376b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="376b5-102">SYNOPSIS</span></span>
<span data-ttu-id="376b5-103">Batch 계산 노드에서 계정 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="376b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="376b5-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="376b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="376b5-105">DESCRIPTION</span></span>
<span data-ttu-id="376b5-106">**Set-AzBatchComputeNodeUser** cmdlet은 Azure Batch 계산 노드에서 사용자 계정의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="376b5-107">예제</span><span class="sxs-lookup"><span data-stu-id="376b5-107">EXAMPLES</span></span>

### <span data-ttu-id="376b5-108">예제 1: 사용자 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="376b5-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="376b5-109">이 명령은 ContosoPool이라는 풀에 지정된 ID가 있는 계산 노드에서 PFuller라는 사용자 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="376b5-110">명령은 계정 암호 및 만료 시간을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="376b5-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="376b5-111">PARAMETERS</span></span>

### <span data-ttu-id="376b5-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="376b5-112">-BatchContext</span></span>
<span data-ttu-id="376b5-113">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="376b5-114">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="376b5-115">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="376b5-116">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="376b5-117">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="376b5-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="376b5-118">-ComputeNodeId</span></span>
<span data-ttu-id="376b5-119">이 cmdlet이 작동하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376b5-120">-DefaultProfile</span></span>
<span data-ttu-id="376b5-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="376b5-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="376b5-122">-ExpiryTime</span></span>
<span data-ttu-id="376b5-123">사용자 계정에 대한 만료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="376b5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="376b5-124">-Name</span></span>
<span data-ttu-id="376b5-125">이 cmdlet이 수정하는 사용자 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b5-126">-Password</span><span class="sxs-lookup"><span data-stu-id="376b5-126">-Password</span></span>
<span data-ttu-id="376b5-127">사용자 계정에 대한 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b5-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="376b5-128">-PoolId</span></span>
<span data-ttu-id="376b5-129">이 cmdlet이 작동하는 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376b5-130">CommonParameters</span></span>
<span data-ttu-id="376b5-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="376b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376b5-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="376b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376b5-133">입력</span><span class="sxs-lookup"><span data-stu-id="376b5-133">INPUTS</span></span>

### <span data-ttu-id="376b5-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="376b5-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="376b5-135">출력</span><span class="sxs-lookup"><span data-stu-id="376b5-135">OUTPUTS</span></span>

### <span data-ttu-id="376b5-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="376b5-136">System.Void</span></span>

## <span data-ttu-id="376b5-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="376b5-137">NOTES</span></span>

## <span data-ttu-id="376b5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="376b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="376b5-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="376b5-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="376b5-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="376b5-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="376b5-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="376b5-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="376b5-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="376b5-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
