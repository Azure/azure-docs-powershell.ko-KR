---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: 7e8159a7a17276d749adb89ea4e1b82118f9b2bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531453"
---
# <span data-ttu-id="88296-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="88296-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="88296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88296-102">SYNOPSIS</span></span>
<span data-ttu-id="88296-103">계정에서 인증서를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88296-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88296-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88296-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88296-105">DESCRIPTION</span></span>
<span data-ttu-id="88296-106">**제거-AzureBatchCertificate** cmdlet은 지정 된 Azure Batch 계정에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="88296-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88296-107">EXAMPLES</span></span>

### <span data-ttu-id="88296-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="88296-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="88296-109">이 명령은 지정 된 지문이 있는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="88296-110">예제 2: 모든 활성 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="88296-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="88296-111">이 명령은 Get-AzureBatchCertificate cmdlet을 사용 하 여 활성 상태인 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88296-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="88296-112">이 명령은 파이프라인 연산자를 사용 하 여 활성 인증서를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88296-113">해당 cmdlet은 각 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="88296-114">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="88296-115">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88296-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="88296-116">변수</span><span class="sxs-lookup"><span data-stu-id="88296-116">PARAMETERS</span></span>

### <span data-ttu-id="88296-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88296-117">-BatchContext</span></span>
<span data-ttu-id="88296-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88296-119">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88296-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88296-120">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88296-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88296-121">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88296-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88296-122">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88296-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88296-123">-DefaultProfile</span></span>
<span data-ttu-id="88296-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88296-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88296-125">-지문</span><span class="sxs-lookup"><span data-stu-id="88296-125">-Thumbprint</span></span>
<span data-ttu-id="88296-126">이 cmdlet이 삭제 하는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="88296-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="88296-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="88296-128">*손도장* 매개 변수를 파생 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="88296-129">현재는 유효한 값만 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="88296-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="88296-130">-확인</span><span class="sxs-lookup"><span data-stu-id="88296-130">-Confirm</span></span>
<span data-ttu-id="88296-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88296-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88296-132">-WhatIf</span></span>
<span data-ttu-id="88296-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88296-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88296-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88296-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88296-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88296-135">CommonParameters</span></span>
<span data-ttu-id="88296-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88296-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88296-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88296-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88296-138">입력</span><span class="sxs-lookup"><span data-stu-id="88296-138">INPUTS</span></span>

### <span data-ttu-id="88296-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88296-139">System.String</span></span>

### <span data-ttu-id="88296-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88296-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="88296-141">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88296-141">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="88296-142">출력</span><span class="sxs-lookup"><span data-stu-id="88296-142">OUTPUTS</span></span>

### <span data-ttu-id="88296-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="88296-143">System.Void</span></span>

## <span data-ttu-id="88296-144">상속자</span><span class="sxs-lookup"><span data-stu-id="88296-144">NOTES</span></span>

## <span data-ttu-id="88296-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88296-145">RELATED LINKS</span></span>

[<span data-ttu-id="88296-146">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="88296-146">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="88296-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="88296-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="88296-148">새-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="88296-148">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="88296-149">중지-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="88296-149">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="88296-150">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88296-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


