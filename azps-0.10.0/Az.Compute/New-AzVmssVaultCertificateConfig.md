---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876984"
---
# <span data-ttu-id="80f2c-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="80f2c-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="80f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="80f2c-103">키 보관소 인증서 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="80f2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80f2c-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80f2c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80f2c-105">DESCRIPTION</span></span>
<span data-ttu-id="80f2c-106">**AzVmssVaultCertificateConfig** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터에 배치 해야 하는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="80f2c-107">이 cmdlet의 출력은 Add-AzVmssSecret cmdlet과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="80f2c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="80f2c-108">EXAMPLES</span></span>

### <span data-ttu-id="80f2c-109">예제 1: 키 보관소 인증서 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="80f2c-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="80f2c-110">이 명령은 지정 된 인증서 URL에 있는 MyCerts 이라는 인증서 저장소를 사용 하는 키 자격 증명 모음 인증서 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="80f2c-111">변수</span><span class="sxs-lookup"><span data-stu-id="80f2c-111">PARAMETERS</span></span>

### <span data-ttu-id="80f2c-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="80f2c-112">-CertificateStore</span></span>
<span data-ttu-id="80f2c-113">인증서가 추가 되는 확장 집합의 가상 컴퓨터에서 인증서 저장소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="80f2c-114">이는 Windows 가상 컴퓨터 배율 집합에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="80f2c-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="80f2c-115">-CertificateUrl</span></span>
<span data-ttu-id="80f2c-116">키 자격 증명 모음에 저장 된 인증서의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="80f2c-117">U t f-8로 인코딩된 다음 JSON 개체의 base64 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="80f2c-118">{"data": " \< Base 64 인코딩-인증서 " \> ," dataType ":" pfx "," 암호 ":" \< pfx-file-password \> "}</span><span class="sxs-lookup"><span data-stu-id="80f2c-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="80f2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f2c-119">-DefaultProfile</span></span>
<span data-ttu-id="80f2c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f2c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="80f2c-121">-Confirm</span></span>
<span data-ttu-id="80f2c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f2c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f2c-123">-WhatIf</span></span>
<span data-ttu-id="80f2c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80f2c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f2c-126">CommonParameters</span></span>
<span data-ttu-id="80f2c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f2c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f2c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f2c-129">입력</span><span class="sxs-lookup"><span data-stu-id="80f2c-129">INPUTS</span></span>

### <span data-ttu-id="80f2c-130">않아야</span><span class="sxs-lookup"><span data-stu-id="80f2c-130">None</span></span>
<span data-ttu-id="80f2c-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80f2c-132">출력</span><span class="sxs-lookup"><span data-stu-id="80f2c-132">OUTPUTS</span></span>

###  
<span data-ttu-id="80f2c-133">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80f2c-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="80f2c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="80f2c-134">NOTES</span></span>

## <span data-ttu-id="80f2c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80f2c-135">RELATED LINKS</span></span>

[<span data-ttu-id="80f2c-136">추가-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="80f2c-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
