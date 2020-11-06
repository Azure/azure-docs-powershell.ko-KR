---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 8c9b48046393a55bc0d37e0fe6d08361dcf04246
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531770"
---
# <span data-ttu-id="e8260-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="e8260-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="e8260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8260-102">SYNOPSIS</span></span>
<span data-ttu-id="e8260-103">일괄 처리 계정에서 사용할 수 있는 일괄 처리 노드 에이전트 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8260-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8260-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8260-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8260-105">DESCRIPTION</span></span>
<span data-ttu-id="e8260-106">**Get-AzureBatchNodeAgentSku** Cmdlet은 Azure Batch 계정에서 사용할 수 있는 노드 에이전트 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="e8260-107">*Batchcontext* 매개 변수를 사용 하 여 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="e8260-108">OData (Open Data Protocol) 필터와 일치 하는 Sku에 대 한 검색 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e8260-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e8260-109">EXAMPLES</span></span>

### <span data-ttu-id="e8260-110">예제 1: 사용 가능한 모든 노드 에이전트 Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="e8260-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="e8260-111">첫 번째 명령은 **AzureRmBatchAccountKeys** 를 사용 하 여 구독에 대 한 선택 키를 포함 하는 일괄 처리 계정 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="e8260-112">명령은 다음 명령에 사용할 컨텍스트를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="e8260-113">두 번째 명령은 일괄 처리에서 지 원하는 사용 가능한 모든 노드 에이전트 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="e8260-114">변수</span><span class="sxs-lookup"><span data-stu-id="e8260-114">PARAMETERS</span></span>

### <span data-ttu-id="e8260-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e8260-115">-BatchContext</span></span>
<span data-ttu-id="e8260-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e8260-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e8260-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e8260-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e8260-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8260-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8260-121">-DefaultProfile</span></span>
<span data-ttu-id="e8260-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8260-123">-필터</span><span class="sxs-lookup"><span data-stu-id="e8260-123">-Filter</span></span>
<span data-ttu-id="e8260-124">노드 에이전트 Sku에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="e8260-125">필터를 지정 하지 않으면이 cmdlet은 일괄 처리에서 지 원하는 모든 노드 에이전트 Sku를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8260-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e8260-126">-MaxCount</span></span>
<span data-ttu-id="e8260-127">반환할 노드 에이전트 Sku의 최대 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-127">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8260-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8260-128">CommonParameters</span></span>
<span data-ttu-id="e8260-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8260-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8260-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8260-131">입력</span><span class="sxs-lookup"><span data-stu-id="e8260-131">INPUTS</span></span>

### <span data-ttu-id="e8260-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e8260-132">BatchAccountContext</span></span>
<span data-ttu-id="e8260-133">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8260-133">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="e8260-134">출력</span><span class="sxs-lookup"><span data-stu-id="e8260-134">OUTPUTS</span></span>

### <span data-ttu-id="e8260-135">Microsoft.Azure.Commands.Batch. PSNodeAgentSku에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="e8260-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="e8260-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e8260-136">NOTES</span></span>

## <span data-ttu-id="e8260-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8260-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8260-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e8260-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


