---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531839"
---
# <span data-ttu-id="9cb9a-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="9cb9a-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="9cb9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb9a-103">실패 한 인증서 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cb9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cb9a-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cb9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9cb9a-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb9a-106">**Stop-AzureBatchCertificateDeletion** Cmdlet은 Azure Batch 서비스에서 실패 한 인증서 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="9cb9a-107">인증서가 **Deletefailed** 상태에 있는 경우에만 삭제를 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="9cb9a-108">이 cmldet는 인증서를 **활성** 상태로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="9cb9a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9cb9a-109">EXAMPLES</span></span>

### <span data-ttu-id="9cb9a-110">예제 1: 삭제 취소</span><span class="sxs-lookup"><span data-stu-id="9cb9a-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="9cb9a-111">이 명령은 지정 된 지문이 있는 인증서의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="9cb9a-112">변수</span><span class="sxs-lookup"><span data-stu-id="9cb9a-112">PARAMETERS</span></span>

### <span data-ttu-id="9cb9a-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9cb9a-113">-BatchContext</span></span>
<span data-ttu-id="9cb9a-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9cb9a-115">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9cb9a-116">-지문</span><span class="sxs-lookup"><span data-stu-id="9cb9a-116">-Thumbprint</span></span>
<span data-ttu-id="9cb9a-117">이 cmdlet이 **활성** 상태로 복원 하는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb9a-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9cb9a-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="9cb9a-119">*손도장* 매개 변수를 파생 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="9cb9a-120">현재는 유효한 값만 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-120">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb9a-121">-DefaultProfile</span></span>
<span data-ttu-id="9cb9a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cb9a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb9a-123">CommonParameters</span></span>
<span data-ttu-id="9cb9a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb9a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb9a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb9a-126">입력</span><span class="sxs-lookup"><span data-stu-id="9cb9a-126">INPUTS</span></span>

### <span data-ttu-id="9cb9a-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9cb9a-127">BatchAccountContext</span></span>
<span data-ttu-id="9cb9a-128">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cb9a-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9cb9a-129">출력</span><span class="sxs-lookup"><span data-stu-id="9cb9a-129">OUTPUTS</span></span>

## <span data-ttu-id="9cb9a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9cb9a-130">NOTES</span></span>

## <span data-ttu-id="9cb9a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cb9a-131">RELATED LINKS</span></span>

[<span data-ttu-id="9cb9a-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9cb9a-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9cb9a-133">-AzureBatchCertificate 제거</span><span class="sxs-lookup"><span data-stu-id="9cb9a-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="9cb9a-134">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9cb9a-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


