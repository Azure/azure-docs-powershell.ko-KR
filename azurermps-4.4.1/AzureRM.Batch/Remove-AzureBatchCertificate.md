---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528271"
---
# <span data-ttu-id="059db-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="059db-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="059db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059db-102">SYNOPSIS</span></span>
<span data-ttu-id="059db-103">계정에서 인증서를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="059db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="059db-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="059db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="059db-105">DESCRIPTION</span></span>
<span data-ttu-id="059db-106">**제거-AzureBatchCertificate** cmdlet은 지정 된 Azure Batch 계정에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="059db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="059db-107">EXAMPLES</span></span>

### <span data-ttu-id="059db-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="059db-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="059db-109">이 명령은 지정 된 지문이 있는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="059db-110">예제 2: 모든 활성 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="059db-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="059db-111">이 명령은 Get-AzureBatchCertificate cmdlet을 사용 하 여 활성 상태인 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059db-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="059db-112">이 명령은 파이프라인 연산자를 사용 하 여 활성 인증서를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="059db-113">해당 cmdlet은 각 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="059db-114">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="059db-115">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="059db-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="059db-116">변수</span><span class="sxs-lookup"><span data-stu-id="059db-116">PARAMETERS</span></span>

### <span data-ttu-id="059db-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="059db-117">-BatchContext</span></span>
<span data-ttu-id="059db-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="059db-119">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="059db-120">-지문</span><span class="sxs-lookup"><span data-stu-id="059db-120">-Thumbprint</span></span>
<span data-ttu-id="059db-121">이 cmdlet이 삭제 하는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="059db-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="059db-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="059db-123">*손도장* 매개 변수를 파생 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="059db-124">현재는 유효한 값만 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="059db-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="059db-125">-확인</span><span class="sxs-lookup"><span data-stu-id="059db-125">-Confirm</span></span>
<span data-ttu-id="059db-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059db-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059db-127">-WhatIf</span></span>
<span data-ttu-id="059db-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="059db-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059db-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="059db-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059db-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059db-130">-DefaultProfile</span></span>
<span data-ttu-id="059db-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="059db-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059db-132">CommonParameters</span></span>
<span data-ttu-id="059db-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059db-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059db-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059db-135">입력</span><span class="sxs-lookup"><span data-stu-id="059db-135">INPUTS</span></span>

### <span data-ttu-id="059db-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="059db-136">BatchAccountContext</span></span>
<span data-ttu-id="059db-137">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="059db-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="059db-138">출력</span><span class="sxs-lookup"><span data-stu-id="059db-138">OUTPUTS</span></span>

## <span data-ttu-id="059db-139">상속자</span><span class="sxs-lookup"><span data-stu-id="059db-139">NOTES</span></span>

## <span data-ttu-id="059db-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="059db-140">RELATED LINKS</span></span>

[<span data-ttu-id="059db-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="059db-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="059db-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="059db-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="059db-143">새-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="059db-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="059db-144">중지-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="059db-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="059db-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="059db-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


