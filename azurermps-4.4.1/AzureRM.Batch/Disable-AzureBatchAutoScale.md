---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531850"
---
# <span data-ttu-id="278a0-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="278a0-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="278a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278a0-102">SYNOPSIS</span></span>
<span data-ttu-id="278a0-103">풀의 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="278a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="278a0-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="278a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="278a0-105">DESCRIPTION</span></span>
<span data-ttu-id="278a0-106">**Disable-AzureBatchAutoScale 크기 조정** cmdlet은 지정 된 풀의 자동 크기 조정을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="278a0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="278a0-107">EXAMPLES</span></span>

### <span data-ttu-id="278a0-108">예제 1: 풀의 자동 크기 조정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="278a0-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="278a0-109">이 명령은 MyPool 이라는 풀에 대해 자동 크기 조정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="278a0-110">변수</span><span class="sxs-lookup"><span data-stu-id="278a0-110">PARAMETERS</span></span>

### <span data-ttu-id="278a0-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="278a0-111">-BatchContext</span></span>
<span data-ttu-id="278a0-112">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="278a0-113">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="278a0-114">-Id</span><span class="sxs-lookup"><span data-stu-id="278a0-114">-Id</span></span>
<span data-ttu-id="278a0-115">풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-115">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="278a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278a0-116">-DefaultProfile</span></span>
<span data-ttu-id="278a0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="278a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278a0-118">CommonParameters</span></span>
<span data-ttu-id="278a0-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278a0-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="278a0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278a0-121">입력</span><span class="sxs-lookup"><span data-stu-id="278a0-121">INPUTS</span></span>

### <span data-ttu-id="278a0-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="278a0-122">BatchAccountContext</span></span>
<span data-ttu-id="278a0-123">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="278a0-124">이름</span><span class="sxs-lookup"><span data-stu-id="278a0-124">String</span></span>
<span data-ttu-id="278a0-125">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="278a0-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="278a0-126">출력</span><span class="sxs-lookup"><span data-stu-id="278a0-126">OUTPUTS</span></span>

## <span data-ttu-id="278a0-127">상속자</span><span class="sxs-lookup"><span data-stu-id="278a0-127">NOTES</span></span>

## <span data-ttu-id="278a0-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="278a0-128">RELATED LINKS</span></span>

[<span data-ttu-id="278a0-129">Enable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="278a0-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="278a0-130">Test-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="278a0-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="278a0-131">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="278a0-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


