---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: 56ec7eafcea7233697089d692b2799fa6c9b744a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043002"
---
# <span data-ttu-id="4a859-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="4a859-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="4a859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a859-102">SYNOPSIS</span></span>
<span data-ttu-id="4a859-103">일괄 처리 계정에 대해 일괄 지원 되는 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="4a859-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a859-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a859-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4a859-105">DESCRIPTION</span></span>
<span data-ttu-id="4a859-106">**AzBatchSupportedImage** Cmdlet은 Azure Batch 계정에서 사용할 수 있는 지원 되는 가상 컴퓨터 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="4a859-107">*Batchcontext* 매개 변수를 사용 하 여 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="4a859-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4a859-108">EXAMPLES</span></span>

### <span data-ttu-id="4a859-109">예제 1: 사용 가능한 모든 지원 되는 이미지 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a859-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="4a859-110">첫 번째 명령은 **AzBatchAccountKey** 를 사용 하 여 구독에 대 한 선택 키를 포함 하는 일괄 처리 계정 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="4a859-111">명령은 다음 명령에 사용할 컨텍스트를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="4a859-112">두 번째 명령은 해당 Batch 계정에서 사용할 수 있는 지원 되는 모든 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="4a859-113">변수</span><span class="sxs-lookup"><span data-stu-id="4a859-113">PARAMETERS</span></span>

### <span data-ttu-id="4a859-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4a859-114">-BatchContext</span></span>
<span data-ttu-id="4a859-115">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="4a859-116">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="4a859-117">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="4a859-118">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="4a859-119">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4a859-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a859-120">-DefaultProfile</span></span>
<span data-ttu-id="4a859-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a859-122">-필터</span><span class="sxs-lookup"><span data-stu-id="4a859-122">-Filter</span></span>
<span data-ttu-id="4a859-123">지원 되는 이미지에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="4a859-124">필터를 지정 하지 않으면이 cmdlet은 일괄 계정에서 지 원하는 모든 이미지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="4a859-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4a859-125">-MaxCount</span></span>
<span data-ttu-id="4a859-126">반환할 지원 되는 최대 이미지 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="4a859-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a859-127">CommonParameters</span></span>
<span data-ttu-id="4a859-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a859-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a859-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a859-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a859-130">입력</span><span class="sxs-lookup"><span data-stu-id="4a859-130">INPUTS</span></span>

### <span data-ttu-id="4a859-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4a859-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4a859-132">출력</span><span class="sxs-lookup"><span data-stu-id="4a859-132">OUTPUTS</span></span>

### <span data-ttu-id="4a859-133">Microsoft.Azure.Commands.Batch. Pa Ageinformation 모델</span><span class="sxs-lookup"><span data-stu-id="4a859-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="4a859-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4a859-134">NOTES</span></span>

## <span data-ttu-id="4a859-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a859-135">RELATED LINKS</span></span>
[<span data-ttu-id="4a859-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4a859-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)