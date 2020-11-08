---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216421"
---
# <span data-ttu-id="6733a-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6733a-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="6733a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6733a-102">SYNOPSIS</span></span>
<span data-ttu-id="6733a-103">지정 된 Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="6733a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6733a-104">SYNTAX</span></span>

### <span data-ttu-id="6733a-105">파일 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6733a-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6733a-106">RawData</span><span class="sxs-lookup"><span data-stu-id="6733a-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6733a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6733a-107">DESCRIPTION</span></span>
<span data-ttu-id="6733a-108">**새 AzBatchCertificate** cmdlet은 지정 된 Azure Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="6733a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6733a-109">EXAMPLES</span></span>

### <span data-ttu-id="6733a-110">예제 1: 파일에서 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="6733a-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="6733a-111">이 명령은 E:\Certificates\MyCert.cer. 파일을 사용 하 여 지정 된 Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="6733a-112">예제 2: 원시 데이터의 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="6733a-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="6733a-113">첫 번째 명령은 MyCert 이라는 파일의 데이터를 $RawData 변수로 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="6733a-114">두 번째 명령은 $RawData에 저장 된 원시 데이터를 사용 하 여 지정 된 Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="6733a-115">변수</span><span class="sxs-lookup"><span data-stu-id="6733a-115">PARAMETERS</span></span>

### <span data-ttu-id="6733a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6733a-116">-BatchContext</span></span>
<span data-ttu-id="6733a-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6733a-118">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6733a-119">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6733a-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6733a-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6733a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6733a-122">-DefaultProfile</span></span>
<span data-ttu-id="6733a-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6733a-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="6733a-124">-FilePath</span></span>
<span data-ttu-id="6733a-125">인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="6733a-126">인증서 파일은 .cer 또는 .pfx 형식 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6733a-127">-종류</span><span class="sxs-lookup"><span data-stu-id="6733a-127">-Kind</span></span>
<span data-ttu-id="6733a-128">만들 인증서의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-128">The kind of certificate to create.</span></span> <span data-ttu-id="6733a-129">이를 지정 하지 않으면 암호가 없는 모든 인증서가 CER이 고 암호가 있는 모든 인증서가 PFX로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6733a-130">-암호</span><span class="sxs-lookup"><span data-stu-id="6733a-130">-Password</span></span>
<span data-ttu-id="6733a-131">인증서 개인 키에 액세스 하는 데 사용할 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="6733a-132">.Pfx 형식의 인증서를 지정 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6733a-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="6733a-133">-RawData</span></span>
<span data-ttu-id="6733a-134">.Cer 또는 .pfx 형식의 원시 인증서 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6733a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6733a-135">CommonParameters</span></span>
<span data-ttu-id="6733a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6733a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6733a-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6733a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6733a-138">입력</span><span class="sxs-lookup"><span data-stu-id="6733a-138">INPUTS</span></span>

### <span data-ttu-id="6733a-139">Byte []</span><span class="sxs-lookup"><span data-stu-id="6733a-139">System.Byte[]</span></span>

### <span data-ttu-id="6733a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6733a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6733a-141">출력</span><span class="sxs-lookup"><span data-stu-id="6733a-141">OUTPUTS</span></span>

### <span data-ttu-id="6733a-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6733a-142">System.Void</span></span>

## <span data-ttu-id="6733a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="6733a-143">NOTES</span></span>

## <span data-ttu-id="6733a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6733a-144">RELATED LINKS</span></span>

[<span data-ttu-id="6733a-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6733a-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="6733a-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6733a-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6733a-147">제거-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6733a-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="6733a-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6733a-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
