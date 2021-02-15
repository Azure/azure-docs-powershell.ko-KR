---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182036"
---
# <span data-ttu-id="20114-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="20114-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="20114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20114-102">SYNOPSIS</span></span>
<span data-ttu-id="20114-103">인증서가 실패한 경우를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="20114-104">구문</span><span class="sxs-lookup"><span data-stu-id="20114-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20114-105">설명</span><span class="sxs-lookup"><span data-stu-id="20114-105">DESCRIPTION</span></span>
<span data-ttu-id="20114-106">**Stop-AzBatchCertificateDeletion** cmdlet은 Azure Batch 서비스에서 인증서 삭제에 실패한 삭제를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="20114-107">인증서가 **DeleteFailed** 상태인 경우 삭제를 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20114-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="20114-108">이 cmdlet은 인증서를 **활성** 상태로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="20114-109">예제</span><span class="sxs-lookup"><span data-stu-id="20114-109">EXAMPLES</span></span>

### <span data-ttu-id="20114-110">예제 1: 지우기 취소</span><span class="sxs-lookup"><span data-stu-id="20114-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="20114-111">이 명령은 지정된 지문이 있는 인증서의 지문을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="20114-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20114-112">PARAMETERS</span></span>

### <span data-ttu-id="20114-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="20114-113">-BatchContext</span></span>
<span data-ttu-id="20114-114">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="20114-115">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="20114-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="20114-116">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20114-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="20114-117">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="20114-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="20114-118">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="20114-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20114-119">-DefaultProfile</span></span>
<span data-ttu-id="20114-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20114-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20114-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="20114-121">-Thumbprint</span></span>
<span data-ttu-id="20114-122">이 cmdlet이 활성 상태로 복원하는 인증서의 **지문을 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="20114-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="20114-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="20114-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="20114-124">지문 매개 변수를 파생하는 데 사용되는 *알고리즘을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="20114-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="20114-125">현재 유효한 값은 sha1뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="20114-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="20114-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20114-126">CommonParameters</span></span>
<span data-ttu-id="20114-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20114-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20114-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20114-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20114-129">입력</span><span class="sxs-lookup"><span data-stu-id="20114-129">INPUTS</span></span>

### <span data-ttu-id="20114-130">System.String</span><span class="sxs-lookup"><span data-stu-id="20114-130">System.String</span></span>

### <span data-ttu-id="20114-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="20114-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="20114-132">출력</span><span class="sxs-lookup"><span data-stu-id="20114-132">OUTPUTS</span></span>

### <span data-ttu-id="20114-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="20114-133">System.Void</span></span>

## <span data-ttu-id="20114-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20114-134">NOTES</span></span>

## <span data-ttu-id="20114-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20114-135">RELATED LINKS</span></span>

[<span data-ttu-id="20114-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="20114-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="20114-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="20114-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="20114-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="20114-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
