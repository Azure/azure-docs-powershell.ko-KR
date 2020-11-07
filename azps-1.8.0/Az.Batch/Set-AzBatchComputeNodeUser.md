---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 95530c75575742e848f39861bed1710be75e318c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93701828"
---
# <span data-ttu-id="66868-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="66868-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="66868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66868-102">SYNOPSIS</span></span>
<span data-ttu-id="66868-103">일괄 처리 계산 노드의 계정 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="66868-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66868-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66868-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66868-105">DESCRIPTION</span></span>
<span data-ttu-id="66868-106">**AzBatchComputeNodeUser** Cmdlet은 Azure 일괄 처리 계산 노드에서 사용자 계정의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="66868-107">예제의</span><span class="sxs-lookup"><span data-stu-id="66868-107">EXAMPLES</span></span>

### <span data-ttu-id="66868-108">예제 1: 사용자 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="66868-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="66868-109">이 명령은 ContosoPool 이라는 풀에서 지정 된 ID를 갖는 계산 노드에서 P_e 라는 이름의 사용자 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="66868-110">이 명령은 계정 암호와 만료 시간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="66868-111">변수</span><span class="sxs-lookup"><span data-stu-id="66868-111">PARAMETERS</span></span>

### <span data-ttu-id="66868-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="66868-112">-BatchContext</span></span>
<span data-ttu-id="66868-113">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="66868-114">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66868-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="66868-115">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="66868-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="66868-116">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66868-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="66868-117">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="66868-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="66868-118">-ComputeNodeId</span></span>
<span data-ttu-id="66868-119">이 cmdlet이 작동 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="66868-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66868-120">-DefaultProfile</span></span>
<span data-ttu-id="66868-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66868-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66868-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="66868-122">-ExpiryTime</span></span>
<span data-ttu-id="66868-123">사용자 계정에 대 한 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="66868-124">-이름</span><span class="sxs-lookup"><span data-stu-id="66868-124">-Name</span></span>
<span data-ttu-id="66868-125">이 cmdlet이 수정 하는 사용자 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66868-126">-암호</span><span class="sxs-lookup"><span data-stu-id="66868-126">-Password</span></span>
<span data-ttu-id="66868-127">사용자 계정에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="66868-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="66868-128">-PoolId</span></span>
<span data-ttu-id="66868-129">이 cmdlet이 작동 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="66868-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66868-130">CommonParameters</span></span>
<span data-ttu-id="66868-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66868-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66868-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66868-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66868-133">입력</span><span class="sxs-lookup"><span data-stu-id="66868-133">INPUTS</span></span>

### <span data-ttu-id="66868-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66868-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="66868-135">출력</span><span class="sxs-lookup"><span data-stu-id="66868-135">OUTPUTS</span></span>

### <span data-ttu-id="66868-136">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="66868-136">System.Void</span></span>

## <span data-ttu-id="66868-137">상속자</span><span class="sxs-lookup"><span data-stu-id="66868-137">NOTES</span></span>

## <span data-ttu-id="66868-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66868-138">RELATED LINKS</span></span>

[<span data-ttu-id="66868-139">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="66868-139">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="66868-140">새로운 AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="66868-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="66868-141">제거-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="66868-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="66868-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66868-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


