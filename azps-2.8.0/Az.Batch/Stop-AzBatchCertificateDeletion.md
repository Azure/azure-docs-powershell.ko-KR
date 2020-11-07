---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: cdddb11071bb7e4c4d57bd44fb2bbe5193b4153f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880025"
---
# <span data-ttu-id="cb4d5-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="cb4d5-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="cb4d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4d5-103">실패 한 인증서 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="cb4d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb4d5-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb4d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="cb4d5-106">**AzBatchCertificateDeletion** Cmdlet은 Azure Batch 서비스에서 인증서 삭제 실패를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="cb4d5-107">인증서가 **Deletefailed** 상태에 있는 경우에만 삭제를 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="cb4d5-108">이 cmdlet은 인증서를 **활성** 상태로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="cb4d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cb4d5-109">EXAMPLES</span></span>

### <span data-ttu-id="cb4d5-110">예제 1: 삭제 취소</span><span class="sxs-lookup"><span data-stu-id="cb4d5-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="cb4d5-111">이 명령은 지정 된 지문이 있는 인증서의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="cb4d5-112">변수</span><span class="sxs-lookup"><span data-stu-id="cb4d5-112">PARAMETERS</span></span>

### <span data-ttu-id="cb4d5-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cb4d5-113">-BatchContext</span></span>
<span data-ttu-id="cb4d5-114">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cb4d5-115">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cb4d5-116">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cb4d5-117">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cb4d5-118">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cb4d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4d5-119">-DefaultProfile</span></span>
<span data-ttu-id="cb4d5-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb4d5-121">-지문</span><span class="sxs-lookup"><span data-stu-id="cb4d5-121">-Thumbprint</span></span>
<span data-ttu-id="cb4d5-122">이 cmdlet이 **활성** 상태로 복원 하는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="cb4d5-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="cb4d5-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="cb4d5-124">*손도장* 매개 변수를 파생 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="cb4d5-125">현재는 유효한 값만 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="cb4d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4d5-126">CommonParameters</span></span>
<span data-ttu-id="cb4d5-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4d5-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb4d5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4d5-129">입력</span><span class="sxs-lookup"><span data-stu-id="cb4d5-129">INPUTS</span></span>

### <span data-ttu-id="cb4d5-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cb4d5-130">System.String</span></span>

### <span data-ttu-id="cb4d5-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cb4d5-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cb4d5-132">출력</span><span class="sxs-lookup"><span data-stu-id="cb4d5-132">OUTPUTS</span></span>

### <span data-ttu-id="cb4d5-133">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="cb4d5-133">System.Void</span></span>

## <span data-ttu-id="cb4d5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="cb4d5-134">NOTES</span></span>

## <span data-ttu-id="cb4d5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb4d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb4d5-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cb4d5-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cb4d5-137">제거-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="cb4d5-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="cb4d5-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb4d5-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


