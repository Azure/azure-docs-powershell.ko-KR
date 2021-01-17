---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350570"
---
# <span data-ttu-id="0b834-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="0b834-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="0b834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b834-102">SYNOPSIS</span></span>
<span data-ttu-id="0b834-103">Batch 계정에 대해 Batch 지원되는 이미지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="0b834-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b834-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b834-105">설명</span><span class="sxs-lookup"><span data-stu-id="0b834-105">DESCRIPTION</span></span>
<span data-ttu-id="0b834-106">**Get-AzBatchSupportedImage** cmdlet은 Azure Batch 계정에서 사용할 수 있는 지원되는 가상 머신 이미지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="0b834-107">*BatchContext* 매개 변수를 사용하여 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="0b834-108">예제</span><span class="sxs-lookup"><span data-stu-id="0b834-108">EXAMPLES</span></span>

### <span data-ttu-id="0b834-109">예제 1: 지원되는 모든 이미지 다운로드</span><span class="sxs-lookup"><span data-stu-id="0b834-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="0b834-110">첫 번째 명령은 **Get-AzBatchAccountKey를** 사용하여 구독에 대한 액세스 키를 포함하는 Batch 계정 컨텍스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="0b834-111">이 명령은 다음 명령에 사용할 $Context 변수에 컨텍스트를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="0b834-112">두 번째 명령은 해당 Batch 계정에 대해 지원되는 모든 이미지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="0b834-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b834-113">PARAMETERS</span></span>

### <span data-ttu-id="0b834-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b834-114">-BatchContext</span></span>
<span data-ttu-id="0b834-115">Batch 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="0b834-116">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="0b834-117">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="0b834-118">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="0b834-119">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0b834-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b834-120">-DefaultProfile</span></span>
<span data-ttu-id="0b834-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b834-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="0b834-122">-Filter</span></span>
<span data-ttu-id="0b834-123">지원되는 이미지에 대한 OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="0b834-124">필터를 지정하지 않으면 이 cmdlet은 Batch 계정에서 지원하는 모든 이미지를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b834-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0b834-125">-MaxCount</span></span>
<span data-ttu-id="0b834-126">반환할 지원되는 이미지의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b834-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b834-127">CommonParameters</span></span>
<span data-ttu-id="0b834-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b834-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b834-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b834-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b834-130">입력</span><span class="sxs-lookup"><span data-stu-id="0b834-130">INPUTS</span></span>

### <span data-ttu-id="0b834-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b834-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0b834-132">출력</span><span class="sxs-lookup"><span data-stu-id="0b834-132">OUTPUTS</span></span>

### <span data-ttu-id="0b834-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="0b834-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="0b834-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b834-134">NOTES</span></span>

## <span data-ttu-id="0b834-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b834-135">RELATED LINKS</span></span>

[<span data-ttu-id="0b834-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b834-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)