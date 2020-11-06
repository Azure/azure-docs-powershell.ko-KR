---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: c6a89a5c42daea7991711dfa0c96953856949aed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526283"
---
# <span data-ttu-id="438a3-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="438a3-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="438a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="438a3-102">SYNOPSIS</span></span>
<span data-ttu-id="438a3-103">일괄 처리 계산 노드의 계정 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="438a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="438a3-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="438a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="438a3-105">DESCRIPTION</span></span>
<span data-ttu-id="438a3-106">**AzureBatchComputeNodeUser** Cmdlet은 Azure 일괄 처리 계산 노드에서 사용자 계정의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="438a3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="438a3-107">EXAMPLES</span></span>

### <span data-ttu-id="438a3-108">예제 1: 사용자 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="438a3-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="438a3-109">이 명령은 ContosoPool 이라는 풀에서 지정 된 ID를 갖는 계산 노드에서 P_e 라는 이름의 사용자 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="438a3-110">이 명령은 계정 암호와 만료 시간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="438a3-111">변수</span><span class="sxs-lookup"><span data-stu-id="438a3-111">PARAMETERS</span></span>

### <span data-ttu-id="438a3-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="438a3-112">-BatchContext</span></span>
<span data-ttu-id="438a3-113">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="438a3-114">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="438a3-115">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="438a3-116">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="438a3-117">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="438a3-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="438a3-118">-ComputeNodeId</span></span>
<span data-ttu-id="438a3-119">이 cmdlet이 작동 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="438a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438a3-120">-DefaultProfile</span></span>
<span data-ttu-id="438a3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="438a3-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="438a3-122">-ExpiryTime</span></span>
<span data-ttu-id="438a3-123">사용자 계정에 대 한 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="438a3-124">-이름</span><span class="sxs-lookup"><span data-stu-id="438a3-124">-Name</span></span>
<span data-ttu-id="438a3-125">이 cmdlet이 수정 하는 사용자 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="438a3-126">-암호</span><span class="sxs-lookup"><span data-stu-id="438a3-126">-Password</span></span>
<span data-ttu-id="438a3-127">사용자 계정에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="438a3-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="438a3-128">-PoolId</span></span>
<span data-ttu-id="438a3-129">이 cmdlet이 작동 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="438a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438a3-130">CommonParameters</span></span>
<span data-ttu-id="438a3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="438a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438a3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438a3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438a3-133">입력</span><span class="sxs-lookup"><span data-stu-id="438a3-133">INPUTS</span></span>

### <span data-ttu-id="438a3-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="438a3-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="438a3-135">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="438a3-135">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="438a3-136">출력</span><span class="sxs-lookup"><span data-stu-id="438a3-136">OUTPUTS</span></span>

### <span data-ttu-id="438a3-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="438a3-137">System.Void</span></span>

## <span data-ttu-id="438a3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="438a3-138">NOTES</span></span>

## <span data-ttu-id="438a3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="438a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="438a3-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="438a3-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="438a3-141">새로운 AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="438a3-141">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="438a3-142">제거-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="438a3-142">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="438a3-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="438a3-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


