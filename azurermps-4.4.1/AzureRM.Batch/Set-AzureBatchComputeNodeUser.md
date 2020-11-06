---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531176"
---
# <span data-ttu-id="cd6e8-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cd6e8-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="cd6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6e8-103">일괄 처리 계산 노드의 계정 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd6e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd6e8-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd6e8-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6e8-106">**AzureBatchComputeNodeUser** Cmdlet은 Azure 일괄 처리 계산 노드에서 사용자 계정의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="cd6e8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd6e8-107">EXAMPLES</span></span>

### <span data-ttu-id="cd6e8-108">예제 1: 사용자 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="cd6e8-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="cd6e8-109">이 명령은 ContosoPool 이라는 풀에서 지정 된 ID를 갖는 계산 노드에서 P_e 라는 이름의 사용자 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="cd6e8-110">이 명령은 계정 암호와 만료 시간을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="cd6e8-111">변수</span><span class="sxs-lookup"><span data-stu-id="cd6e8-111">PARAMETERS</span></span>

### <span data-ttu-id="cd6e8-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cd6e8-112">-BatchContext</span></span>
<span data-ttu-id="cd6e8-113">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cd6e8-114">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="cd6e8-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="cd6e8-115">-ComputeNodeId</span></span>
<span data-ttu-id="cd6e8-116">이 cmdlet이 작동 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cd6e8-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cd6e8-117">-ExpiryTime</span></span>
<span data-ttu-id="cd6e8-118">사용자 계정에 대 한 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-118">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="cd6e8-119">-이름</span><span class="sxs-lookup"><span data-stu-id="cd6e8-119">-Name</span></span>
<span data-ttu-id="cd6e8-120">이 cmdlet이 수정 하는 사용자 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd6e8-121">-암호</span><span class="sxs-lookup"><span data-stu-id="cd6e8-121">-Password</span></span>
<span data-ttu-id="cd6e8-122">사용자 계정에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e8-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cd6e8-123">-PoolId</span></span>
<span data-ttu-id="cd6e8-124">이 cmdlet이 작동 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cd6e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6e8-125">-DefaultProfile</span></span>
<span data-ttu-id="cd6e8-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd6e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6e8-127">CommonParameters</span></span>
<span data-ttu-id="cd6e8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6e8-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6e8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6e8-130">입력</span><span class="sxs-lookup"><span data-stu-id="cd6e8-130">INPUTS</span></span>

### <span data-ttu-id="cd6e8-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cd6e8-131">BatchAccountContext</span></span>
<span data-ttu-id="cd6e8-132">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="cd6e8-133">출력</span><span class="sxs-lookup"><span data-stu-id="cd6e8-133">OUTPUTS</span></span>

## <span data-ttu-id="cd6e8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="cd6e8-134">NOTES</span></span>

## <span data-ttu-id="cd6e8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd6e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="cd6e8-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cd6e8-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cd6e8-137">새로운 AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cd6e8-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="cd6e8-138">제거-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cd6e8-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="cd6e8-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd6e8-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


