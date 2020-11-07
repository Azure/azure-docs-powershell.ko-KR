---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711784"
---
# <span data-ttu-id="3948b-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3948b-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="3948b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3948b-102">SYNOPSIS</span></span>
<span data-ttu-id="3948b-103">지정 된 Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3948b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3948b-104">SYNTAX</span></span>

### <span data-ttu-id="3948b-105">파일 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3948b-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3948b-106">RawData</span><span class="sxs-lookup"><span data-stu-id="3948b-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3948b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3948b-107">DESCRIPTION</span></span>
<span data-ttu-id="3948b-108">**새-AzureBatchCertificate** cmdlet은 지정 된 Azure Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="3948b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3948b-109">EXAMPLES</span></span>

### <span data-ttu-id="3948b-110">예제 1: 파일에서 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="3948b-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="3948b-111">이 명령은 E:\Certificates\MyCert.cer. 파일을 사용 하 여 지정 된 Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="3948b-112">예제 2: 원시 데이터의 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="3948b-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="3948b-113">첫 번째 명령은 MyCert 이라는 파일의 데이터를 $RawData 변수로 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="3948b-114">두 번째 명령은 $RawData에 저장 된 원시 데이터를 사용 하 여 지정 된 Batch 계정에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="3948b-115">변수</span><span class="sxs-lookup"><span data-stu-id="3948b-115">PARAMETERS</span></span>

### <span data-ttu-id="3948b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3948b-116">-BatchContext</span></span>
<span data-ttu-id="3948b-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3948b-118">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3948b-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3948b-119">-FilePath</span></span>
<span data-ttu-id="3948b-120">인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="3948b-121">인증서 파일은 .cer 또는 .pfx 형식 중 하나 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-121">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="3948b-122">-암호</span><span class="sxs-lookup"><span data-stu-id="3948b-122">-Password</span></span>
<span data-ttu-id="3948b-123">인증서 개인 키에 액세스 하는 데 사용할 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="3948b-124">.Pfx 형식의 인증서를 지정 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="3948b-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="3948b-125">-RawData</span></span>
<span data-ttu-id="3948b-126">.Cer 또는 .pfx 형식의 원시 인증서 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="3948b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3948b-127">-DefaultProfile</span></span>
<span data-ttu-id="3948b-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3948b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3948b-129">CommonParameters</span></span>
<span data-ttu-id="3948b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3948b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3948b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3948b-132">입력</span><span class="sxs-lookup"><span data-stu-id="3948b-132">INPUTS</span></span>

### <span data-ttu-id="3948b-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3948b-133">BatchAccountContext</span></span>
<span data-ttu-id="3948b-134">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3948b-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="3948b-135">Byte[]</span></span>
<span data-ttu-id="3948b-136">' RawData ' 매개 변수는 파이프라인에서 ' Byte [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3948b-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="3948b-137">출력</span><span class="sxs-lookup"><span data-stu-id="3948b-137">OUTPUTS</span></span>

## <span data-ttu-id="3948b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="3948b-138">NOTES</span></span>

## <span data-ttu-id="3948b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3948b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3948b-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3948b-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="3948b-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3948b-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3948b-142">-AzureBatchCertificate 제거</span><span class="sxs-lookup"><span data-stu-id="3948b-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="3948b-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3948b-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


