---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531756"
---
# <span data-ttu-id="17d25-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="17d25-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="17d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17d25-102">SYNOPSIS</span></span>
<span data-ttu-id="17d25-103">키 보관소 인증서 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17d25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17d25-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17d25-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17d25-105">DESCRIPTION</span></span>
<span data-ttu-id="17d25-106">**AzureRmVmssVaultCertificateConfig** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터에 배치 해야 하는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="17d25-107">이 cmdlet의 출력은 Add-AzureRmVmssSecret cmdlet과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="17d25-108">예제의</span><span class="sxs-lookup"><span data-stu-id="17d25-108">EXAMPLES</span></span>

### <span data-ttu-id="17d25-109">예제 1: 키 보관소 인증서 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="17d25-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="17d25-110">이 명령은 지정 된 인증서 URL에 있는 MyCerts 이라는 인증서 저장소를 사용 하는 키 자격 증명 모음 인증서 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="17d25-111">변수</span><span class="sxs-lookup"><span data-stu-id="17d25-111">PARAMETERS</span></span>

### <span data-ttu-id="17d25-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="17d25-112">-CertificateStore</span></span>
<span data-ttu-id="17d25-113">인증서가 추가 되는 확장 집합의 가상 컴퓨터에서 인증서 저장소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="17d25-114">이는 Windows 가상 컴퓨터 배율 집합에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d25-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="17d25-115">-CertificateUrl</span></span>
<span data-ttu-id="17d25-116">키 자격 증명 모음에 저장 된 인증서의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="17d25-117">U t f-8로 인코딩된 다음 JSON 개체의 base64 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="17d25-118">{"data": " \<Base64-encoded-certificate\> ", "dataType": "pfx", "password": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="17d25-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d25-119">-확인</span><span class="sxs-lookup"><span data-stu-id="17d25-119">-Confirm</span></span>
<span data-ttu-id="17d25-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d25-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d25-121">-WhatIf</span></span>
<span data-ttu-id="17d25-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17d25-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d25-124">CommonParameters</span></span>
<span data-ttu-id="17d25-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d25-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d25-127">입력</span><span class="sxs-lookup"><span data-stu-id="17d25-127">INPUTS</span></span>

### <span data-ttu-id="17d25-128">않아야</span><span class="sxs-lookup"><span data-stu-id="17d25-128">None</span></span>
<span data-ttu-id="17d25-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17d25-130">출력</span><span class="sxs-lookup"><span data-stu-id="17d25-130">OUTPUTS</span></span>

###  
<span data-ttu-id="17d25-131">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17d25-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="17d25-132">상속자</span><span class="sxs-lookup"><span data-stu-id="17d25-132">NOTES</span></span>

## <span data-ttu-id="17d25-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17d25-133">RELATED LINKS</span></span>

[<span data-ttu-id="17d25-134">추가-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="17d25-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)