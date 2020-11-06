---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 51fca07847ca5bf0c73a5f2c88a41d3de166053c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527068"
---
# <span data-ttu-id="710e8-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="710e8-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="710e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="710e8-102">SYNOPSIS</span></span>
<span data-ttu-id="710e8-103">실패 한 인증서 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="710e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="710e8-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="710e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="710e8-105">DESCRIPTION</span></span>
<span data-ttu-id="710e8-106">**Stop-AzureBatchCertificateDeletion** Cmdlet은 Azure Batch 서비스에서 실패 한 인증서 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="710e8-107">인증서가 **Deletefailed** 상태에 있는 경우에만 삭제를 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="710e8-108">이 cmldet는 인증서를 **활성** 상태로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="710e8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="710e8-109">EXAMPLES</span></span>

### <span data-ttu-id="710e8-110">예제 1: 삭제 취소</span><span class="sxs-lookup"><span data-stu-id="710e8-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="710e8-111">이 명령은 지정 된 지문이 있는 인증서의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="710e8-112">변수</span><span class="sxs-lookup"><span data-stu-id="710e8-112">PARAMETERS</span></span>

### <span data-ttu-id="710e8-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="710e8-113">-BatchContext</span></span>
<span data-ttu-id="710e8-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="710e8-115">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="710e8-116">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="710e8-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="710e8-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="710e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710e8-119">-DefaultProfile</span></span>
<span data-ttu-id="710e8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="710e8-121">-지문</span><span class="sxs-lookup"><span data-stu-id="710e8-121">-Thumbprint</span></span>
<span data-ttu-id="710e8-122">이 cmdlet이 **활성** 상태로 복원 하는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="710e8-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="710e8-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="710e8-124">*손도장* 매개 변수를 파생 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="710e8-125">현재는 유효한 값만 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-125">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="710e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710e8-126">CommonParameters</span></span>
<span data-ttu-id="710e8-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710e8-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710e8-129">입력</span><span class="sxs-lookup"><span data-stu-id="710e8-129">INPUTS</span></span>

### <span data-ttu-id="710e8-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="710e8-130">BatchAccountContext</span></span>
<span data-ttu-id="710e8-131">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="710e8-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="710e8-132">출력</span><span class="sxs-lookup"><span data-stu-id="710e8-132">OUTPUTS</span></span>

## <span data-ttu-id="710e8-133">상속자</span><span class="sxs-lookup"><span data-stu-id="710e8-133">NOTES</span></span>

## <span data-ttu-id="710e8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="710e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="710e8-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="710e8-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="710e8-136">-AzureBatchCertificate 제거</span><span class="sxs-lookup"><span data-stu-id="710e8-136">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="710e8-137">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="710e8-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


