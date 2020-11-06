---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538035"
---
# <span data-ttu-id="ccaa8-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ccaa8-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="ccaa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccaa8-102">SYNOPSIS</span></span>
<span data-ttu-id="ccaa8-103">풀의 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccaa8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccaa8-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccaa8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ccaa8-105">DESCRIPTION</span></span>
<span data-ttu-id="ccaa8-106">**Disable-AzureBatchAutoScale 크기 조정** cmdlet은 지정 된 풀의 자동 크기 조정을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="ccaa8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ccaa8-107">EXAMPLES</span></span>

### <span data-ttu-id="ccaa8-108">예제 1: 풀의 자동 크기 조정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ccaa8-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="ccaa8-109">이 명령은 MyPool 이라는 풀에 대해 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="ccaa8-110">변수</span><span class="sxs-lookup"><span data-stu-id="ccaa8-110">PARAMETERS</span></span>

### <span data-ttu-id="ccaa8-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ccaa8-111">-BatchContext</span></span>
<span data-ttu-id="ccaa8-112">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ccaa8-113">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ccaa8-114">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ccaa8-115">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ccaa8-116">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ccaa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccaa8-117">-DefaultProfile</span></span>
<span data-ttu-id="ccaa8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccaa8-119">-Id</span><span class="sxs-lookup"><span data-stu-id="ccaa8-119">-Id</span></span>
<span data-ttu-id="ccaa8-120">풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccaa8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccaa8-121">CommonParameters</span></span>
<span data-ttu-id="ccaa8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccaa8-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccaa8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccaa8-124">입력</span><span class="sxs-lookup"><span data-stu-id="ccaa8-124">INPUTS</span></span>

### <span data-ttu-id="ccaa8-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ccaa8-125">BatchAccountContext</span></span>
<span data-ttu-id="ccaa8-126">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ccaa8-127">이름</span><span class="sxs-lookup"><span data-stu-id="ccaa8-127">String</span></span>
<span data-ttu-id="ccaa8-128">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ccaa8-129">출력</span><span class="sxs-lookup"><span data-stu-id="ccaa8-129">OUTPUTS</span></span>

## <span data-ttu-id="ccaa8-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ccaa8-130">NOTES</span></span>

## <span data-ttu-id="ccaa8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccaa8-131">RELATED LINKS</span></span>

[<span data-ttu-id="ccaa8-132">Enable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="ccaa8-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="ccaa8-133">Test-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="ccaa8-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="ccaa8-134">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ccaa8-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


